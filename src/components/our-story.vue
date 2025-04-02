<script setup lang="ts">
import CardService from './card-service.vue';
import { Pagination as CarouselPagination } from 'vue3-carousel'
import { Navigation as CarouselNavigation } from 'vue3-carousel'
import { Carousel, Slide } from 'vue3-carousel';
import { stories } from '@/assets/data/story';
import storyItem from './story-item.vue';
import { computed } from 'vue';
const props = defineProps({ isPhone: Boolean });

const itemsToShow = computed(() => props.isPhone ? 1 : 2);
</script>
<template>
  <section class="our-story">
    <div class="container">
      <h2>Истории наших клиентов</h2>
      <div class="stories">
        <Carousel class="carousel-container" :items-to-show="itemsToShow" :gap="20">
      <Slide v-for="slide in stories" :key="slide.name">
        <storyItem :name="slide.name" :age="slide.age" :question="slide.question" :answer="slide.answer"></storyItem>
      </Slide>

      <template #addons>
        <CarouselPagination />
        <CarouselNavigation />
      </template>
    </Carousel>

      <CardService></CardService>
      </div>
    </div>
  </section>
</template>
<style scoped>
h2{
  color:black;
  margin-top: 80px;
  margin-bottom: 32px;
}
</style>
<style>
.our-story{
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
