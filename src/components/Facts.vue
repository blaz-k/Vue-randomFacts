<template>
  <div>
    <div>
      <button @click="getRandom">Load rendom fact</button>
      <div v-bind:key="facts.id">
        <p>{{ facts.id }} {{ facts.text }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "Facts",
  data() {
    return {
      facts: [],
    };
  },
  methods: {
    getRandom() {
      axios
        .get("https://uselessfacts.jsph.pl/random.json?language=en")
        .then((response) => {
          console.log(response.data);
          this.posts = response.data;
        })
        .catch((error) => {
          console.log(error);
        });
    },
  },
};
</script>

<style scoped>
</style>