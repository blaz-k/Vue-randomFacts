<template>
  <div>
    <div class="smthNew">
      <button @click="getRandom">Load random fact</button>

      <p>{{ fact.text }}</p>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "Facts",
  created() {
    this.getRandom();
    console.log("created");
  },
  data() {
    return {
      fact: "click on the button",
    };
  },
  methods: {
    getRandom() {
      axios
        .get("https://uselessfacts.jsph.pl/random.json?language=en")
        .then((response) => {
          console.log(response.data);
          this.fact = response.data;
        })
        .catch((error) => {
          console.log(error);
        });
    },
  },
};
</script>

<style scoped>
button {
  padding: 10px;
  background-color: yellowgreen;
  border-radius: 10%;
  margin-bottom: 20px;
  margin-top: 20px;
}

.smthNew {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>