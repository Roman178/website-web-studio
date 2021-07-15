<template>
  <div>
    <header class="header">
      <img src="../../images/logo.svg" alt="logo" />
      <ul class="list">
        <li>Портфолио</li>
        <li>Услуги и цены</li>
        <li>Мы</li>
        <li>Контакты</li>
      </ul>
      <p class="phone">+38 (097) 757 51 51</p>
      <Button textButton="Обсудить проект" />
    </header>
    <main class="content">
      <section class="presentation">
        <div>
          <p>Whales Design</p>
          <h2>Мы помогаем зарабатывать в интернете</h2>
          <Button textButton="Обсудить проект" />
        </div>
      </section>
      <section class="about"></section>
      <section class="completed-projects"></section>
      <section class="briefs"></section>
      <section class="clients"></section>
      <section class="request"></section>
    </main>
    <footer>Done</footer>
  </div>
</template>

<script>
import Button from "../../components/Button.vue";
export default {
  components: {
    Button,
  },
  name: "HomePage",
};
</script>

<style scoped>
@import url("../../fonts/fonts.css");
.header {
  margin: auto;
  max-width: 1100px;
  min-height: 65px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-family: "Montserrat";
}
.list {
  min-width: 410px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  list-style-type: none;
  font-weight: 500;
  font-size: 13px;
  line-height: 16px;
}
.content {
  min-height: 200vh;
  padding-top: 34px;
}

.phone {
  font-weight: bold;
  font-size: 13px;
  line-height: 16px;
  letter-spacing: 0.02em;
}

.presentation {
  max-width: 980px;
  min-height: 443px;
  border: 1px solid black;
}
</style>
