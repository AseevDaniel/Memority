<template>
  <div class="all">
    
    <Home 
      @scroll-to="scrollTo" 
      class="section" 
      id="home"/>
      
    <HowItWork 
      @scroll-to="scrollTo" 
      class="section" 
      id="howItWork"/>

    <PersonalPage 
      @scroll-to="scrollTo" 
      class="section" 
      id="personalPage"/>

    <HowWeWorks 
      @scroll-to="scrollTo" 
      class="section" 
      id="howWeWorks"/>

    <Questions 
      @scroll-to="scrollTo" 
      class="section" 
      id="questions"/>

    <Footer 
      @scroll-to="scrollTo" 
      class="section" 
      id="footer"/>
 
    <base-sidebar 
      @scroll-to="scrollTo" 
      class="button" 
      :section="6"/>
  </div>
</template>

<script>
export default {
  name: 'App',
  components: {
    Home: () => import ('./components/TheHome.vue'),
    Questions: () => import ('./components/TheQuestions.vue'),
    PersonalPage: () => import ('./components/ThePersonalPage.vue'),
    HowWeWorks: () => import ('./components/TheHowWeWorks.vue'),
    HowItWork: () => import ('./components/TheHowItWork.vue'),
    Footer: () => import ('./components/TheFooter.vue')
  },
  methods: {
    scrollTo(i){
      window.scrollTo({
          top: window.innerHeight * i,
          behavior: 'smooth'
      });
    }
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
  // .button{
  //   position: fixed;
  // }
}

</style>
