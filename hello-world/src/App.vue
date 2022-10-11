<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div>
    <pre>
      {{ JSON.stringify(formValue, null, 2) }}
    </pre>
  </div>
  <form>
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" v-model="formValue.name" />
    </div>
    <div>
      <label for="bio">Bio</label>
      <textarea id="bio" v-model="formValue.bio" />
    </div>
    <div>
      <label for="country">Country</label>
      <select type="text" id="country" v-model="formValue.country">
        <option value="Indonesia">Indonesia</option>
        <option value="Saudi Arabia">Saudi Arabia</option>
        <option value="United State">United State</option>
        <option value="Germany">Germany</option>
      </select>
    </div>
    <div>
      <label for="hobby">Hobby</label>
      <select multiple id="hobby" v-model="formValue.hobby">
        <option value="Soccer">Soccer</option>
        <option value="Tennis">Tennis</option>
        <option value="Golf">Golf</option>
        <option value="Racing">Racing</option>
      </select>
    </div>
  </form>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  data() {
    return {
      formValue: {
        name: "",
        bio: "",
        country: "",
        hobby: "",
      },
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
  text-align: center;
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
