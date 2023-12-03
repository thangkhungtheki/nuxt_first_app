<template>
  <div>
    <!-- Hiển thị danh sách bài viết theo trang -->
    <div v-for="post in paginatedPosts" :key="post.id">
      {{ post.title }}
    </div>

    <!-- Sử dụng component Pagination -->
    <Pagination :currentPage="currentPage" :pageCount="pageCount" @pageChange="changePage" />
  </div>
</template>

<script>
import Pagination from '~/components/pagination.vue';

export default {
  components: {
    Pagination
  },
  data() {
    return {
      posts: [
        { title: 1, id: 1 },
        { title: 2, id: 2 },
        { title: 3, id: 3 },
        { title: 1, id: 4 },
        { title: 2, id: 5 },
        { title: 3, id: 6 },
        { title: 1, id: 7 },
        { title: 2, id: 8 },
        { title: 3, id: 9 },
        { title: 1, id: 10 },
        { title: 2, id: 11 },
        { title: 3, id: 12 },
        { title: 1, id: 13 },
        { title: 2, id: 14 },
        { title: 3, id: 15 },
        { title: 1, id: 16 },
        { title: 2, id: 17 },
        { title: 3, id: 18 },
      ], // Danh sách bài viết
      itemsPerPage: 5, // Số lượng bài viết trên mỗi trang
      currentPage: 1 // Trang hiện tại
    };
  },
  computed: {
    pageCount() {
      return Math.ceil(this.posts.length / this.itemsPerPage);
    },
    paginatedPosts() {
      const startIndex = (this.currentPage - 1) * this.itemsPerPage;
      const endIndex = startIndex + this.itemsPerPage;
      return this.posts.slice(startIndex, endIndex);
    }
  },
  methods: {
    changePage(pageNumber) {
      this.currentPage = pageNumber;
    }
  }
};
</script>
