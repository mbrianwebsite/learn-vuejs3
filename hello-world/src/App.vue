<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <h2>{{ name }}</h2>
  <div>
    <button v-on:click="name = 'Ivan Haris'">Change Name</button>
  </div>
  <br />
  <h2>{{ count }}</h2>
  <div>
    <button v-on:click="count = count - 1">Decrease Value</button>
    <button v-on:click="count = count + 1">Increase Value</button>
  </div>
  <br />
  <h2>{{ number }}</h2>
  <div>
    <button v-on:click="decrement2(2)">Decrease Value -2 (Function)</button>
    <button v-on:click="decrement()">Decrease Value (Function)</button>
    <button v-on:click="increment()">Increase Value (Function)</button>
    <button v-on:click="increment2(2)">Increase Value +2 (Function)</button>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  data() {
    return {
      name: "Muhammad Brian",
      count: 0,
      number: 0,
    };
  },
  methods: {
    increment() {
      this.number += 1;
    },
    decrement() {
      this.number -= 1;
    },
    increment2(num) {
      this.number += num;
    },
    decrement2(num) {
      this.number -= num;
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
