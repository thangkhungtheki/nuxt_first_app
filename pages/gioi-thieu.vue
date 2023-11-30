<template>
  <div>
    <b-breadcrumb :items="items"></b-breadcrumb>
    <player></player>
    <Chapagination></Chapagination>
  </div>
  </template>
  
  <script>
  import player from "~/components/jwplayer.op.vue"
  import Chapagination from "../components/chapagination.vue";
    export default {
    components : {
      Chapagination,
    },
    player,
    
    data() {
        return {
            items: [
                {
                    text: 'Trang chủ',
                    href: '#'
                },
                {
                    text: 'Nội dung',
                    href: '#'
                },
                {
                    text: 'Thư viện',
                    active: true
                }
            ]
        };
    },
    components: { Chapagination }
}
  </script>