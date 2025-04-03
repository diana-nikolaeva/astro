<template>
    <div class="card-service">
    <div class="service">
      <div class="service-icon"><img src="../assets/icons/circleDots.svg" alt="service icon"></div>
      <a href="/" class="btn decktop">Попробовать бесплатно</a>
      <div class="service-descr">30 экспертов онлайн, забронируйте консультацию</div>
    </div>
    <a href="/" class="btn mobile">Попробовать бесплатно</a>
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
    padding: 1.875rem;
  }
}
.service{
  display: flex;
  margin-bottom: 1rem;
  align-items: center;
  @media screen and (min-width:800px){
    flex-direction: row-reverse;
    font-size: 1.5rem;
    img{
      display: block;
      width: 40px;
    }
  }

}
.service-descr{
  @media screen and (min-width:800px){
    max-width: 250px;
  }
  @media screen and (min-width:950px){
    max-width: 350px;
  }
}
.service-icon{
  background: rgba(255, 255, 255, 0.10);
  padding: .9375rem;
  margin-right: .75rem;
  border-radius: 1.5625rem;
  display: flex;
  align-items: center;
  justify-content: center;
  @media screen and (min-width:800px){
    width: 90px;
    height: 90px;
    border-radius: 45px;

  }
}
.decktop{
  display: none;
  @media screen and (min-width:800px){
    display: block;
    width: 19.375rem;
    font-size: 1.0625rem;
    color:#E23065;
  }
}
.btn.mobile{
    @media screen and (min-width:800px){
    display: none;
    }
  }
  .service{
    @media screen and (min-width:800px){
    margin-bottom: 0;
    }
  }
</style>
