<template>
  <div class="home">
    <div class="header">
      <img src="../assets/logo.svg" alt="">
      <ul class="menu">
        <li>как это работает?</li>
        <li>о нас</li>
        <li>контакты</li>
        <li>стать партнером</li>
      </ul>
    </div>
    <div class="center">
      <h1>Успей защитить свои важные моменты от времени</h1>
      <base-button class="button" :title="'Стать участником клуба'"></base-button>
    </div>
    

  <base-sidebar :section="1"></base-sidebar>
  </div>
</template>

<script>
export default {
  name: 'Home',
}
</script>

<style scoped lang="scss">
@import '../css/variables.scss';
.home{
  .header{
    display: flex;
    justify-content: space-between;
    padding: 45px 100px;
    img{

    }
    .menu{
      display: flex;
      align-items: center;
      li{
        text-transform: uppercase;
        font-size: 12px;
        padding-left: 30px;
        line-height: 15px;
        list-style-type: none; 
        color: $color-grey;
        transition: .5s;
        &:hover{
          color: $color-orange;
          cursor: pointer;
        }
      }
    }
  }
  .center{
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    h1{
      max-width: 34vw;
      font-weight: 600;
      text-transform: uppercase;
      font-size: 22px;
      line-height: 35px;
      letter-spacing: 5px;
      color: white;
      text-align: center;
      margin-bottom: 60px;
    }
    .button{
      margin-left: 50%;
      transform: translateX(-50%);
      &:hover{
        transform: translateX(-50%) scale(1.05);
      }
    }
  }
}
</style>
