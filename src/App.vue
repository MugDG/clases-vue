<template>
  <div>
    <Navbar v-on:search-movie-title="searchMovie"></Navbar>
    <Content v-bind:movie-title="movieTitleToSearch"></Content>
  </div>
</template> 



<script>
import Navbar from "./components/Navbar.vue"
import Content from "./components/Content.vue"
export default {
  name: 'App',
  components: {
    Navbar,
    Content
  },
  data (){
    return {
      movieTitleToSearch:''
    }
  },
  methods:{
    searchMovie: function (title) {
      this.movieTitleToSearch = title
    }
  }
}
</script>


