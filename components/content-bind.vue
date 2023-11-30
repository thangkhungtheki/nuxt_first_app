<template>
  <b-container class="custom-container" fluid="xl">
    <b-row class="custom-row justify-content-center">
      <b-col lg="2" md="6" sm="6" v-for="(image, index) in images" :key="image.id" class="custom-col">
        <img :src="image.url" alt="Hình ảnh" :class="{ 'img-fluid': isSmallScreen, 'custom-image': true }">
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
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
          ],
      isSmallScreen: false,
    };
  },
  mounted() {
    // Kiểm tra kích thước màn hình khi trang được tải
    this.checkScreenSize();

    // Thêm sự kiện lắng nghe để kiểm tra lại khi kích thước màn hình thay đổi
    window.addEventListener('resize', this.checkScreenSize);
  },
  methods: {
    checkScreenSize() {
      // Kiểm tra kích thước màn hình và cập nhật giá trị isSmallScreen
      this.isSmallScreen = window.innerWidth < 768; // Giả sử màn hình nhỏ hơn 768px là màn hình nhỏ
    },
  },
  beforeDestroy() {
    // Gỡ bỏ sự kiện lắng nghe khi component bị hủy
    window.removeEventListener('resize', this.checkScreenSize);
  },
};
</script>

<style scoped>
/* Thêm các tùy chọn CSS cho custom-container, custom-row, custom-col, và custom-image nếu cần */
.custom-image {
    max-width: 100%;
    height: 100%;
    border: 1px solid #fff; /* Điều chỉnh độ dày của viền */
  }
  .custom-col {
      max-width: auto;
      padding: 5px 5px;
      /* flex: 0 0 auto; */
  }
  /* .custom-container {
      max-width: 800px;
  } */
  .custom-row {
      /* max-width: 1200px; */
  }
  .wrapperc {
    max-width: 1000px;
  }
  .col-sm-6 {
    max-width: 200px;
  }
  
</style>
