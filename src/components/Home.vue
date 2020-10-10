<template>
  <div class="home">
    <h1>Успей защитить свои важные моменты от времени</h1>
  </div>
</template>

<script>
export default {
  name: 'Home',
  props: {
    msg: String
  }
}
</script>

<style scoped lang="scss">
.home{
  display: flex;
  justify-content: center;
  align-items: center;
  h1{
    font-size: 40px;
    font-family: 'Courier New', Courier, monospace;
    color: white;
  }
}
</style>
