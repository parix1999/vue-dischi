<template>
  <div id="app">
    <Loading  v-if="albums.length == 0"/>

    <Header @search="inputUtente"
    @cerca="filtro"/>

    <div class="container spazio-sotto">
      <!-- Dentro il main mandiamo i dati -->
      <Main :albums = "filteredAlbums"/>

    </div>

  </div>
</template>

<script>
import axios from 'axios'

import Header from './components/Header.vue';
import Main from './components/Main.vue';
import Loading from './components/Loading.vue';


export default {
  name: 'App',
  components: {
    Header,
    Main,
    Loading,
  },
  data: function(){
    return{
      // album sarà la array vuota dove lavorare i dati
      albums:[],
      filteredAlbums: [],
    }
  },
  created() {
    // Chiamata per ricevere i dati
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result)=>{
      this.albums = result.data.response;
      this.filteredAlbums = result.data.response;
    });
  },
  methods: {
    inputUtente(searchString) {
      alert(searchString)
    },
    filtro(choice) {
      this.filteredAlbums = this.albums.filter((element)=>{
        element.genre.includes(choice);
      });
    }


  }
}
</script>

<style lang="scss">
@import './style/app.scss';
  .spazio-sotto {
    padding: 50px 0;
  }
  


</style>
