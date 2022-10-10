<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div>
    <h2 v-if="num === 0">This Number Is Zero</h2>
    <h2 v-else-if="num < 0">This Number Is Negative</h2>
    <h2 v-else-if="num > 0">This Number Is Positive</h2>
    <h2 v-else>This Not A Number</h2>

    <template v-if="display == true">
      <h2>Muhammad Brian</h2>
      <h2>Website Developer</h2>
      <h2>MBrian Website</h2>
    </template>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  data() {
    return {
      num: "This not a number",
      display: true,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
