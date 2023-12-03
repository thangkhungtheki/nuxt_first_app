<template>
    <div>
        <!-- Hiển thị danh sách bài viết theo trang -->
        <div >
            <b-container class="custom-container" fluid>
                <b-row class="custom-row">
                    <b-col lg="2" md="6" sm="6" class="custom-col" v-for="post in paginatedPosts" :key="post.id">

                        <img :src="post.url" alt="Hình ảnh" class="img-fluid custom-image" />

                        <div><span>{{ post.content }}</span></div>
                    </b-col>
                </b-row>
            </b-container>
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
            images: [
                { id: 1, url: 'jpeg/1.jpeg', content: "aaaa" },
                { id: 2, url: 'jpeg/2.webp', content: "bbbb" },
                { id: 3, url: 'jpeg/3.webp', content: "cccc" },
                { id: 4, url: 'jpeg/4.jpg', content: "dddd" },
                { id: 5, url: 'jpeg/5.jpg', content: "eeee" },
                { id: 6, url: 'jpeg/6.webp', content: "ffff" },
                { id: 7, url: 'jpeg/1.jpeg', content: "gggg" },
                { id: 8, url: 'jpeg/2.webp', content: "hhhhh" },
                { id: 9, url: 'jpeg/3.webp', content: "ggggg" },
                { id: 10, url: 'jpeg/4.jpg', content: "aaaa" },
                { id: 11, url: 'jpeg/5.jpg', content: "hhhh" },
                { id: 12, url: 'jpeg/6.webp', content: "eeeee" },
                { id: 13, url: 'jpeg/1.jpeg', content: "aaaa" },
                { id: 14, url: 'jpeg/2.webp', content: "bbbb" },
                { id: 15, url: 'jpeg/3.webp', content: "cccc" },
                { id: 16, url: 'jpeg/4.jpg', content: "dddd" },
                { id: 17, url: 'jpeg/5.jpg', content: "eeee" },
                { id: 18, url: 'jpeg/6.webp', content: "ffff" },
                { id: 19, url: 'jpeg/1.jpeg', content: "gggg" },
                { id: 20, url: 'jpeg/2.webp', content: "hhhhh" },
                { id: 21, url: 'jpeg/3.webp', content: "ggggg" },
                { id: 22, url: 'jpeg/4.jpg', content: "aaaa" },
                { id: 23, url: 'jpeg/5.jpg', content: "hhhh" },
                { id: 24, url: 'jpeg/6.webp', content: "eeeee" },
                { id: 25, url: 'jpeg/1.jpeg', content: "aaaa" },
                { id: 26, url: 'jpeg/2.webp', content: "bbbb" },
                { id: 27, url: 'jpeg/3.webp', content: "cccc" },
                { id: 28, url: 'jpeg/4.jpg', content: "dddd" },
                { id: 29, url: 'jpeg/5.jpg', content: "eeee" },
                { id: 30, url: 'jpeg/6.webp', content: "ffff" },
                { id: 31, url: 'jpeg/1.jpeg', content: "gggg" },
                { id: 32, url: 'jpeg/2.webp', content: "hhhhh" },
                { id: 33, url: 'jpeg/3.webp', content: "ggggg" },
                { id: 34, url: 'jpeg/4.jpg', content: "aaaa" },
                { id: 35, url: 'jpeg/5.jpg', content: "hhhh" },
                { id: 36, url: 'jpeg/6.webp', content: "eeeee" },
                { id: 37, url: 'jpeg/1.jpeg', content: "aaaa" },
                { id: 38, url: 'jpeg/2.webp', content: "bbbb" },
                { id: 39, url: 'jpeg/3.webp', content: "cccc" },
                { id: 40, url: 'jpeg/4.jpg', content: "dddd" },
                { id: 41, url: 'jpeg/5.jpg', content: "eeee" },
                { id: 42, url: 'jpeg/6.webp', content: "ffff" },
                { id: 43, url: 'jpeg/1.jpeg', content: "gggg" },
                { id: 44, url: 'jpeg/2.webp', content: "hhhhh" },
                { id: 45, url: 'jpeg/3.webp', content: "ggggg" },
                { id: 46, url: 'jpeg/4.jpg', content: "aaaa" },
                { id: 47, url: 'jpeg/5.jpg', content: "hhhh" },
                { id: 48, url: 'jpeg/6.webp', content: "eeeee" },
                { id: 49, url: 'jpeg/1.jpeg', content: "aaaa" },
                { id: 50, url: 'jpeg/2.webp', content: "bbbb" },
                { id: 51, url: 'jpeg/3.webp', content: "cccc" },
                { id: 52, url: 'jpeg/4.jpg', content: "dddd" },
                { id: 53, url: 'jpeg/5.jpg', content: "eeee" },
                { id: 54, url: 'jpeg/6.webp', content: "ffff" },
                { id: 55, url: 'jpeg/1.jpeg', content: "gggg" },
                { id: 56, url: 'jpeg/2.webp', content: "hhhhh" },
                { id: 57, url: 'jpeg/3.webp', content: "ggggg" },
                { id: 58, url: 'jpeg/4.jpg', content: "aaaa" },
                { id: 59, url: 'jpeg/5.jpg', content: "hhhh" },
                { id: 60, url: 'jpeg/6.webp', content: "eeeee" },
                { id: 61, url: 'jpeg/1.jpeg', content: "aaaa" },
                { id: 62, url: 'jpeg/2.webp', content: "bbbb" },
                { id: 63, url: 'jpeg/3.webp', content: "cccc" },
                { id: 64, url: 'jpeg/4.jpg', content: "dddd" },
                { id: 65, url: 'jpeg/5.jpg', content: "eeee" },
                { id: 66, url: 'jpeg/6.webp', content: "ffff" },
                { id: 67, url: 'jpeg/1.jpeg', content: "gggg" },
                { id: 68, url: 'jpeg/2.webp', content: "hhhhh" },
                { id: 69, url: 'jpeg/3.webp', content: "ggggg" },
                { id: 70, url: 'jpeg/4.jpg', content: "aaaa" },
                { id: 71, url: 'jpeg/5.jpg', content: "hhhh" },
                { id: 72, url: 'jpeg/6.webp', content: "eeeee" },
                // Thêm các đối tượng hình ảnh khác nếu cần
            ],
            itemsPerPage: 15, // Số lượng bài viết trên mỗi trang
            currentPage: 1 // Trang hiện tại
        };
    },
    computed: {
        pageCount() {
            return Math.ceil(this.images.length / this.itemsPerPage);
        },
        paginatedPosts() {
            const startIndex = (this.currentPage - 1) * this.itemsPerPage;
            const endIndex = startIndex + this.itemsPerPage;
            return this.images.slice(startIndex, endIndex);
        }
    },
    methods: {
        changePage(pageNumber) {
            this.currentPage = pageNumber;
        }
    }
};
</script>

<style scoped>
.custom-image {
    max-width: 100%;
    width: 100%;
    height: 80%;
    border: 1px solid #fff;
    /* Điều chỉnh độ dày của viền */
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