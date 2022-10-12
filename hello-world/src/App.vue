<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <h2 v-once>{{ name }}</h2>
  <div>
    <button @click="name = 'Batman'">Click</button>
    <h2 v-pre>{{ name }}</h2>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  data() {
    return {
      name: "Robin",
    };
  },
  methods: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}

label {
  font-weight: 600;
  display: flex;
  margin-bottom: 5px;
}

input + label {
  font-weight: 600;
  display: inline-flex;
  margin-bottom: 20px;
}

input[type="text"],
input[type="number"],
textarea,
select {
  display: block;
  width: 400px;
  padding: 6px 12px;
  font-size: 14;
  line-height: 1.43;
  color: #555;
  background-color: #fff;
  border: 1px solid #ccc;
  border-radius: 4px;
}
</style>
