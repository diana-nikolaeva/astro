<script setup lang="ts">
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide } from 'vue3-carousel';
import cardCouch from './card-couch.vue';
import { couches } from '../assets/data/couches.ts';
import { Pagination as CarouselPagination } from 'vue3-carousel'
import { Navigation as CarouselNavigation } from 'vue3-carousel'
import { computed } from 'vue';
const props = defineProps({ isPhone: Boolean });

const itemsToShow = computed(() => props.isPhone ? 1 : 3);
</script>
<template>
  <section class="our-couch">
    <div class="container">
      <h2>Наши тарологи</h2>
    </div>

    <Carousel class="carousel-container" :items-to-show="itemsToShow">
      <Slide v-for="slide in couches" :key="slide.name">
        <cardCouch :count="slide.count" :img="slide.img" :name="slide.name" :skill="slide.skill"
          :speciality="slide.speciality" :star="slide.star"></cardCouch>
      </Slide>

      <template #addons>
        <div class="navigation-wrapper">
          <CarouselNavigation />
        </div>
        <CarouselPagination />
      </template>
    </Carousel>


    <div class="content">
      На Astro7 консультируют более 150 тарологов. Вы сможете выбрать любого и поговорить с ним.
    </div>
    <a href="/" class="btn pink">Попробовать бесплатно</a>

  </section>

</template>
<style scoped>
.our-couch {
  background: radial-gradient(116.56% 60.56% at 100% 0%, rgba(192, 37, 83, 0.40) 8.09%, rgba(192, 37, 83, 0.36) 21.09%, rgba(192, 37, 83, 0.00) 100%),
    #1E1E1E;
  padding: 2.5rem 0;
  position: relative;
  margin-bottom: 2.5rem;

  @media screen and (min-width:1000px) {
    margin-bottom: 5rem;
  }
}

.carousel-container {
  max-width: 960px;
  margin: 0 auto;
}


.status img {
  margin-right: 6px;
}

h2 {
  font-size: 1.25rem;
  margin-bottom: 2rem;
  margin-bottom: .75rem;
  text-align: center;

  @media screen and (min-width:1000px) {
    text-align: left;
    margin-bottom: 2rem;
  }
}

.content {
  margin: 4rem 2.625rem;
  text-align: center;
}

.btn {
  margin: 0 2rem 2.5rem;

  @media screen and (min-width:800px) {
    margin: 0 auto;
  }
}

.carousel__pagination {
  bottom: -2rem;
}

.navigation-wrapper {
  position: absolute;
  height: 30px;
  top: -67px;
  right: 8px;
  width: 92px;
  display: none;
  @media screen and (min-width:1000px) {
    display: block;
    }
}
</style>

<style>
.our-couch {
  .carousel__pagination-button {
    background-color: rgba(255, 255, 255, 0.20);
    width: .5rem;
    height: .5rem;
    margin-right: .75rem;
    border-radius: .625rem;
  }

  .carousel__pagination-button--active {
    background-color: #fff !important;
    width: 2rem;
  }

  .carousel__prev {
    border: 1px solid #fff;
    border-radius: 20px;

  }

  .carousel__next {
    border: 1px solid #fff;
    border-radius: 20px;
  }

}
</style>
