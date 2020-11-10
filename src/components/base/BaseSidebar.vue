<template>
    <div class="right-nav">
        <div class="line"></div>
        
         <div 
            v-for="(menu, i) in menus" 
            :key="i" 
            @click="scrollTo(i)" 
            :class="{active: section == ++i}" 
            class="circle">
        </div>
     
    </div>
</template>

<script>
export default {
  name: 'BaseSidebar',
  data:() => {
      return{
          section: 1,
          menus: 6
      }
  },
  mounted(){
       window.addEventListener('scroll', () => {
           console.log(window.pageYOffset/window.innerHeight)
            let scroll = (window.pageYOffset/window.innerHeight) + 0.5
            scroll < 1 && (this.section = 1)
            scroll > 1 && scroll < 2 && (this.section = 2)
            scroll > 2 && scroll < 3 && (this.section = 3)
            scroll > 3 && scroll < 4 && (this.section = 4)
            scroll > 4 && scroll < 5 && (this.section = 5)
            scroll > 5 && (this.section = 6)
       })
  },
  methods: {
      scrollTo(i){
          this.$emit('scroll-to', i)
      }
  }

}
</script>

<style scoped lang="scss">
@import '../../css/variables.scss';
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
            transform: translateX(-1px);
            background: $color-white;
            z-index: 99;
        }
        .circle{
            width: 1.3vh;
            height: 1.3vh;
            // border: 1px solid $color-white;
            background: $color-white;
            border-radius: 50%;
            z-index: 999;
            transition: .5s;
            &:hover{
                transform: scale(1.2);
                cursor: pointer;
            }
        }
        .active{
            // border: 1px solid $color-orange;
            background: $color-orange;
        }
    }
</style>
