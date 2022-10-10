<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
  <h2 v-for="name in fullNames" :key="name.first">
    {{ name.first }} {{ name.last }}
  </h2>
  <div v-for="actor in actors" :key="actor.name">
    <h2>{{ actor.name }}</h2>
    <h3 v-for="movie in actor.movies" :key="movie">{{ movie }}</h3>
  </div>
  <h2 v-for="(value, index, key) in myInfo" :key="value">
    {{ key }} {{ index }} {{ value }}
  </h2>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  data() {
    return {
      names: ["Muhammad", "Brian", "Ivan"],
      fullNames: [
        { first: "Muhammad", last: "Brian" },
        { first: "Ivan", last: "Haris" },
      ],
      actors: [
        { name: "C. Bale", movies: ["Batman", "The Prestige"] },
        { name: "L. D. Caprio", movies: ["Titanic", "Inception"] },
      ],
      myInfo: {
        myName: "Muhammad",
        myChannel: "MBrian Website",
        myCourse: "Vue",
      },
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
