<template>
  <v-container class="grey lighten-5 mt-12">
    <v-row no-gutters>
        <News class="ma-5"
        v-for="onenews in news"
        v-bind:news="onenews"
      />
    </v-row>
  </v-container>

</template>
  
<script> 
import News from '@/components/news/News.vue'
  export default {
    name: 'NewsPage',
    components:{
      News,
    },
    mounted(){
      this.getNews()
    },
    data:() => ({
        news:[]
    }),
    methods:{
      async getNews(){
        try{
          const response = await this.axios.get('https://newsapi.org/v2/top-headlines?country=us&apiKey=d7f41a32c26b4bbfb596d58b1a54c766')
          this.news = response.data.articles
          console.log(this.news);
        }
        catch(err){
         alert(err)
        }
      }
    }

  }
  </script>
  