<template>
  <div id="app">
    <MyHeader @search='getFilms'/>
    <MyMain :films="films"/>
  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyMain from './components/MyMain.vue'

const axios = require('axios');

export default {
  name: 'App',
  components: {
    MyHeader,
    MyMain
  },
  
  data(){
    return{
      films: [],
    }
  },

  methods: {
    getFilms(keyword){
      //uso un iterpolazione per richiedere tramite la keyword i films
      axios.get('https://api.themoviedb.org/3/search/movie/?api_key=35d5e8ab27efec855252b6c0fe9dbdfb&query=' + keyword + '&language=it-IT')
        .then((response) => {
          this.films = response.data.results;

        })
        .catch(function (error) {
          // handle error
          console.log(error);
        })
        .then(function () {
          // always executed
        });
     }
  }

}
</script>

<style lang="scss">


@import './assets/style/generals.scss'

</style>
