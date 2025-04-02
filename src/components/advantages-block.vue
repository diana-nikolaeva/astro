<script setup lang="ts">
import advantageItem from './advantage-item.vue';
import { advantages } from '@/assets/data/advantage';
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide } from 'vue3-carousel';
import AdvantageItem from './advantage-item.vue';
import { Pagination as CarouselPagination } from 'vue3-carousel'
defineProps({ isPhone: Boolean });
</script>
<template>
  <section class="advantages">
    <div class="container">
      <h2>Ощутите преимущества консультаций с тарологами Astro7</h2>
      <Carousel v-if="isPhone">
        <Slide v-for="slide in advantages" :key="slide.title">
          <AdvantageItem :icon="slide.icon" :title="slide.title" :description="slide.description"></AdvantageItem>
        </Slide>
        <template #addons>
        <CarouselPagination />
      </template>
      </Carousel>

      <div class="carousel carousel-advantage" v-else>
        <advantageItem :icon="item.icon" :title="item.title" :description="item.description" class="advantage-block"
          v-for="item in advantages" :key="item.title"></advantageItem>
      </div>
    </div>
  </section>
</template>
<style scoped>
.carousel-advantage {
  margin: 2rem 0;
}

h2 {
  color: black
}

.carousel-advantage {
  display: grid;
  grid-template-columns: auto auto;
  grid-gap: 1.25rem;
}

.advantage-block {
  height: 100%;
}
</style>
<style>
.advantages{
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
