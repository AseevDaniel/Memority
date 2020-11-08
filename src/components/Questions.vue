<template>
  <div class="questions">
    <h1>Успей защитить свои важные моменты от времени</h1>

  <base-sidebar class="button" :section="5"></base-sidebar>
  </div>
</template>

<script>
export default {
  name: 'Questions',
}
</script>

<style scoped lang="scss">
@import '../css/variables.scss';
.questions{
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  h1{
    font-size: 40px;
    color: red;
  }
}
</style>
