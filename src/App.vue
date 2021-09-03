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
  margin: 10;
  padding: 0;
  display: ;
}

body {
  font-size: 10pt;

  font-family: Verdana, Geneva, Arial, Helvetica, sans-serif;

  color: black;

  line-height: 14pt;

  padding-left: 5pt;

  padding-right: 5pt;

  padding-top: 5pt;

}

h1 {
  font: 44px Verdana, Geneva, Arial, Helvetica, sans-serif;
  display: flex;
  justify-content: center;
  font-weight: bold;

  line-height: 20px;
}
</style>
