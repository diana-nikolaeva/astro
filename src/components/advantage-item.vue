<script setup lang="ts">
defineProps(
  {
    icon: String,
    title:String,
    description:String
  }
);
</script>
<template>
      <div class="advantage-item">
        <div class="advantage-icon">
          <img :src="icon" alt="icon advantage">
        </div>
        <div class="title-advantage">{{title }}</div>
        <div class="descr-advantage">{{ description }}</div>
    </div>
</template>
<style scoped>
.advantage-item{
  padding: 24px 16px;
  border-radius: 20px;
  border: 1px solid rgba(0, 16, 36, 0.10);
}
.advantage-icon{
  width: 54px;
  height: 54px;
  border-radius: 41.481px;
  background: rgba(0, 16, 36, 0.04);
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto;
  margin-bottom: 1.125rem;
}
.title-advantage{
  color: black;
  text-align: center;
}
.descr-advantage{
  color:#A8ADB4;
  text-align: center;
}

</style>
