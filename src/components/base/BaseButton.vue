<template>
  <button>{{title}}</button>
</template>

<script>
export default {
  name: 'BaseButton',
  props:{
      title: {
          type: String,
          required: true,
          validator: value => {
              return !!value
          }
      }
  }
}
</script>

<style scoped lang="scss">
@import '../../css/variables.scss';
    button {
        padding: 15px 30px;
        text-transform: uppercase;
        font-weight: 600;
        background: $color-orange;
        border: none;
        border-radius: 8px;
        cursor: pointer;
        transition: .5s;
        white-space: nowrap;
    }
</style>
