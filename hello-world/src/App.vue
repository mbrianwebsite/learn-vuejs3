<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <h2>Inline = {{ 1 + 2 + 3 }}</h2>
  <h2>Add = {{ add() }}</h2>
  <h2>Plus = {{ plus(5, 6, 7) }}</h2>
  <h2>Multiply = {{ multiply(10) }}</h2>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  data() {
    return {
      baseMultiplier: 5,
    };
  },
  methods: {
    add() {
      return 2 + 3 + 5;
    },
    plus(a, b, c) {
      return a + b + c;
    },
    multiply(number) {
      return number * this.baseMultiplier;
    },
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
