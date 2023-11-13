<template>
  <div>
    <b-breadcrumb :items="items"></b-breadcrumb>
    <player></player>
  </div>
  </template>
  
  <script>
  import player from "~/components/jwplayer.op.vue"
    export default {
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
        }
      }
    }
  </script>