<template>
  <button>{{ text }}</button>
</template>

<script>
export default {
  name: "MyButton",
  props: ["text"],
};
</script>

<style scoped>
button {
  padding: 10px;
  background-color: yellowgreen;
  border-radius: 20%;
}
</style>