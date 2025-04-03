<script setup lang="ts">
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide } from 'vue3-carousel';
import { Pagination as CarouselPagination } from 'vue3-carousel'
import { reviews } from '@/assets/data/reviews';
import reviewItem from './review-item.vue';
defineProps({ isPhone: Boolean });

</script>
<template>
  <div class="carousel">
    <div class="carousel-container reviews-carousel">
      <Carousel v-if="isPhone" class="carousel-container" >
      <Slide v-for="slide in reviews" :key="slide.name">
        <reviewItem :img="slide.img" :name="slide.name" :age="slide.age" :review="slide.review"
          :avatarCouch="slide.avatarCouch" :nameCouch="slide.nameCouch" :spetiality="slide.spetiality">
        </reviewItem>
      </Slide>
      <template #addons>
        <CarouselPagination />
      </template>
    </Carousel>
    <reviewItem v-else v-for="item in reviews" :key="item.name" :img="item.img" :name="item.name" :age="item.age" :review="item.review"
    :avatarCouch="item.avatarCouch" :nameCouch="item.nameCouch" :spetiality="item.spetiality"></reviewItem>
    </div>
  </div>
</template>
<style scoped>
.carousel-container{
  @media screen and (min-width:800px) {
    display: flex;
    justify-content: center;
  }
}
</style>
<style>
.reviews-carousel{
  margin: 0 auto;
  .carousel__pagination{
    bottom: -32px;
  }
  .carousel__pagination-button{
    width: .5rem;
    height: .5rem;
    background-color: rgba(0, 0, 0, 0.20);
    margin-right: .75rem;
    border-radius: 5px;
  }
  .carousel__pagination-button--active{
    width: 32px;
    border-radius: 5px;
    background-color:#E23065;
  }
}
</style>
