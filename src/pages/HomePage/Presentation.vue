<template>
  <section class="presentation">
    <div class="presentation__wrapper">
      <div class="presentation__main-block">
        <p class="presentation__subtitle">Whales Design</p>
        <h1 class="presentation__title">
          Мы помогаем зарабатывать в интернете
        </h1>
        <Button textButton="Обсудить проект" />
      </div>
      <ul class="presentation__carousel">
        <li class="presentation__li-item">
          <p class="presentation__li-item-num">01.</p>
          <p class="presentation__li-item-title">Графический дизайн</p>
        </li>
      </ul>
    </div>
    <img src="../../images/load-carousel.svg" alt="" />
  </section>
</template>

<script>
import Button from "../../components/Button.vue";
export default {
  name: "Presentation",
  components: {
    Button,
  },
};
</script>

<style scoped>
.presentation {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.presentation__wrapper {
  display: flex;
  width: 100%;
  justify-content: space-between;
  align-items: center;
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

.presentation__carousel {
  list-style-type: none;
  display: flex;
  margin: 0;
  padding: 0;
  max-width: 534px;
  width: 100%;
  min-height: 443px;
}

.presentation__li-item {
  background-size: contain;
  background-repeat: no-repeat;
  background-position: right center;
  background-image: url("../../images/present-img.png");
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.presentation__li-item-num {
  margin: 0;
  font-style: normal;
  font-weight: 300;
  font-size: 30px;
  line-height: 145%;
  letter-spacing: 0.02em;
}

.presentation__li-item-title {
  margin: 0;
  font-weight: bold;
  font-size: 45px;
  line-height: 145%;
  letter-spacing: 0.02em;
}
</style>
