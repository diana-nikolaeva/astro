<template>
  <section class="about-us">
    <div class="container">
      <h2>О нас</h2>
        <div class="about-items">
          <div class="about-item ">
            <div class="about-number">1800</div>
            <div class="number-descr">Консультаций в день</div>
          </div>
          <div class="about-item">
            <div class="about-number">2 млн</div>
            <div class="number-descr">Клиентов на сервисе</div>
          </div>
          <div class="about-item">
            <div class="about-number">200</div>
            <div class="number-descr">Экспертов</div>
          </div>
          <div class="about-item ">
            <div class="about-number">100%</div>
            <div class="number-descr">Конфиденциальность</div>
          </div>
    </div>
    </div>
  </section>
</template>
<style scoped>
.about-us{
  padding-top: 2.5rem;
}
h2{
  font-size: 1.25rem;
  margin-bottom: 2rem;
  color:#131314;
  font-weight: 600;
  @media screen and (min-width:800px){
    font-size: 1.875rem;
  }
}
.about-items{
  display: flex;
  flex-wrap: wrap;
  margin-bottom: 3rem;
  @media screen and (min-width:800px){
    flex-wrap: nowrap;
  }
}
.about-item:first-child, .about-item:nth-child(2){
margin-bottom: .75rem;
@media screen and (min-width:800px){
  margin-bottom: 0;
}
}
.about-item:first-child,.about-item:nth-child(3){
  margin-right: .75rem;
}
.about-item{
  border-radius: 20px;
  border: 1px solid rgba(0, 16, 36, 0.10);
  background: #E23065;
  width: 47%;
  text-align: center;
  padding: 1rem;
  box-sizing: border-box;
  @media screen and (min-width:800px){
    margin-bottom: 0;
    margin-right: .875rem;
    &:last-child{
      margin-right: 0;
    }
  }
}
.first-row{
  margin-bottom: .75rem;
  @media screen and (min-width:800px){
    margin-bottom: 0;
  }
}
.second-row{
  margin-bottom: 3rem;
  @media screen and (min-width:800px){
    margin-bottom: 0;
  }

}
.about-number{
  font-size: 1.25rem;
  font-weight: 600;
}
.number-descr{
  color:rgba(255, 255, 255, 0.70);
  font-size: .8125rem;
}
@media screen and (min-width:800px) {
  .rows-container{
    display: flex;
    margin-bottom: 3rem;
  }
}
</style>
