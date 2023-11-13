<template>
  <div>
    <div>
      <input v-model="sotap" type="text" placeholder="Số tập" />
      <input v-model="idfilm" type="text" placeholder="ID Film" />
      <button @click="handleButtonClick">nhấn vào Play</button>
    </div>
    <jwplayer :options = 'jwoptions' :videoSrc="yourVideoSource" :logo="yourLogoPath"></jwplayer>
  </div> 
  </template>
  
  <script>
  import axios from "axios"
  import jwplayer from '~/components/jwplayer.vue'
  
  export default {
    
    data() {
      return {
        sotap: "94364",
        idfilm: "4931",
        yourVideoSource: 'pngs/output.m3u8',
        yourLogoPath: 'logo.png',
        jwoptions: {
          //file: 'pngs/output.m3u8',
          heigh: 360,
          width: 640,
          mute: true,
          
        },
        
      };
    },
    components: {
      jwplayer
    },
    methods: {
      
    async fetchM3U8URL(url) {
      try {
        const response = await axios.get(url);
        const m3u8URL = response.data;
        console.log(url)
        
        return m3u8URL;
      } catch (error) {
        console.error('Lỗi khi gọi API:', error);
        return null;
      }
    },
    async changeVideoSource(url) {
      const m3u8 = await this.fetchM3U8URL(url);
      if (m3u8) {
        console.log('có file m3u8 nhé dm')
        //console.log(this.filem3u8)
        this.yourVideoSource = url + '/file.m3u8'
        this.jwoptions = {
          //file: "pngs/test.m3u8",
          heigh: 360,
          width: 640,
          mute: true,
        }
        
        alert('Video đã thay đổi thành: ')
      } else {
        alert('Không thể thay đổi video.');
      
    }
    },
    handleButtonClick() {
      
        // Xử lý sự kiện khi nút được nhấn
        
        alert("Số tập: " + this.sotap + " & idfilm: " + this.idfilm);
        let url = '//' + '127.0.0.1:3000' + '/g?idunique=' + this.sotap + '&idfilm=' + this.idfilm
        // await this.changeVideoSource(url)
        this.yourVideoSource = url + '/file.m3u8'
        this.jwoptions = {
          //file: "pngs/test.m3u8",
          heigh: 360,
          width: 640,
          mute: true,
        }
        
        alert('Video đã thay đổi thành: ')
      },
    },
    
  };
  </script>