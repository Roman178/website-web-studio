<template>
  <button class="btn">{{ textButton }}</button>
</template>

<script>
export default {
  name: "Button",
  props: {
    textButton: {
      type: String,
      default: () => "",
    },
  },
};
</script>

<style scoped>
.btn {
  margin: 0;
  padding: 0;
  border: none;
  width: 171px;
  height: 41px;
  background-color: #5551f7;
  font-family: "Montserrat";
  font-weight: 500;
  font-size: 13px;
  line-height: 16px;
  letter-spacing: 0.02em;
  color: #fff;
  cursor: pointer;
}
</style>
