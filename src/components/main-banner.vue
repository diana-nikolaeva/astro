<template>
  <div class="banner-container">
    <div class="container main-banner">
      <div class="logo-container">
        <div class="logo">
          <img src="../assets/icons/logo.svg" alt="logo company">
        </div>
        <div class="logo-descr">Сервис эзотерических консультаций № 1 в России с 2009 г.</div>
      </div>
      <div class="banner-columnns">
        <div class="banner-column first-column">
          <h1>Консультации с тарологом по телефону или в чате</h1>
          <h2>Получите прогноз по вашей ситуации бесплатно</h2>
          <a href="/" class="btn">Попробовать бесплатно</a>
          </div>
          <div class="banner-column second-column">
          <img src="../assets/images/main-banner.png" alt="">
          </div>
      </div>
    </div>
  </div>
</template>
<style scoped>
.banner-container {
  background:radial-gradient(116.56% 60.56% at 100% 0%, rgba(192, 37, 83, 0.40) 8.09%, rgba(192, 37, 83, 0.36) 21.09%, rgba(192, 37, 83, 0.00) 100%),
  #1E1E1E
}
.main-banner{
  @media screen and (min-width:800px){
    padding: 0 7.5rem;
  }

}
.banner-columnns{
  @media screen and (min-width:800px){
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    position: relative;
  }
}
.banner-column{
  @media screen and (min-width:800px){
    width: 50%;
    padding-bottom: 5.625rem;

  }
}
.second-column{
  @media screen and (min-width:800px) {
    position: absolute;
    bottom: -97px;
    right: -70px;
  }
}

.logo-container {
  padding-top: .5rem;
  display: flex;
  margin-bottom: 3.75rem;
  align-items: center;
  @media  screen and (min-width:800px) {
    padding-top: 1.875rem;
    margin-bottom: 6.25rem;
  }
}
.logo{
  margin-right: 2rem;
  display: flex;
  align-items: center;
  max-width: 5rem;
  @media  screen and (min-width:800px){
    max-width: 8.125rem;
  }
}
.logo img{
  height: 2rem;
  width:100%;
}
.logo-descr{
  font-size: .8125rem;
}

h1 {
  font-size: 1.875rem;
  font-weight: 600;
  line-height: 100%;
  letter-spacing: -0.0563rem;
  margin-bottom: 1.5rem;
  @media  screen and (min-width:800px){
    font-size: 3.125rem;
  }
}

h2 {
  font-size: .9375rem;
  font-weight: 400;
  line-height: 135%;
  letter-spacing: -0.0187rem;
  opacity: 0.6;
  margin-bottom: 2rem;
  @media  screen and (min-width:800px){
    font-size: 1.0625rem;
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
  margin-bottom: 1.25rem;
  cursor: pointer;
  display: block;
  text-decoration: none;
}
.banner-column img{
  width: 100%;

}
@media screen and (min-width:800px){
  .first-column{
    margin-right: 90px;
  }
}

</style>
