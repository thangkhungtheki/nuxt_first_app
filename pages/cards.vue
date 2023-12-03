<template>
    <b-container class="custom-container" fluid>
      <b-row class="custom-row">
        <b-col lg="2" md="6" sm="6" v-for="(image, index) in images" :key=image.id class="custom-col">
            
          <img :src="image.url" alt="Hình ảnh" class="img-fluid custom-image"/>
          <div><span>{{ image.content }}</span></div>
        </b-col>
      </b-row>
    </b-container>
  </template>
  
  <script>
  export default {
    
    data() {
      return {
        images: [
          { id: 1, url: 'jpeg/1.jpeg', content: "aaaa" },
          { id: 2, url: 'jpeg/2.webp', content: "bbbb" },
          { id: 3, url: 'jpeg/3.webp', content: "cccc"},
          { id: 4, url: 'jpeg/4.jpg' , content: "dddd" },
          { id: 5, url: 'jpeg/5.jpg' , content: "eeee"},
          { id: 6, url: 'jpeg/6.webp', content: "ffff" },
          { id: 7, url: 'jpeg/1.jpeg', content: "gggg" },
          { id: 8, url: 'jpeg/2.webp' , content: "hhhhh"},
          { id: 9, url: 'jpeg/3.webp' , content: "ggggg"},
          { id: 10, url: 'jpeg/4.jpg' , content: "aaaa"},
          { id: 11, url: 'jpeg/5.jpg' , content: "hhhh"},
          { id: 12, url: 'jpeg/6.webp' , content: "eeeee"},
          // Thêm các đối tượng hình ảnh khác nếu cần
        ]
      };
    }
  };
  </script>

<style scoped>
.custom-image {
  max-width: 100%;
  width: 100%;
  height: 80%;
  border: 1px solid #fff; /* Điều chỉnh độ dày của viền */
}
.custom-col {
    max-width: 220px;
    padding: 5px 5px;
    flex: 0 0 auto;
}
/* .custom-container {
    max-width: 800px;
} */
.custom-row {
    max-width: 1200px;
}
</style>