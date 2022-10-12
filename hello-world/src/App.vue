<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div>
    <pre>
      {{ JSON.stringify(formValue, null, 2) }}
    </pre>
  </div>
  <form @submit.prevent="submitForm">
    <div>
      <label for="name">Name</label>
      <input type="text" id="name" v-model.trim="formValue.name" />
    </div>
    <div>
      <label for="nickName">Nick Name</label>
      <input type="text" id="nickName" v-model.trim.lazy="formValue.nickName" />
    </div>
    <div>
      <label for="age">Age</label>
      <input
        @keyup.enter="submitForm"
        type="number"
        id="age"
        v-model.number="formValue.age"
      />
    </div>
    <div>
      <label for="bio">Bio</label>
      <textarea id="bio" v-model="formValue.bio" />
    </div>
    <div>
      <label for="country">Country</label>
      <select id="country" v-model="formValue.country">
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
    <div>
      <input
        type="checkbox"
        id="status"
        v-model="formValue.status"
        true-value="yes"
        false-value="no"
      />
      <label for="status">Are you a Programmer</label>
    </div>
    <div>
      <div>Skill Set</div>
      <input
        type="checkbox"
        id="html"
        value="html"
        v-model="formValue.skillSet"
      />
      <label for="html">html</label>
      <input
        type="checkbox"
        id="css"
        value="css"
        v-model="formValue.skillSet"
      />
      <label for="css">css</label>
      <input type="checkbox" id="js" value="js" v-model="formValue.skillSet" />
      <label for="js">js</label>
    </div>
    <div>
      <div>Year of Experience</div>
      <input type="radio" id="0-2" value="0-2" v-model="formValue.experience" />
      <label for="0-2">0-2</label>
      <input type="radio" id="2-6" value="2-6" v-model="formValue.experience" />
      <label for="2-6">2-6</label>
      <input type="radio" id="6-8" value="6-8" v-model="formValue.experience" />
      <label for="6-8">6-8</label>
      <input
        type="radio"
        id="8-10"
        value="8-10"
        v-model="formValue.experience"
      />
      <label for="8-10">8-10</label>
    </div>
    <button>Submit</button>
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
        nickName: "",
        age: null,
        bio: "",
        country: "",
        hobby: [],
        status: "no",
        skillSet: [],
        experience: "",
      },
    };
  },
  methods: {
    submitForm() {
      console.log("Form Values", this.formValue);
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
