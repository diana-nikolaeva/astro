<script setup lang="ts">
</script>
<template>
  <div class="carousel">
    <div class="carousel-container">
      <div class="carousel-item review-item">
        <div class="container-review">
          <div class="author-review author">
            <div class="photo">
              <img src="../assets/images/avatar-reviews.jpg" alt="photo-author">
            </div>
            <div class="data-author">
              <div class="name">Олеся</div>
              <div class="age">38 лет</div>
            </div>
          </div>
          <div class="text-review">
            «Ребенок в этом году заканчивает 9 класс и ужасно переживает из-за ОГЭ. Особенно сложно даётся математика.
            Мы конечно волнуемся и стараемся поддержать. Вопрос: сдаст ли сын экзамены?»
          </div>
        </div>
        <div class="answer">
          <h3>Ответ эксперта</h3>
          <div class="author-answer">
            <div class="container-answer">
              <div class="photo">
                <img src="../assets/images/avatar-tarolog.jpg" alt="photo-answer">
              </div>
              <div class="data-author author-answer">
                <div class="name">Лора Нейман</div>
                <div class="age">Таролог, рунолог. Успешно практикует 5 лет</div>
              </div>
            </div>
            <audio controls src="../assets/audio/audio.mp3"></audio>
          </div>
        </div>
      </div>
      <div class="carousel-item review-item">
        <div class="container-review">
          <div class="author-review author">
            <div class="photo">
              <img src="../assets/images/avatar-reviews.jpg" alt="photo-author">
            </div>
            <div class="data-author">
              <div class="name">Олеся</div>
              <div class="age">38 лет</div>
            </div>
          </div>
          <div class="text-review">
            «Ребенок в этом году заканчивает 9 класс и ужасно переживает из-за ОГЭ. Особенно сложно даётся математика.
            Мы конечно волнуемся и стараемся поддержать. Вопрос: сдаст ли сын экзамены?»
          </div>
        </div>
        <div class="answer">
          <h3>Ответ эксперта</h3>
          <div class="author-answer">
            <div class="container-answer">
              <div class="photo">
                <img src="../assets/images/avatar-tarolog.jpg" alt="photo-answer">
              </div>
              <div class="data-author author-answer">
                <div class="name">Лора Нейман</div>
                <div class="age">Таролог, рунолог. Успешно практикует 5 лет</div>
              </div>
            </div>
            <audio controls src="../assets/audio/audio.mp3"></audio>
          </div>
        </div>
      </div>
      <div class="carousel-item review-item">
        <div class="container-review">
          <div class="author-review author">
            <div class="photo">
              <img src="../assets/images/avatar-reviews.jpg" alt="photo-author">
            </div>
            <div class="data-author">
              <div class="name">Олеся</div>
              <div class="age">38 лет</div>
            </div>
          </div>
          <div class="text-review">
            «Ребенок в этом году заканчивает 9 класс и ужасно переживает из-за ОГЭ. Особенно сложно даётся математика.
            Мы конечно волнуемся и стараемся поддержать. Вопрос: сдаст ли сын экзамены?»
          </div>
        </div>
        <div class="answer">
          <h3>Ответ эксперта</h3>
          <div class="author-answer">
            <div class="container-answer">
              <div class="photo">
                <img src="../assets/images/avatar-tarolog.jpg" alt="photo-answer">
              </div>
              <div class="data-author author-answer">
                <div class="name">Лора Нейман</div>
                <div class="age">Таролог, рунолог. Успешно практикует 5 лет</div>
              </div>
            </div>
            <audio controls src="../assets/audio/audio.mp3"></audio>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.review-item {
  border-radius: 1.25rem;
  border: 1px solid #E5E7E9;
}

.container-review {
  padding: 1.5rem 1.25rem;
}

.author {
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

.data-author .name {
  color: #131314;
}

.data-author .age {
  color: #A8ADB4;
}

.photo img {
  display: block;
  width: 100%;
}

.text-review {
  font-size: .9375rem;
  color: #131314;
}

.container-answer {
  display: flex;
}

.answer {
  background: #F5F6F6;
  padding: 1.5rem 1.25rem;
}

h3 {
  color: #E23065;
  font-size: .9375rem;
  margin-bottom: 1rem;
  font-weight: 600;
}

.author-answer {
  margin-bottom: 1rem;
}

audio {
  width: 100%;
  height: 64px;
}

audio::-webkit-media-controls-panel {
  background: #fff;
  border-radius: 1rem;
  overflow: hidden;

}

audio::-webkit-media-controls-play-button {
  background: #E23065;
  border-radius: 25px;
  width: 36px;
  height: 36px;
}

audio::-webkit-media-controls-current-time-display,
audio::-webkit-media-controls-time-remaining-display,
audio::-webkit-media-controls-mute-button {
  display: none;
}
.carousel-container{
  @media screen and (min-width:800px) {
    display: flex;
  }
}
.carousel-item{
  overflow: hidden;
  @media screen and (min-width:800px){
    margin-right: 20px;
    &:last-child{
      margin-right: 0;
    }
  }
}

</style>
