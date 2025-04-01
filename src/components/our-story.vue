<script setup>
import CardService from './card-service.vue';
</script>
<template>
  <section class="our-story">
    <div class="container">
      <div class="stories">
        <div class="store-item">
          <div class="question">
            <div class="author-story">
            <div class="photo">
              <img src="../assets/images/avatar-reviews.jpg" alt="photo-author">
            </div>
            <div class="data-author">
              <div class="name">Олеся</div>
              <div class="age">38 лет</div>
            </div>
            </div>
            <div class="story-content">
              Я решила разводиться с мужем, нет сил и желания терпеть отношения. Муж меня не уважает, ни в чем не помогает, я тащу все на себе. Не понимаю сути отношений, если в них, я взваливаю двойную ношу проблем и отвечаю теперь за нас двоих. Слабо верю что люди меняются. Есть ли шанс сделать эти отношения другими?
            </div>
          </div>

          <div class="answer">
          <h3>Отзыв клиента</h3>
          <div class="answer-text">В очень трудной жизненной ситуации жизнь свела меня с Нонной. Несколько раз я обращалась за консультацией к этому эксперту. Видела мучительную для меня ситуацию не так, как мне говорила Нонна, я даже сомневалась сначала в ее словах. Но поверила и послушала ее совета! Я хотела подавать на развод, но Нонна все объяснила, как она видит, что необходимо сделать, что нас с мужем ждет в будущем. Я ей настолько поверила, что сделала так как она мне советовала. И результат! Моя семья не распалась, а наоборот сейчас, как заново рождена. Муж говорит мне «Спасибо тебе за мудрость, что не сделала ужасный для нашей семьи шаг.» А я говорю Нонне – от всего сердца примите мою благодарность, уважение за Ваш труд!</div>
          <a class="also" href="/">еще</a>
        </div>
      </div>
      <CardService></CardService>
      </div>
    </div>
  </section>
</template>
<style scoped>
.store-item {
  border-radius: 1.25rem;
  border: 1px solid #E5E7E9;
}
.question{
  padding: 1.5rem 1.25rem;
}
.author-story{
  display: flex;
}
.photo {
  width: 3.375rem;
  height: 3.375rem;
  border-radius: 40px;
  margin-right: .75rem;
  margin-bottom: 1rem;
  overflow: hidden;
}
.name{
  color:#131314;
}
.age{
  color:#A8ADB4;
}
h3{
  color:#E23065;
  font-size: .9375rem;
  font-weight: 600;
  margin-bottom: 16px;
}
.answer-text{
  height: 7.5rem;
  overflow: hidden;
  color:#131314
}
.story-content{
  color: #131314;
}
.answer{
  padding: 1.5rem 1.25rem;
  background: #F5F6F6;
  position: relative;
}
.also{
  position: absolute;
  bottom: 1.5rem;
  right: 1rem;
  background: linear-gradient(89deg, rgba(245, 246, 246, 0.00) 0.49%, #F5F6F6 26.04%);
  color:#E23065;
  width: 6.25rem;
  text-align: right;
}
</style>
