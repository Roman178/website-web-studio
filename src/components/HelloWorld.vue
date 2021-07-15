<template>
  <div class="hello">
    <h1>Hello Vue {{ test }}</h1>
    <h2>{{ myProp }}</h2>
    <h2>{{ computedTest }}</h2>
    <p v-bind:key="index" v-for="(item, index) in computedTest">
      {{ item + " " + myProp }}
    </p>

    <form action="">
      <label for="my-input">
        <input type="text" v-model="test" id="my-input" />
      </label>
    </form>
    <button @click="myMethod">Button</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",

  methods: {
    myMethod() {
      this.$watch("computedTest", function(newVal, oldVal) {
        const gop = `
        ${oldVal} 
        ${newVal} 
        Changed
        `;
        return console.log(gop);
      });
    },
  },

  // watch: {
  //   computedTest: {
  //     handler() {
  //       console.log("Changed");
  //     },
  //   },
  // },

  computed: {
    computedTest() {
      return (this.test + " COMPUTED " + 13).split(" ");
    },
  },

  props: {
    myProp: {
      type: String,
      default: "Hi from props",
    },
  },
  data() {
    return {
      test: "Hello JOPRF ",
    };
  },
};
</script>

<style scoped></style>
