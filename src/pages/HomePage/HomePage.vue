<template>
  <div class="page">
    <Header />
    <main class="content">
      <div class="conten__wrapper">
        <section class="presentation">
          <div class="presentation__wrapper">
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
          </div>
          <img src="../../images/load-carousel.svg" alt="" />
        </section>
        <section class="about">
          <h3 class="about__title">О нас</h3>
          <p class="about__main-paragraph">
            Мы онлайн дизайн студия, которая, помогает нашим клиентам по всему
            миру получать осмысленный дизайн, создавая, значимые связи между
            людьми и брендами!
          </p>
          <p class="about__subparagraph">
            Выполняем проекты для ведущих веб-студий по всему миру в качестве
            субподрядчиков. Ключевой состав команды работает с момента основания
            компании. Мы гарантируем индивидуальный подход к каждому новому
            веб-сайту, логотипу, и/или фирменному стилю.
          </p>
        </section>
      </div>
      <section class="completed-projects">
        <div class="completed-projects__wrapper">
          <h3 class="completed-projects__title">Наши работы</h3>

          <div class="tabs-component">
            <ul class="tabs-component-tabs">
              <li
                v-for="(isTabActive, numberOfTab) in selectedTab"
                :key="numberOfTab"
                @click="selectTab(numberOfTab)"
                :class="{ 'is-active': isTabActive }"
                class="tabs-component-tab"
              >
                <a class="tabs-component-tab-a">{{ numberOfTab }} </a>
              </li>
              <li class="tabs-component-tab">
                Все работы <span class="tabs-component__arrow">&#129042;</span>
              </li>
            </ul>
            <div class="tabs-component-panels">
              <section class="tabs-component-panel"></section>
            </div>
          </div>
        </div>
      </section>
      <section class="briefs"></section>
      <section class="clients"></section>
      <section class="request"></section>
    </main>
    <footer></footer>
  </div>
</template>

<script>
import "./tabs.css";
import Button from "../../components/Button.vue";
import Header from "../../components/Header.vue";

export default {
  data() {
    return {
      selectedTab: {
        ["Логотипы"]: true,
        ["Веб-сайты"]: false,
        ["Фирменный стиль"]: false,
        ["Иллюстрации"]: false,
      },
    };
  },

  methods: {
    selectTab(tabToSelect) {
      for (let key in this.selectedTab) {
        if (key === tabToSelect) {
          this.selectedTab[key] = true;
        } else {
          this.selectedTab[key] = false;
        }
      }
    },

    tabTestTwo(selectedTab) {
      console.log(selectedTab);
    },
  },
  components: {
    Button,
    Header,
  },
  name: "HomePage",
};
</script>

<style scoped>
@import url("../../fonts/fonts.css");

.page {
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.content {
  width: 100%;
  padding-top: 34px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.conten__wrapper {
  width: 100%;
  max-width: 980px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 940px;
}

.presentation {
  display: flex;
  flex-direction: column;
  /* justify-content: space-between; */
  align-items: flex-start;
  /* width: 100%; */
  /* min-height: 443px; */
  /* border: 1px solid black */
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

.completed-projects {
  max-width: 1100px;
  width: 100%;
  padding-top: 149px;
}

.completed-projects__wrapper {
  padding-left: 65px;
}

.completed-projects__title {
  font-weight: 500;
  font-size: 30px;
  line-height: 145%;
  letter-spacing: 0.02em;
  color: #1c1d28;
}

.completed-projects__arrow {
  font-size: 30px;
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

.about {
  max-width: 830px;
}

.about__title {
  margin: 0 0 15px 0;
  font-weight: 300;
  font-size: 15px;
  line-height: 145%;
  letter-spacing: 0.05em;
  color: #1c1d28;
}

.about__main-paragraph {
  margin: 0 0 40px 0;
  font-weight: bold;
  font-size: 30px;
  line-height: 145%;
  letter-spacing: 0.02em;
  color: #1c1d28;
}

.about__subparagraph {
  margin: 0;
  font-weight: normal;
  font-size: 15px;
  line-height: 185%;
  letter-spacing: 0.02em;
  color: #1c1d28;
}

.tabs-component-tabs {
  margin: 0;
}
</style>
