<script>
import Cards from './partials/Cards.vue'
import { store } from '../data/store'
export default {
  name: 'Main',

  components:{
    Cards,
  },

  data(){
    return{
      store
    }
  }

}
</script>

<template>
  <main>
    <h3>SEARCH BAR</h3>

    <div class="container">
      <Cards 
      v-for="card in store.cardsList"
      :key="card.id"
      :card="card"
      />!
    </div>
    <br>
    <br>
    <br>
  </main>
</template>

<style lang="scss" scoped>
@use '../scss/partials/generals' as *;
@use '../scss/partials/variables' as *;

main{
  background-color: $bg-brown;
}
.container{
  background-color: white;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 100px 50px 20px 50px;
}

h3{
  height: 40px;
}


</style>