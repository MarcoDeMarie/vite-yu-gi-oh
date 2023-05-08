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
    <div class="reserch">
      <input v-model.trim="store.cardSearch" type="text" placeholder="Cerca una carta">
      <button @click="$emit('startSearch')" >Cerca</button>
      <button @click="store.cardSearch=null; $emit('startSearch')">Reset</button>
    </div>

    <div class="container">
      <Cards 
      v-for="card in store.cardsList"
      :key="card.id"
      :card="card"
      />
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
  padding: 20px 50px 20px 50px;
}

h3{
  height: 40px;
}

.reserch{
  display: flex;
  justify-content: center;
  padding: 15px 0 15px 0;
  input{
    height: 30px;
    width: 200px;
    margin-right: 10px;
  }
}


</style>