<template>
  <div class="all">
    
    <Home class="section" id="home"></Home>
    <HowItWork class="section" id="howItWork"/>
    <PersonalPage class="section" id="personalPage"/>
    <HowWeWorks class="section" id="howWeWorks"/>
    <Questions class="section" id="questions"/>
    <Footer class="section" id="footer"/>
 
  </div>
</template>

<script>
const Home = () => import ('./components/Home.vue')
const Questions = () => import ('./components/Questions.vue')
const PersonalPage = () => import ('./components/PersonalPage.vue')
const HowWeWorks = () => import ('./components/HowWeWorks.vue')
const HowItWork = () => import ('./components/HowItWork.vue')
const Footer = () => import ('./components/Footer.vue')

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
    background-color: black;
  }
}

</style>
