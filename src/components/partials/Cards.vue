<script>
export default {
  name: 'Cards'

}
</script>

<template>
  <div class="container">
    <div class="card">
      <img src="https://images.ygoprodeck.com/images/cards/34541863.jpg" alt="">
      <h3>"A" Cell Breeding Device</h3>
      <p>Spell Card</p>
    </div>
    <div class="card">
      <img src="https://images.ygoprodeck.com/images/cards/34541863.jpg" alt="">
      <h3>"A" Cell Breeding Device</h3>
      <p>Spell Card</p>
    </div>
    <div class="card">
      <img src="https://images.ygoprodeck.com/images/cards/34541863.jpg" alt="">
      <h3>"A" Cell Breeding Device</h3>
      <p>Spell Card</p>
    </div>
    <div class="card">
      <img src="https://images.ygoprodeck.com/images/cards/34541863.jpg" alt="">
      <h3>"A" Cell Breeding Device</h3>
      <p>Spell Card</p>
    </div>
    <div class="card">
      <img src="https://images.ygoprodeck.com/images/cards/34541863.jpg" alt="">
      <h3>"A" Cell Breeding Device</h3>
      <p>Spell Card</p>
    </div>
    
    
    
  </div>
</template>

<style lang="scss" scoped>
@use '../../scss/partials/generals' as *;
@use '../../scss/partials/variables' as *;
.container{
  background-color: white;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  padding: 100px 50px 20px 50px;
}

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