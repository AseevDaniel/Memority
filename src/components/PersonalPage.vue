<template>
  <div class="personalPage">
   <div class="top">
      <h1>персональная страница</h1>
      <p>Небанальное визуальное повествование — 
        краеугольный камень, на котором зиждутся 
        сегодня ведущие интернет-сообщества.</p>
   </div>
   <img src="../assets/personalpage/personalPage.svg" alt="" class="main-img">

   <base-button class="button" :title="'Просмотреть свою страницу'"></base-button>

  <base-sidebar :section="3"></base-sidebar>
  </div>
</template>

<script>
export default {
  name: 'PersonalPage',
}
</script>

<style scoped lang="scss">
@import '../css/variables.scss';
.personalPage{
  // display: flex;
  // justify-content: center;
  // align-items: center;
  position: relative;
  .top{
    position: absolute;
    top: 10vh;
    right: 8vw;
    text-align: right;
    width: 35vw;
    h1{
      color: $color-orange;
      padding-bottom: 25px;
    }
    p{
      text-align: left;
      color: $color-white;
    }
  }
  .main-img{
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -55%);
  }
  .button{
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    bottom: 10%;
  }
}
</style>
