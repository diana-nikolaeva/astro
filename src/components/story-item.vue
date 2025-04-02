<script setup lang="ts">
defineProps(
  {
    name: String,
    age:String,
    question:String,
    answer:String
  }
);
</script>
<template>
  <div class="store-item">
          <div class="question">
            <div class="author-story">
            <div class="photo">
              <img src="../assets/images/avatar-reviews.jpg" alt="photo-author">
            </div>
            <div class="data-author">
              <div class="name">{{name}}</div>
              <div class="age">{{age}} лет</div>
            </div>
            </div>
            <div class="story-content">{{question}}</div>
          </div>

          <div class="answer">
          <h3>Отзыв клиента</h3>
          <div class="answer-text">{{answer}}</div>
          <a class="also" href="/">еще</a>
        </div>
      </div>
</template>
<style scoped>
.store-item {
  border-radius: 1.25rem;
  border: 1px solid #E5E7E9;
  max-width: 470px;
  max-height: 500px;
  overflow: hidden;
  display: flex;
  flex-direction: column;
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
.answer-text{
  overflow: hidden;
  color:#131314
}
.story-content{
  color: #131314;
}
.answer{
  padding: 1.5rem 1.25rem;
  background: #F5F6F6;
  overflow: hidden;
  display: flex;
  flex-direction: column;
}
.also{
  position: absolute;
  bottom: 1.5625rem;
  right: 1.3125rem;
  background: linear-gradient(89deg, rgba(245, 246, 246, 0.00) 0.49%, #F5F6F6 26.04%);
  color:#E23065;
  width: 6.25rem;
  text-align: right;
}
h3{
  color:#E23065;
  font-size: .9375rem;
  font-weight: 600;
  margin-bottom: 1rem;
}
</style>

