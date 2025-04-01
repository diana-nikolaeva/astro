<template>
  <div class="container banner-container">
    <div class="banner-column first-column">
      <div class="logo-container">
        <div class="logo">
          <img src="../assets/icons/logo.svg" alt="logo company">
        </div>
        <div class="logo-descr">Сервис эзотерических консультаций № 1 в России с 2009 г.</div>
      </div>
      <h1>Консультации с тарологом по телефону или в чате</h1>
      <h2>Получите прогноз по вашей ситуации бесплатно</h2>
      <a href="/" class="btn">Попробовать бесплатно</a>
    </div>
    <div class="banner-column second-column">
      <img src="../assets/images/main-banner.png" alt="">
    </div>
  </div>
</template>
<style scoped>
.banner-container {
  background:radial-gradient(116.56% 60.56% at 100% 0%, rgba(192, 37, 83, 0.40) 8.09%, rgba(192, 37, 83, 0.36) 21.09%, rgba(192, 37, 83, 0.00) 100%),
  #1E1E1E
}

.logo-container {
  padding-top: .5rem;
  display: flex;
  margin-bottom: 3.75rem;
}
.logo{
  margin-right: 2rem;
  display: flex;
  align-items: center;
}
.logo img{
  height: 2rem;
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
}

h2 {
  font-size: .9375rem;
  font-weight: 400;
  line-height: 135%;
  letter-spacing: -0.0187rem;
  opacity: 0.6;
  margin-bottom: 2rem;
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
</style>
