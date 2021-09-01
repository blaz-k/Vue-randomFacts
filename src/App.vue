<template>
  <div id="app">
    <Facts v-bind:facts="facts" />
  </div>
</template>

<script>
import Facts from "./components/Facts";
import axios from "axios";

export default {
  name: "app",
  components: {
    Facts,
  },
  data() {
    return {
      facts: [],
    };
  },
  methods: {
    created() {
      axios
        .get("https://uselessfacts.jsph.pl/random.json?language=en")
        .then((res) => (this.facts = res.data))
        .catch((err) => console.log(err));
    },
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

/*
.btn {
  display: inline-block;
  border: none;
  background: #555;
  color: #fff;
  padding: 7px 20px;
  cursor: pointer;
}
.btn:hover {
  background: #666;
}*/
</style>
