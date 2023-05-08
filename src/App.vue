<script>

import axios from 'axios'
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import { store } from './data/store' 

export default {
  name: 'App',
  components:{
    Header,
    Main,
  },

  data() {
    return {
      store
    }
  },
  
  methods:{
    getApi(){
      axios.get(store.apiUrl, {
        params: {
          name: store.cardSearch
        }
      })
        .then(result => {
          store.cardsList = result.data.data
          console.log(store.cardsList);
        })
    }
  },
  mounted(){
    this.getApi();
  }

}
</script>

<template>
  <Header />

  <Main @startSearch="getApi"/>
  
</template>

<style lang="scss">

</style>