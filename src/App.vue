<template>
  <div class="all">
    
    <div class="right-nav">
      <div class="line"></div>
      <div class="circle active"></div>
      <div class="circle"></div>
      <div class="circle"></div>
      <div class="circle"></div>
      <div class="circle"></div>
      <div class="circle"></div>
    </div>
    <Home class="section" id="home"></Home>
    <HowItWork class="section" id="howItWork"/>
    <PersonalPage class="section" id="personalPage"/>
    <HowWeWorks class="section" id="howWeWorks"/>
    <Questions class="section" id="questions"/>
    <Footer class="section" id="footer"/>
 
  </div>
</template>

<script>
// const Home = () => import ('./components/Home.vue')
// const Questions = () => import ('./components/Questions.vue')
// const PersonalPage = () => import ('./components/PersonalPage.vue')
// const HowWeWorks = () => import ('./components/HowWeWorks.vue')
// const HowItWork = () => import ('./components/HowItWork.vue')
// const Footer = () => import ('./components/Footer.vue')

import Home from './components/Home.vue'
import Questions from './components/Questions.vue'
import PersonalPage from './components/PersonalPage.vue'
import HowWeWorks from './components/HowWeWorks.vue'
import HowItWork from './components/HowItWork.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Home,
    Questions,
    PersonalPage,
    HowWeWorks,
    HowItWork,
    Footer
  }
}
</script>

<style lang="scss">
@import './css/variables.scss';
*{
  margin: 0;
  outline: none;
  font-family: 'Montserrat', sans-serif;
}
.all{
  .right-nav{
    position: fixed;
    top: 50%;
    right: 64px;
    transform: translateY(-50%);
    height: 20vh;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    z-index: 9999;
    .line{
      position: absolute;
      left: 50%;
      height: 20vh;
      width: 1px;
      background: $color-white;
      z-index: 99;
    }
    .circle{
      width: 1vh;
      height: 1vh;
      // border: 1px solid $color-white;
      background: $color-white;
      border-radius: 50%;
      z-index: 999;
    }
    .active{
      // border: 1px solid $color-orange;
      background: $color-orange;
    }
    
  }
  #home{
    background-image: url(./assets/home.svg);
  }
  #howItWork{
    background-image: url(./assets/howItWork.svg);
  }
  #personalPage{
    background-image: url(./assets/personalPage.svg);
  }
  #howWeWorks{
   background-image: url(./assets/howWeWorks.svg);
  }
  #questions{
    background-image: url(./assets/questions.svg);
  }
  #footer{
    // background-image: url(./assets/footer.svg);
  }
  .section{
    height: 100vh;
    width: 100vw;
    background-size: cover;
    
  }
}

</style>
