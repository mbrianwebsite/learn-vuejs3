<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <h1>Full Name - {{ firstName }} {{ lastName }}</h1>
  <h1>Computed Full Name - {{ fullName }}</h1>
  <h2>
    Total - {{ items.reduce((total, curr) => (total = total + curr.price), 0) }}
  </h2>
  <button
    @click="
      items.push({
        id: 1,
        title: 'Phone',
        price: 100,
      })
    "
  >
    Push Item
  </button>
  <h2>Total - {{ total }}</h2>
  <h2>Method Total - {{ getTotal() }}</h2>
  <input v-model="country" type="text" />
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  data() {
    return {
      firstName: "Muhammmad",
      lastName: "Brian",
      items: [
        {
          id: 1,
          title: "Phone",
          price: 100,
        },
        {
          id: 2,
          title: "Tablet",
          price: 200,
        },
        {
          id: 3,
          title: "TV",
          price: 300,
        },
      ],
      country: "",
    };
  },
  methods: {
    getTotal() {
      console.log("getTotal");
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
    },
  },
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
    total() {
      console.log("total");
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
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
