<template>
  <section class="about-us">
    <div class="container">
      <h2>О нас</h2>
      <div class="about-items first-row">
        <div class="about-item ">
          <div class="about-number">1800</div>
          <div class="number-descr">Консультаций в день</div>
        </div>
        <div class="about-item">
          <div class="about-number">2 млн</div>
          <div class="number-descr">Клиентов на сервисе</div>
        </div>
      </div>
      <div class="about-items second-row">
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
}
.about-items{
  display: flex;
}
.about-item:first-child{
  margin-right: .75rem;
}
.about-item{
  border-radius: 20px;
  border: 1px solid rgba(0, 16, 36, 0.10);
  background: #E23065;
  width: 50%;
  text-align: center;
  padding: 1rem;
  box-sizing: border-box;
}
.first-row{
  margin-bottom: .75rem;
}
.second-row{
  margin-bottom: 3rem;
}
.about-number{
  font-size: 1.25rem;
  font-weight: 600;
}
.number-descr{
  color:rgba(255, 255, 255, 0.70);
  font-size: .8125rem;
}
</style>
