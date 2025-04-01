<script setup lang="ts">
document.addEventListener('DOMContentLoaded', function () {
  const container = document.querySelector('.carousel-container') as HTMLDivElement;
  const items = document.querySelectorAll('.carousel-item');
  const dots = document.querySelectorAll('.carousel-dot');
  const prevBtn = document.querySelector('.carousel-btn.prev');
  const nextBtn = document.querySelector('.carousel-btn.next');

  let currentIndex = 0;
  const itemCount = items.length;

  function updateCarousel() {
    container!.style.transform = `translateX(-${currentIndex * 100}%)`;

    // Обновляем активную точку
    dots.forEach((dot, index) => {
      dot.classList.toggle('active', index === currentIndex);
    });
  }

  // Переход к следующему элементу
  function nextSlide() {
    currentIndex = (currentIndex + 1) % itemCount;
    updateCarousel();
  }

  // Переход к предыдущему элементу
  function prevSlide() {
    currentIndex = (currentIndex - 1 + itemCount) % itemCount;
    updateCarousel();
  }

  // Клик по точкам навигации
  dots.forEach(dot => {
    dot.addEventListener('click', function () {
      currentIndex = parseInt(this.getAttribute('data-index'));
      updateCarousel();
    });
  });

  // Кнопки вперед/назад
  nextBtn.addEventListener('click', nextSlide);
  prevBtn.addEventListener('click', prevSlide);

  // Автоматическое перелистывание (опционально)
  // setInterval(nextSlide, 3000);
});
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

  <button class="carousel-btn prev">❮</button>
  <button class="carousel-btn next">❯</button>

  <div class="carousel-nav">
    <div class="carousel-dot active" data-index="0"></div>
    <div class="carousel-dot" data-index="1"></div>
    <div class="carousel-dot" data-index="2"></div>
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

/* carousel */

.carousel {
  position: relative;
  width: 100%;
  max-width: 600px;
  margin: 0 auto;
  overflow: hidden;
}

.carousel-container {
  display: flex;
  transition: transform 0.5s ease;
}

.carousel-item {
  min-width: 100%;
  box-sizing: border-box;
  padding: 20px;
  text-align: center;
  border: 1px solid #ddd;
}

.carousel-nav {
  display: flex;
  justify-content: center;
  margin-top: 10px;
}

.carousel-dot {
  width: 12px;
  height: 12px;
  margin: 0 5px;
  border-radius: 50%;
  background: #bbb;
  cursor: pointer;
}

.carousel-dot.active {
  background: #333;
}

.carousel-btn {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(0, 0, 0, 0.5);
  color: white;
  border: none;
  padding: 10px;
  cursor: pointer;
}

.carousel-btn.prev {
  left: 10px;
}

.carousel-btn.next {
  right: 10px;
}
</style>
