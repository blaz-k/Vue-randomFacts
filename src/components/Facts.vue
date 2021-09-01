<template>
  <div>
    <div v-bind:key="fact.id" v-for="fact in facts">
      <h3>{{ fact.title }}</h3>
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