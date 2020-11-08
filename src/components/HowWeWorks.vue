<template>
  <div class="howWeWorks">
    <div class="top">
      <div class="text">
        <h1>Как мы работаем?</h1>
        <p>Небанальное визуальное повествование — 
          краеугольный камень, на котором зиждутся 
          сегодня ведущие интернет-сообщества. </p>
      </div>
      <iframe class="video"
          src="https://www.youtube.com/embed/ktvTqknDobU">
      </iframe>
    </div>
    <div class="bot">
      <div
        class="card"
        v-for="(item, index) in items"
        :key="index"
        >
      <img :src="require(`../assets/howweworks/${item.src}`)" alt="">
      <p>{{item.text}}</p>
      </div>
    </div>

  <base-sidebar class="button" :section="4"></base-sidebar>
  </div>
</template>

<script>
export default {
  name: 'HowWeWorks',
  data(){
    return{
      items:[
        {
          src: 'item.svg',
          text: 'Небанальное визуальное ' + 
          'повествование — краеугольный камень,' +  
          'на котором зиждутся сегодня ведущие интернет-сообщества.'
        },
        {
          src:  'item.svg',
          text: 'Небанальное визуальное ' + 
          'повествование — краеугольный камень,'
        },
        {
          src:  'item.svg',
          text: 'Небанальное визуальное повествование'
        },
        {
          src:  'item.svg',
          text: 'Небанальное визуальное ' + 
          'повествование — краеугольный камень,' +  
          'на котором зиждутся сегодня ведущие интернет-сообщества.'
        },
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../css/variables.scss';
.howWeWorks{
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  .top{
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    padding: 0 125px;
    padding-top: 7vh;
    .text{
      width: 35%;
      h1{
        padding-bottom: 40px;
      }
    }
    .video{
      width: 500px;
      height: 250px;
    }
  }
  .bot{
    display: flex;
    justify-content: center;
    align-items: flex-start;
    margin-top: 40px;
    .card{
      padding: 20px;
      display: flex;
      flex-direction: column;
      align-items: center;
      img{
        width: 25vh;
      }
      p{
        margin-top: 15px;
        text-align: center;
        max-width: 240px;
        font-size: 12px;
      }
    }
  }
  
}
</style>
