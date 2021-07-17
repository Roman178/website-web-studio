<template>
  <header class="header">
    <img src="../images/logo.svg" alt="logo" />
    <ul class="header__list">
      <li>Портфолио</li>
      <li>Услуги и цены</li>
      <li>Мы</li>
      <li>Контакты</li>
    </ul>
    <p class="header__phone">+38 (097) 757 51 51</p>
    <Button textButton="Обсудить проект" />
  </header>
</template>

<script>
import Button from "../components/Button.vue";
export default {
  components: { Button },
  name: "Header",
};
</script>

<style scoped>
.header {
  max-width: 1100px;
  width: 100%;
  min-height: 65px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}
.header__list {
  margin: 0;
  min-width: 410px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  list-style-type: none;
  font-weight: 500;
  font-size: 13px;
  line-height: 16px;
}

.header__phone {
  margin: 0;
  font-weight: bold;
  font-size: 13px;
  line-height: 16px;
  letter-spacing: 0.02em;
}
</style>
