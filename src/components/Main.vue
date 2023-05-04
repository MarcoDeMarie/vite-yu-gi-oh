<script>
import Cards from './partials/Cards.vue'
export default {
  name: 'Main',

  components:{
    Cards,
  }

}
</script>

<template>
  <main>
    <h3>SEARCH BAR</h3>
    
      <Cards />
      
  </main>
</template>

<style lang="scss" scoped>
@use '../scss/partials/generals' as *;
@use '../scss/partials/variables' as *;

main{
  background-color: $bg-brown;
  height: 100vh;
  width: 100vw;
}
h3{
  height: 40px;
}


</style>