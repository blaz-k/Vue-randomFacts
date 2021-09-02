<template>
  <div id="app">
    <h1>Random facts</h1>
    <button>Submit</button>
    <MyButton text="clicked" />
    <Facts />

    <MyButton text="drugi click" />
  </div>
</template>

<script>
import Facts from "./components/Facts";
import MyButton from "./components/MyButton";
import axios from "axios";

export default {
  name: "app",
  components: {
    Facts,
    MyButton,
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
        .then((response) => (this.facts = response.data))
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
