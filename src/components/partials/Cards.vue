<script>
export default {
  name: 'Cards',
  props:{
    card: Object

  }

}
</script>

<template>
  <div class="card">
    <img :src="card.card_images[0].image_url" :alt="card.name">
    <h3>{{ card.name }}</h3>
    <p>{{ card.type }}</p>
  </div>
</template>

<style lang="scss" scoped>
@use '../../scss/partials/generals' as *;
@use '../../scss/partials/variables' as *;


.card{
  margin-bottom: 10px;
  height: 350px;
  width: 170px;
  background-color: $bg-brown;
  text-align: center;

  h3{
    color: white;
  }
  
  img{
    height: 250px;
  }
  p{
    padding: 10px;
  }
}


</style>