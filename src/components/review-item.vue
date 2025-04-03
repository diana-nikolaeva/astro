<script lang="ts" setup>
defineProps(
  {
    img: String,
    name: String,
    age:String,
    review:String,
    avatarCouch: String,
    nameCouch:String,
    spetiality:String
  }
);

</script>
<template>
  <div class="carousel-item review-item">
        <div class="container-review">
          <div class="author-review author">
            <div class="photo">
              <img :src="img" alt="photo-author">
            </div>
            <div class="data-author">
              <div class="name">{{name}}</div>
              <div class="age">{{ age }} лет</div>
            </div>
          </div>
          <div class="text-review">{{review}}</div>
        </div>
        <div class="answer">
          <h3>Ответ эксперта</h3>
          <div class="author-answer">
            <div class="container-answer">
              <div class="photo">
                <img :src="avatarCouch" alt="photo-answer">
              </div>
              <div class="data-author author-answer">
                <div class="name">{{nameCouch}}</div>
                <div class="age">{{spetiality}}</div>
              </div>
            </div>
            <audio controls >
              <source src="../assets/audio/audio.mp3" type="audio/mpeg">
            </audio>
          </div>
        </div>
      </div>
</template>
<style scoped>
.review-item {
  border-radius: 1.25rem;
  border: 1px solid #E5E7E9;
  max-width: 470px;
  @media screen and (min-width:1000px) {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
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


audio::-webkit-media-controls-current-time-display,
audio::-webkit-media-controls-time-remaining-display,
audio::-webkit-media-controls-mute-button {
  display: none;
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
