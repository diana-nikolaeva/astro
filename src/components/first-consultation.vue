<script setup lang="ts">

import reviewsBlock from './reviews-block.vue';
import { onMounted, onBeforeUnmount, ref } from 'vue'

const isPhone = ref(true)

if (typeof window !== 'undefined') {
  const onResize = () => {
    isPhone.value = window.innerWidth <= 1000
  }

  onMounted(() => window.addEventListener('resize', onResize))
  onBeforeUnmount(() => window.removeEventListener('resize', onResize))
  onResize()
}
</script>
<template>
  <section>
    <div class="container">
      <h2>Как проходит первая консультация</h2>
      <div class="steps-consultation">
        <div class="step">
          <div class="icon-step">
            <img src="../assets/icons/people-icon.svg" alt="people-icon">
          </div>
          <div class="step-content">
            <div class="title">Выберите эксперта</div>
            <div class="step-descr">С помощью фильтров или доверьтесь интуиции</div>
          </div>
        </div>
        <div class="step">
          <div class="icon-step">
            <img src="../assets/icons/check-icon.svg" alt="check-icon">
          </div>
          <div class="step-content">
            <div class="title">Забронируйте консультацию</div>
            <div class="step-descr">Выберите длительность и способ связи</div>
          </div>
        </div>
        <div class="step">
          <div class="icon-step">
            <img src="../assets/icons/phone-icon.svg" alt="phone-icon">
          </div>
          <div class="step-content">
            <div class="title">Дождитесь звонка</div>
            <div class="step-descr">Эксперт позвонит в течение 2х минут после оплаты</div>
          </div>
        </div>
      </div>
      <h2>С чем к нам обращаются</h2>
      <reviewsBlock :is-phone="isPhone"></reviewsBlock>
      <div class="content">Мы понимаем, что у каждого человека есть наболевшая проблема. Вы всегда можете обсудить ее с тарологом.</div>
      <a href="/" class="btn pink">Попробовать бесплатно</a>
      <div class="container-couch">
        <h2>Эксперты проходят строгий отбор</h2>
      <div class="step">
          <div class="icon-step">1</div>
          <div class="step-content">
            <div class="title">Тестирование</div>
            <div class="step-descr">Обязательное требование — практический опыт не менее 5 лет. Профессиональные способности проверяют независимые добровольцы</div>
          </div>
      </div>
      <div class="step">
          <div class="icon-step">2</div>
          <div class="step-content">
            <div class="title">Собеседование</div>
            <div class="step-descr">На собеседовании отслеживаем коммуникативные способности, уровень эмпатии, манеру и стиль беседы.</div>
          </div>
      </div>
      <div class="step">
          <div class="icon-step">3</div>
          <div class="step-content">
            <div class="title">Испытательный период</div>
            <div class="step-descr">Только 10% специалистов проходят отбор. В течение 3‍-‍х месяцев мы оцениваем навыки и собираем отзывы от клиентов</div>
          </div>
      </div>
      </div>
    </div>
  </section>
</template>
<style scoped>
h2{
  margin-bottom: 2rem;
  color:#131314;
  font-weight: 600;
}
.step{
  border-radius: 16px;
  border: 1px solid  rgba(0, 16, 36, 0.10);
  margin-bottom: .75rem;
  padding: 16px;
  display: flex;
  align-items: center;
}
.icon-step {
  background: rgba(0, 16, 36, 0.04);
  border-radius: 32px;
  padding: .9375rem;
  margin-right: 1rem;
  height: 3.375rem;
  color:#E23065;
  min-width: 3.375rem;
  box-sizing: border-box;
  text-align: center;
}
.title{
  color:#131314;
}
.step-descr{
  color:#A8ADB4;
}
.steps-consultation{
  margin-bottom: 3rem;
}
.content{
  margin: 4rem 0 2rem 0;
  color: #131314;
  font-size: 17px;
  text-align: center;
  @media screen and (min-width:1000px) {
    width: 60%;
    margin: 2rem auto;
  }
}
.pink{
  margin-bottom: 3rem;
}
.container-couch{
  margin-bottom: 40px;
}
</style>
