<template>
  <div>
    <div v-bind:facts="facts">
      <h3>random facts from facts: {{ facts }}</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: "Facts",
  props: ["facts"],
};
</script>

<style scoped>
</style>