<template>
    <v-card
    class="mx-auto"
    max-width="344"
  >
    <v-img
      :src="news.urlToImage"
      height="200px"
    ></v-img>

    <v-card-title>
        <NavLink :href="news.url">
            {{news.title}}
        </NavLink>
    </v-card-title>

    <v-card-subtitle>
      {{news.content}}
    </v-card-subtitle>

    <v-card-actions>
        <a :href="news.url">
            <v-btn
        color="orange lighten-2"
      >
        Explore
      </v-btn>
        </a>


      <v-spacer></v-spacer>

    </v-card-actions>

   
  </v-card>
</template>
  
<script>

export default {
    name: 'News',
    props:{
        news:{
            type:Object,
        }
    }
}
</script>
  