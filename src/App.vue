<script setup lang="ts">
import mainBanner from './components/main-banner.vue';
import aboutUs from './components/about-us.vue';
import firstConsultation from './components/first-consultation.vue';
import ourCouch from './components/our-couch.vue';
import advantagesBlock from './components/advantages-block.vue';
import ourStory from './components/our-story.vue';
import saleBlock from './components/sale-block.vue';
import footerBlock from './components/footer-block.vue';
import { onMounted, onBeforeUnmount, ref } from 'vue'

const isPhone = ref(true)

if (typeof window !== 'undefined') {
  const onResize = () => {
    isPhone.value = window.innerWidth <= 1000
  }

  onMounted(() => window.addEventListener('resize', onResize))
  onBeforeUnmount(() => window.removeEventListener('resize', onResize))
  onResize()
}

</script>

<template>
  <header>
    <mainBanner></mainBanner>
  </header>
  <main>
    <aboutUs></aboutUs>
    <firstConsultation></firstConsultation>
    <ourCouch :is-phone="isPhone"></ourCouch>
    <advantagesBlock :is-phone="isPhone"></advantagesBlock>
    <ourStory :is-phone="isPhone"></ourStory>
    <saleBlock></saleBlock>
  </main>
  <footer>
    <footerBlock></footerBlock>
  </footer>
</template>

<style>
@font-face {
  font-family: Inter;
  src: url(./assets/fonts/Inter-Regular.otf);
}

* {
  font-family: Inter;
  color: #fff;
}

.container {
  padding: 0 1rem;
  max-width: 90rem;
  margin: 0 auto;

  @media screen and (min-width:800px) {
    padding: 0 3rem;
  }

  @media screen and (min-width:1440px) {
    padding: 0 15rem;
  }
}

.btn {
  background: #fff;
  border-radius: 16px;
  padding: 16px;
  font-size: 17px;
  font-weight: 500;
  letter-spacing: -0.34px;
  color: #1E1E1E;
  text-align: center;
  cursor: pointer;
  display: block;
  text-decoration: none;

  @media screen and (min-width:800px) {
    max-width: 19.375rem;
    margin: 0 auto;
  }
}

.btn.pink {
  background: #E23065;
  color: #fff;
}
</style>
