<script setup lang="ts">
defineProps(
  {
    img: String,
    name: String,
    speciality: String,
    skill: String,
    star: String,
    count: String
  }
);
</script>

<template>
  <div class="couch-item">
    <span class="status"><img src="../assets/icons/circle.svg" alt="circle icon">на линии</span>
    <img class="main-photo" :src="img" alt="photo couch">
    <div class="couch-info">
      <div class="name">{{ name }}</div>
      <div class="specialty">{{ speciality }}</div>
      <div class="tags">
        <div class="skill tag">
          <span><img src="../assets/icons/students.svg" alt="icon skill"></span>
          <span>{{ skill }}</span>
        </div>
        <div class="rate tag">
          <span><img src="../assets/icons/star.svg" alt="icon rate"></span>
          <span>{{ star }}</span>
        </div>
        <div class="consultation tag">
          <span><img src="../assets/icons/chatCircle.svg" alt="icon-consultation"></span>
          <span>{{ count }}</span>
        </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.couch-item {
  position: relative;
  width: 19.25rem;
  margin: 0 auto;
  border-radius: 28px;
  overflow: hidden;
}

.status {
  position: absolute;
  color: #0DC100;
  top: 1.25rem;
  left: 1.25rem;
}
.main-photo {
  display: block;
  background: black;
}

.couch-info {
  position: absolute;
  bottom: 0;
  padding-bottom: 1.25rem;
  padding-left: 1rem;
  box-sizing: border-box;
  background: linear-gradient(180deg, rgba(0, 0, 0, 0.00) 0%, #000 100%);
}

.specialty {
  opacity: 0.8;
  margin: .75rem 0;
}

.tags {
  display: flex;
  flex-wrap: wrap;
}

.tag {
  background: #29292B;
  padding: 0 .625rem;
  border-radius: 1.875rem;
  display: flex;
  align-items: center;
  width: max-content;
  flex-direction: row;
  margin-right: .5rem;
  margin-bottom: .5rem;
}
</style>
