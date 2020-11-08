<template>
  <div class="howItWork">

      <div class="top">
        <div class="content">
          <h1>Как это работает?</h1>
          <p>Небанальное визуальное повествование — краеугольный камень, 
            на котором зиждутся сегодня ведущие интернет-сообщества. 
            Креативные способы подачи материала, такие, к примеру, 
            как добавление живого текста и анимационных эффектов, 
            являются отличным способом привнести самобытность в ваши 
            статьи, «истории», а также фото- и видеопубликации в соцсетях.
          </p>
        </div>
        <img src="../assets/howitwork/1.svg" alt="">
      </div>

      <div class="carousel">
        <h1 class="gallery">Галерея</h1>
        <carousel-3d  
          class="slider"
          :controls-visible="true"
          :controls-prev-html="'&#10092; '" 
          :controls-next-html="'&#10093;'" 
          :controls-width="30" 
          :controls-height="60" 
          :space="(width/6) + 100">
          <slide v-for="(slide, i) in slides" :index="i" :key="i">
            <figure>
              <img :src="require(`../assets/slider/slider${sliderMethod(i)}.svg`)">
            </figure>
          </slide>
        </carousel-3d>
      </div>
  <base-sidebar class="button" :section="2"></base-sidebar>
  </div>
</template>

<script>
import { Carousel3d, Slide} from 'vue-carousel-3d'
export default {
  name: 'HowItWork',
  components: {
    Carousel3d, 
    Slide
  },
  data(){
    return{
      slides: 6,
      width: 0
    }
  },
  methods: {
    sliderMethod(i){
      i++
      if(i > 3) return i - 3
      else return i
    }
  },
  mounted(){
    this.width = document.documentElement.clientWidth
    console.log(this.width)
  }

}
</script>

<style scoped lang="scss">
@import '../css/variables.scss';
.howItWork{
  // display: flex;
  // flex-direction: column;
  // justify-content: center;
  // align-items: center;
  max-width: 100vw;
  position: relative;
  h1{
    color: $color-orange;
  }
  .top{
    display: flex;
    justify-content: space-between;
    height: 50%;
    margin: 0 auto;
    width: 80vw;

    .content{
      width: 45%;
      h1{
        margin-top: 12vh;
        margin-bottom: 6vh;
      }
      p{
        color: $color-white;
      }
    }
    // padding: 0 100px;
    img{
      align-self: flex-end;
      transform: translate(-4vw, 6vh) ;
      // scale(1.1)
    }
  }
  .carousel{
    display: flex;
    height: 50%;
    width: 100%;
  }
  .gallery{
    position: absolute;
    left: 9vw;
    bottom: 330px;
    
  }
  .slider{
    align-self: flex-end;
    img{
      cursor: pointer;
    }
  }
}
</style>
