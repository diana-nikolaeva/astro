<template>
  <div class="card-service">
    <div class="service">
      <div class="service-icon"><img src="../assets/icons/circleDots.svg" alt="service icon"></div>
      <div class="service-descr">30 экспертов онлайн, забронируйте консультацию</div>
    </div>
    <a href="/" class="btn">Попробовать бесплатно</a>
  </div>
</template>
<style scoped>
.card-service{
  background: #E23065;
  padding: 1rem;
  border-radius: 1rem;
  margin-top: 3rem;
  margin-bottom: 2.5rem;
  @media screen and (min-width:800px){
    margin-top: 4.5rem;
  }
}
.service{
  display: flex;
  margin-bottom: 1rem;

}
.service-icon{
  background: rgba(255, 255, 255, 0.10);
  padding: .9375rem;
  margin-right: .75rem;
  border-radius: 1.5625rem;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
