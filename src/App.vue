<template>
  <div class="all">
    
    <Home id="home"/>
 
  </div>
</template>

<script>
import Home from './components/Home.vue'

export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
}
#home{
  height: 100vh;
  width: 100vw;
  background-image: url(./assets/home.svg);
}
</style>
