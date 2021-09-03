<template>
  <div id="app">
    <h1>Random facts</h1>
    <Facts />
  </div>
</template>

<script>
import Facts from "./components/Facts";

export default {
  name: "app",
  components: {
    Facts,
  },
};
</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  line-height: 1.4;
}
</style>
