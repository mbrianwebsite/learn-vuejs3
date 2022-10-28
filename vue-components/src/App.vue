<template>
  <GreetWord name="Muhammad" otherName="Ahmad" />
  <GreetWord name="Brian" otherName="Adam" />
  <GreetWord name="Ivan" otherName="Haris" />
  <GreetWord :name="name" :otherName="channel" />
</template>

<script>
import GreetWord from "./components/GreetWord.vue";

export default {
  name: "App",
  components: {
    GreetWord,
  },
  data() {
    return {
      name: "MBrian Website",
      channel: "mbrianwebsite.com",
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
