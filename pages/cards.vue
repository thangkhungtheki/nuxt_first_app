<template>
    <b-container class="custom-container" fluid="sm">
      <b-row class="custom-row">
        <b-col lg="2" md="6" sm="6" v-for="(image, index) in images" :key="image.id"  class="custom-col">
          <img :src="image.url" alt="Hình ảnh" class="img-fluid custom-image">
        </b-col>
      </b-row>
    </b-container>
  </template>
  
  <script>
  export default {
    layout: 'layout1',
    data() {
      return {
        images: [
          { id: 1, url: 'jpeg/1.jpeg' },
          { id: 2, url: 'jpeg/2.webp' },
          { id: 3, url: 'jpeg/3.webp' },
          { id: 4, url: 'jpeg/4.jpg' },
          { id: 5, url: 'jpeg/5.jpg' },
          { id: 6, url: 'jpeg/6.webp' },
          { id: 7, url: 'jpeg/1.jpeg' },
          { id: 8, url: 'jpeg/2.webp' },
          { id: 9, url: 'jpeg/3.webp' },
          { id: 10, url: 'jpeg/4.jpg' },
          { id: 11, url: 'jpeg/5.jpg' },
          { id: 12, url: 'jpeg/6.webp' },
          // Thêm các đối tượng hình ảnh khác nếu cần
        ]
      };
    }
  };
  </script>

<style scoped>
.custom-image {
  max-width: 100%;
  height: 100%;
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