<template>
  <section class="our-couch">
    <div class="container">
      <h2>Наши тарологи</h2>
    </div>
    <div class="couch-item">
      <span class="status"><img src="../assets/icons/circle.svg" alt="circle icon">на линии</span>
      <img class="main-photo" src="../assets/images/avatar-three-m.png" alt="photo couch">
      <div class="couch-info">
        <div class="name">Вера Кант</div>
        <div class="specialty">Таролог, рунолог, астролог, нумеролог</div>
        <div class="tags">
          <div class="skill tag">
          <span><img src="../assets/icons/students.svg" alt="icon skill"></span>
          <span>18 лет опыта</span>
        </div>
        <div class="rate tag">
          <span><img src="../assets/icons/star.svg" alt="icon rate"></span>
          <span>5/5</span>
        </div>
        <div class="consultation tag">
          <span><img src="../assets/icons/chatCircle.svg" alt="icon-consultation"></span>
          <span>3104 консультаций</span>
        </div>
        </div>

      </div>
    </div>
    <div class="content">
      На Astro7 консультируют более 150 тарологов. Вы сможете выбрать любого и поговорить с ним.
    </div>
    <a href="/" class="btn pink">Попробовать бесплатно</a>
  </section>

</template>
<style scoped>
.our-couch {
  background: radial-gradient(116.56% 60.56% at 100% 0%, rgba(192, 37, 83, 0.40) 8.09%, rgba(192, 37, 83, 0.36) 21.09%, rgba(192, 37, 83, 0.00) 100%),
  #1E1E1E;
  padding: 2.5rem 0;
  position: relative;
  margin-bottom: 2.5rem;
}
.status{
  position: absolute;
  color: #0DC100;
  top:1.25rem;
  left: 1.25rem;
}
.status img{
  margin-right: 6px;
}
h2{
  font-size: 1.25rem;
  margin-bottom: 2rem;
  margin-bottom: .75rem;
  text-align: center;
}
.couch-item{
  position: relative;
  width: 19.25rem;
  margin: 0 auto;
  border-radius: 28px;
  overflow: hidden;
}
.main-photo{
  display: block;
  background: black;
}
.couch-info{
  position: absolute;
  bottom: 0;
  padding-bottom: 1.25rem;
  padding-left: 1rem;
  box-sizing: border-box;
  background: linear-gradient(180deg, rgba(0, 0, 0, 0.00) 0%, #000 100%);
}
.specialty{
  opacity: 0.8;
  margin: .75rem 0;
}
.tags{
  display: flex;
  flex-wrap: wrap;
}
.tag{
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
.content{
  margin: 2rem 2.625rem;
  text-align: center;
}
.btn{
  margin: 0 2rem 2.5rem ;
}
</style>
