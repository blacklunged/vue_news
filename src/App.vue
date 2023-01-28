<template>
  <v-app>
    <Navbar/>
    <NewsPage/> 
  </v-app>
</template>

<script>
import Navbar from "@/components/Navbar.vue"
import NewsPage from "@/components/news/NewsPage.vue"
export default {
  name: 'App',
  components:{
    Navbar, NewsPage
  }

};
</script>
