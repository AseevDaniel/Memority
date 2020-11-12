<template>
  <div class="questions">
    <h1>Часто задаваемые вопросы</h1>
    <div class="content">
      <div class="item"
        v-for="(item, index) in questions"
        :key="index">
        <div class="circle">+</div>
        <p>{{item}}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Questions',
  data(){
    return{
      questions: [
        'ЧТО ТАКОЕ ЦИФРОВОЕ НАСЛЕДИЕ?',
        'ЧТО ТАКОЕ ЦИФРОВОЕ НАСЛЕДИЕ?',
        'ЧТО ТАКОЕ ИНТЕРАКТИВНЫЙ МЕМОРИАЛ?',
        'ЧТО ТАКОЕ ИНТЕРАКТИВНЫЙ МЕМОРИАЛ?',
        'ПОЧЕМУ ВАЖНО СОЗДАТЬ ИНТЕРАКТИВНЫЙ МЕМОРИАЛ?' ,
        'ПОЧЕМУ ВАЖНО СОЗДАТЬ ИНТЕРАКТИВНЫЙ МЕМОРИАЛ?' ,
        'ГДЕ МОЖНО ПОСМОТРЕТЬ ВАШИ ВЫПОЛНЕННЫЕ ПРОЕКТЫ?',
        'ГДЕ МОЖНО ПОСМОТРЕТЬ ВАШИ ВЫПОЛНЕННЫЕ ПРОЕКТЫ?',
        'КАК Я МОГУ СОЗДАТЬ МЕМОРИАЛ?',
        'КАК Я МОГУ СОЗДАТЬ МЕМОРИАЛ?',
        'СКОЛЬКО СТОИТ ИНТЕРАКТИВНЫЙ МЕМОРИАЛ?',
        'СКОЛЬКО СТОИТ ИНТЕРАКТИВНЫЙ МЕМОРИАЛ?',
        'КАК ДОБАВИТЬ ЕЩЕ ОДНУ МЕМОРИАЛЬНУЮ СТРАНИЦУ?',
        'КАК ДОБАВИТЬ ЕЩЕ ОДНУ МЕМОРИАЛЬНУЮ СТРАНИЦУ?',
        'КАК ПОЛУЧИТЬ ПРОМО-КОД НА СКИДКУ?',
        'КАК ПОЛУЧИТЬ ПРОМО-КОД НА СКИДКУ?',
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import '../css/variables.scss';
.questions{
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  h1{
    margin-top: 65px;
  }
  .content{
    margin-top: 65px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-auto-rows: 60px;
    grid-column-gap: 80px;
    padding: 0 60px;
    .item{
      display: flex;
      .circle{
        height: 28px;
        width: 28px;
        background: #20232D;
        border-radius: 50%;
        box-shadow: -4px -4px 4px rgba(255, 255, 255, 0.05), 4px 4px 4px rgba(0, 0, 0, 0.25);
        color: $color-orange;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 24px;
        font-weight: 300;
        margin-right: 25px;
        transition: .25s;
        &:hover{
          cursor: pointer;
          transform: scale(1.2);
        }
      }
      p{
        font-size: 12px;
      }
    }
  }
}
</style>
