<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div>
    <div>{{ greet }} {{ name }}</div>
    <div v-text="channel"></div>
    <div v-html="channelBold"></div>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  data() {
    return {
      greet: "Hello",
      name: "Bro",
      channel: "MBrian Website",
      channelBold: "<b>MBrian Website</b>",
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
