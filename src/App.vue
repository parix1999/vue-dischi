<template>
  <div id="app">
    <Header />
    <div class="container spazio-sotto">
      <!-- Dentro il main mandiamo i dati -->
      <Main :albums = "albums"/>

    </div>

  </div>
</template>

<script>
import axios from 'axios'

import Header from './components/Header.vue';
import Main from './components/Main.vue';


export default {
  name: 'App',
  components: {
    Header,
    Main,
  },
  data: function(){
    return{
      // album sarà la array vuota dove lavorare i dati
      albums:[],
    }
  },
  created() {
    // Chiamata per ricevere i dati
    axios.get('https://flynn.boolean.careers/exercises/api/array/music').then((result)=>{
      this.albums = result.data.response;
    });
  }
}
</script>

<style lang="scss">
@import './style/app.scss';
  .spazio-sotto {
    padding: 50px 0;
  }
  


</style>
