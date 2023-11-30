<template>
    <div>
      <button v-for="pageNumber in pageCount" :key="pageNumber" @click="changePage(pageNumber)" :class="{ active: currentPage === pageNumber }">
        {{ pageNumber }}
      </button>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      currentPage: {
        type: Number,
        required: true
      },
      pageCount: {
        type: Number,
        required: true
      }
    },
    methods: {
      changePage(pageNumber) {
        this.$emit('pageChange', pageNumber);
      }
    }
  };
  </script>
  
  <style scoped>
  button {
    margin: 5px;
    padding: 5px 10px;
    cursor: pointer;
    border: 1px solid #ddd;
    background-color: #f8f8f8;
  }
  
  button.active {
    background-color: #4CAF50;
    color: white;
  }
  </style>
  