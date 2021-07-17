<template>
  <div id="app">
    <!-- <HelloWorld myProp="From parent" /> -->
    <HomePage></HomePage>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import HomePage from "./pages/HomePage/HomePage.vue";

export default {
  name: "App",
  components: {
    HomePage,

    // HelloWorld,
  },
};
</script>

<style>
#app {
  padding: 30px 30px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  font-family: "Montserrat", Arial, Helvetica, sans-serif;
}
</style>
