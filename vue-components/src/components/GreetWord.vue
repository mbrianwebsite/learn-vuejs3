<template>
  <h2>Hello {{ name }} a.k.a {{ otherName }}</h2>
</template>

<script>
export default {
  name: "GreetWord",
  props: ["name", "otherName"],
};
</script>

<style scoped></style>
