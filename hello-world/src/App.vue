<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <h2>{{ thename }}</h2>
  <div>
    <button @click="changeName($event), decrement2(2, $event)">
      Change Name
    </button>
  </div>
  <br />
  <h2>{{ count }}</h2>
  <div>
    <button @click="count = count - 1">Decrease Value</button>
    <button @click="count = count + 1">Increase Value</button>
  </div>
  <br />
  <h2>{{ number }}</h2>
  <div>
    <button @click="decrement2(2, $event)">
      Decrease Value -2 (Function, Event)
    </button>
    <button @click="decrement()">Decrease Value (Function)</button>
    <button @click="increment()">Increase Value (Function)</button>
    <button @click="increment2(2)">Increase Value +2 (Function)</button>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  data() {
    return {
      thename: "Muhammad Brian",
      count: 0,
      number: 0,
    };
  },
  methods: {
    changeName(event) {
      this.thename = "Ivan Haris";
      console.log("Event", event);
    },
    increment() {
      this.number += 1;
    },
    decrement() {
      this.number -= 1;
    },
    increment2(num) {
      this.number += num;
    },
    decrement2(num, event) {
      this.number -= num;
      console.log("Event", event);
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
