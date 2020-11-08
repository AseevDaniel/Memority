<template>
  <div class="footer">
    <div class="top">
      <h1>Не опоздай!</h1>
      <h1>Успей защитить свои важные моменты от времени</h1>
      <base-button 
        class="button" 
        :title="'Задать вопрос'"/>
    </div>

    <img class="sideimg" src="../assets/footer/footer.svg" alt="">

    <base-navigation 
      @scroll-to="$emit('scroll-to', $event)"
      class="bot"/>

  <base-sidebar 
    @scroll-to="$emit('scroll-to', $event)" 
    class="button" 
    :section="6"/>
  </div>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style scoped lang="scss">
@import '../css/variables.scss';
.footer{
  position: relative;
  display: flex;
  justify-content: flex-start;
  align-items: center;
  .top{
    max-width: 500px;
    margin-left: 100px;
    transform: translateY(-50px);
    h1{
      color: $color-white;
    }
    .button{
      margin-top: 50px;
      &:hover{
        transform: scale(1.05);
      }
    }
  }
  .sideimg{
    position: absolute;
    right: 0;
    top: 50%;
    transform: translateY(-55%);
    max-height: 80vh;
  }
  .bot{
    position: absolute;
    bottom: 0;
    left: 0;
    background: black;
  }
  
}
</style>
