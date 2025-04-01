<template>
  <section class="sale">
    <div class="container">
      <h2>Таролог ответит на один ваш вопрос бесплатно</h2>
      <div class="steps">
        <div class="step">
          <div class="icon-step">1</div>
          <div class="step-content">
            <div class="step-descr">Длительность бесплатной консультации 5‍-‍7 минут, после её окончания вы сможете продлить консультацию.</div>
          </div>
        </div>
        <div class="step">
          <div class="icon-step">2</div>
          <div class="step-content">
            <div class="step-descr">Вам позвонит оператор службы поддержки, чтобы подобрать эксперта и удобное время для консультации. Если не дозвонится, напишет вам в WhatsApp.</div>
          </div>
        </div>
        <div class="step">
          <div class="icon-step">3</div>
          <div class="step-content">
            <div class="step-descr">На электронную почту отправим письмо с доступом в личный кабинет.</div>
          </div>
        </div>
        <div class="step">
          <div class="icon-step">4</div>
          <div class="step-content">
            <div class="step-descr">Предложение актуально только для телефонной консультации.</div>
          </div>
        </div>
      </div>
      <a href="/" class="btn pink">Попробовать бесплатно</a>
    </div>
  </section>
</template>
<style scoped>
h2{
  margin-bottom: 1.5rem;
}
.sale{
  background:radial-gradient(116.56% 60.56% at 100% 0%, rgba(192, 37, 83, 0.40) 8.09%, rgba(192, 37, 83, 0.36) 21.09%, rgba(192, 37, 83, 0.00) 100%),
  #1E1E1E;
  padding-top: 2.5rem;
  padding-bottom: 2.5rem;
}
.step{
  margin-bottom: 1rem;
  padding: 16px;
  display: flex;
  align-items: center;
  border-radius: 20px;
  border: 1px solid rgba(255, 255, 255, 0.10);
}
.icon-step{
  background: rgba(255, 255, 255, 0.04);
  border-radius: 32px;
  padding: .9375rem;
  margin-right: 1rem;
  height: 3.375rem;
  color:#E23065;
  min-width: 3.375rem;
  box-sizing: border-box;
  text-align: center;
}
.step-descr{
  color:#A8ADB4;
  font-size: .9375rem;
}
</style>
