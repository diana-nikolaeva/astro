<script setup lang="ts">
import mainBanner from './components/main-banner.vue';
import aboutUs from './components/about-us.vue';
import firstConsultation from './components/first-consultation.vue';
import ourCouch from './components/our-couch.vue';
import advantagesBlock from './components/advantages-block.vue';
import ourStory from './components/our-story.vue';
</script>

<template>
  <header>
    <mainBanner></mainBanner>
  </header>
  <main>
    <aboutUs></aboutUs>
    <firstConsultation></firstConsultation>
    <ourCouch></ourCouch>
    <advantagesBlock></advantagesBlock>
    <ourStory></ourStory>
  </main>
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
}
.btn.pink{
  background: #E23065;
  color:#fff;
}
</style>
