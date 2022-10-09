<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <div>
    <div>{{ greet }} {{ name }}</div>
    <div v-text="channel"></div>
    <div v-html="channelBold"></div>
    <div v-bind:id="headingId">Heading</div>
    <button v-bind:disabled="isDisabled">Button</button>
    <h1 v-bind:class="status">Status</h1>
    <h1 v-bind:class="isItalic && status">Italic</h1>
    <h1 v-bind:class="isItalic ? status : 'strong'">Bold Or Italic</h1>
    <h1 v-bind:class="[status, 'strong']">Bold and Italic</h1>
    <h1 v-bind:class="[isItalic && status, isItalic ? status : 'strong']">
      Function at Array
    </h1>
    <h1
      v-bind:class="{
        toitalic: isItalic,
        strong: !isItalic,
      }"
    >
      Bold and Italic
    </h1>
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
      headingId: "heading",
      isDisabled: true,
      status: "toitalic",
      isItalic: true,
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

.toitalic {
  font-style: italic;
}

.strong {
  font-weight: 900;
}
</style>
