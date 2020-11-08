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
    top: 8vh;
    right: 8vw;
    text-align: right;
    width: 40vw;
    h1{
      padding-bottom: 20px;
    }
    p{
      text-align: left;
    }
  }
  .main-img{
    position: absolute;
    width: 80vw;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
  }
  .button{
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    bottom: 5%;
  }
}
</style>
