<template>
    <div class="wrapper">
       <Header></Header>
       <br/>
       <nuxt></nuxt>
       <br/>
       <Footer></Footer>
    </div>
</template>

<script>
    import Header from "~/components/header.vue"
    import Footer from "~/components/footer.vue"
    
    export default {
        comments:{
            Header,
            Footer,
            
        }
    }
</script>

