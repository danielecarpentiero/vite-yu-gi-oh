<template>
  <div class="single-card">
    <img :src="img" alt="card-desc" />
    <h3>{{ title }}</h3>
    <div class="archetype">{{ archetype }}</div>
  </div>
</template>

<script>
export default {
  name: "SingleCard",
  props: ["img", "title", "archetype"],
};
</script>

<style scoped>
.single-card {
  width: 100%;
}
</style>
