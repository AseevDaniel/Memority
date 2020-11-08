<template>
    <div class="right-nav">
      <div class="line"></div>
      <div :class="{active: section == 1}" class="circle"></div>
      <div :class="{active: section == 2}" class="circle"></div>
      <div :class="{active: section == 3}" class="circle"></div>
      <div :class="{active: section == 4}" class="circle"></div>
      <div :class="{active: section == 5}" class="circle"></div>
      <div :class="{active: section == 6}" class="circle"></div>
    </div>
</template>

<script>
export default {
  name: 'BaseSidebar',
  props:{
      section: {
          type: Number,
          required: true,
          validator: value => {
              return !!value
          }
      }
  },

}
</script>

<style scoped lang="scss">
@import '../../css/variables.scss';
    .right-nav{
        position: absolute;
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
