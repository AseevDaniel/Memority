<template>
    <div class="header">
        <img src="../../assets/logo.svg" alt="">
        <ul class="menu">
            <li @click="$emit('scroll-to', 1)">как это работает?</li>
            <li @click="$emit('scroll-to', 2)">о нас</li>
            <li @click="$emit('scroll-to', 3)">контакты</li>
            <li @click="$emit('scroll-to', 4)">стать партнером</li>
        </ul>
    </div>
</template>

<script>
export default {
  name: 'BaseNavigation',
}
</script>

<style scoped lang="scss">
@import '../../css/variables.scss';
  .header{
    display: flex;
    justify-content: space-between;
    padding: 30px 100px;
    width: calc(100vw - 2 * 100px);
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
</style>
