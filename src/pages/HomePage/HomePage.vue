<template>
  <div>
    <Header />
    <main class="content">
      <section class="presentation">
        <div class="presentation__main-block">
          <p class="presentation__subtitle">Whales Design</p>
          <h1 class="presentation__title">
            Мы помогаем зарабатывать в интернете
          </h1>
          <Button textButton="Обсудить проект" />
        </div>
        <ul class="carousel">
          <li class="li-item">
            <p class="li-item-num">01.</p>
            <p class="li-item-title">Графический дизайн</p>
          </li>
        </ul>
      </section>
      <section class="about">
        <p>О нас</p>
        <p>
          Мы онлайн дизайн студия, которая, помогает нашим клиентам по всему
          миру получать осмысленный дизайн, создавая, значимые связи между
          людьми и брендами!
        </p>
        <p>
          Выполняем проекты для ведущих веб-студий по всему миру в качестве
          субподрядчиков. Ключевой состав команды работает с момента основания
          компании. Мы гарантируем индивидуальный подход к каждому новому
          веб-сайту, логотипу, и/или фирменному стилю.
        </p>
      </section>
      <section class="completed-projects"></section>
      <section class="briefs"></section>
      <section class="clients"></section>
      <section class="request"></section>
    </main>
    <footer></footer>
  </div>
</template>

<script>
import Button from "../../components/Button.vue";
import Header from "../../components/Header.vue";
export default {
  components: {
    Button,
    Header,
  },
  name: "HomePage",
};
</script>

<style scoped>
@import url("../../fonts/fonts.css");

.content {
  padding-top: 34px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.presentation {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 980px;
  min-height: 443px;
  /* border: 1px solid black; */
}

.presentation__main-block {
  max-width: 261px;
}

.presentation__subtitle {
  margin: 0 0 13px 0;
  font-weight: 300;
  font-size: 13px;
  line-height: 145%;
  letter-spacing: 0.05em;
  color: #1c1d28;
}

.presentation__title {
  margin: 0 0 41px 0;
  font-weight: 500;
  font-size: 30px;
  line-height: 145%;
  letter-spacing: 0.02em;
  color: #1c1d28;
}

.carousel {
  list-style-type: none;
  display: flex;
  margin: 0;
  padding: 0;
  max-width: 534px;
  width: 100%;
  min-height: 443px;
}

.li-item {
  background-size: contain;
  background-repeat: no-repeat;
  background-position: right center;
  background-image: url("../../images/present-img.png");
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.li-item-num {
  margin: 0;
  font-style: normal;
  font-weight: 300;
  font-size: 30px;
  line-height: 145%;
  letter-spacing: 0.02em;
}

.li-item-title {
  margin: 0;
  font-weight: bold;
  font-size: 45px;
  line-height: 145%;
  letter-spacing: 0.02em;
}

.item-span {
}
</style>
