<template>
  <div class="page">
    <Header />
    <main class="content">
      <div class="conten__wrapper">
        <Presentation />
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
          <div class="completed-projects__tabs-box">
            <ul class="completed-projects__tabs-list">
              <li
                v-for="(isTabActive, numberOfTab) in selectedTab"
                :key="numberOfTab"
                @click="selectTab(numberOfTab)"
                :class="{ 'completed-projects__tab_is-active': isTabActive }"
                class="completed-projects__tab"
              >
                <a class="completed-projects__tab-link">{{ numberOfTab }} </a>
              </li>
              <li class="completed-projects__tab">
                Все работы
                <img
                  src="../../images/arrow.svg"
                  alt="arrow"
                  class="completed-projects__tab-arrow"
                />
              </li>
            </ul>
            <div class="completed-projects__grid"></div>
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
import Header from "../../components/Header.vue";
import Presentation from "./Presentation.vue";

export default {
  components: {
    Header,
    Presentation,
  },
  name: "HomePage",
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

.completed-projects {
  max-width: 1100px;
  width: 100%;
  padding-top: 149px;
}

.completed-projects__wrapper {
  padding-left: 65px;
}

.completed-projects__title {
  margin: 0 0 25px 0;
  font-weight: 500;
  font-size: 30px;
  line-height: 145%;
  letter-spacing: 0.02em;
  color: #1c1d28;
}

.completed-projects__tabs-box {
}

.completed-projects__tabs-list {
  list-style-type: none;
  margin: 0 0 30px 0;
  padding: 0;
  display: flex;
}

.completed-projects__tab {
  margin-right: 40px;
  transition: all 0.2s linear;
  cursor: pointer;
}

.completed-projects__tab:last-of-type {
  margin-right: 0;
  margin-left: auto;
  color: #ff5c66;
}

.completed-projects__tab-link {
  color: inherit;
  text-decoration: none;
}

.completed-projects__tab-arrow {
  display: inline-block;
  font-size: 35px;
  vertical-align: middle;
  line-height: 0;
}

.completed-projects__tab_is-active {
  color: #ff5c66;
  text-decoration: underline;
  text-underline-offset: 8px;
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
