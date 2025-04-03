<script setup lang="ts">
import CardService from './card-service.vue';
import { Pagination as CarouselPagination } from 'vue3-carousel'
import { Carousel, Slide } from 'vue3-carousel';
import { stories } from '@/assets/data/story';
import storyItem from './story-item.vue';
import { computed, ref } from 'vue';
const props = defineProps({ isPhone: Boolean });

const itemsToShow = computed(() => props.isPhone ? 1 : 2);
const carouselRef = ref();
const nextIsBlock = computed(() => carouselRef.value?.currentSlide === carouselRef.value?.maxSlide);
const prevIsBlock = computed(() => carouselRef.value?.currentSlide === carouselRef.value?.minSlide);

const next = () => carouselRef.value.next();
const prev = () => carouselRef.value.prev();

</script>
<template>
  <section class="our-story">
    <div class="container">
      <h2>Истории наших клиентов</h2>
      <div class="stories">
        <Carousel class="carousel-container" :items-to-show="itemsToShow" :itemsToScroll="2" :gap="20"
          ref="carouselRef">
          <Slide v-for="slide in stories" :key="slide.name">
            <storyItem :name="slide.name" :age="slide.age" :question="slide.question" :answer="slide.answer">
            </storyItem>
          </Slide>

          <template #addons>
            <CarouselPagination />
            <div class="navigation-wrapper">
              <button class="btn-carousel btn-prev" :class="{ disabled: prevIsBlock }" @click="prev">
                &lt; </button>
              <button class="btn-carousel btn-next" :class="{ disabled: nextIsBlock }" @click="next"> &gt;</button>
            </div>

          </template>
        </Carousel>

        <CardService></CardService>
      </div>
    </div>
  </section>
</template>
<style scoped>
h2 {
  color: black;
  margin-top: 80px;
  margin-bottom: 32px;
  font-weight: 600;
}
</style>
<style>
.our-story {
  .carousel__pagination {
    bottom: -32px;
  }

  .carousel__pagination-button {
    width: .5rem;
    height: .5rem;
    background-color: rgba(0, 0, 0, 0.20);
    margin-right: .75rem;
    border-radius: 5px;
  }

  .carousel__pagination-button--active {
    width: 32px;
    border-radius: 5px;
    background-color: #E23065;
  }

  .navigation-wrapper {
    position: absolute;
    height: 30px;
    top: -67px;
    right: 0;
    width: 120px;
    display: none;

    @media screen and (min-width:1000px) {
      display: block;
    }

    .btn-carousel {
      border: 1px solid #131314;
      border-radius: 2.5rem;
      width: 2.875rem;
      height: 2.875rem;
      background: #fff;
      color: black
    }

    .btn-prev {
      margin-right: 1.25rem;
    }

    .disabled {
      border: 1px solid rgba(19, 19, 20, 0.20);
      color: rgba(19, 19, 20, 0.20);
    }
  }
}
</style>
