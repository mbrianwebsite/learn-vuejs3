<template>
  <h2>Volume Tracker (0-20)</h2>
  <h3>Current Volume {{ volume }}</h3>
  <div>
    <button @click="volume -= 2">Decrease</button>
    <button @click="volume += 2">Increase</button>
  </div>
  <input type="text" v-model="movie" /><br />
  <input type="text" v-model="movieInfo.title" /><br />
  <input type="text" v-model="movieInfo.actor" /><br />
  <div>
    <button @click="movieList.push('Wonder Man')">Add Movie</button>
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  data() {
    return {
      volume: 0,
      movie: "Batman",
      movieInfo: {
        title: "",
        actor: "",
      },
      movieList: ["Batman", "Superman"],
    };
  },
  methods: {},
  computed: {},
  watch: {
    volume(newValue, oldValue) {
      if (newValue > oldValue && newValue === 16) {
        alert(
          "Listening to a high voulme for a long time may damage your hearing"
        );
      }
    },
    movie: {
      handler(newValue) {
        console.log(`Calling API with value = ${newValue}`);
      },
      immediate: true,
    },
    movieInfo: {
      handler(newValue) {
        console.log(
          `Calling API with value Title = ${newValue.title} and Actor = ${newValue.actor}`
        );
      },
      deep: true,
    },
    movieList: {
      handler(newValue) {
        console.log(`Updated Value Movie List ${newValue}`);
      },
      deep: true,
    },
  },
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
</style>
