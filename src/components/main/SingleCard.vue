<template>
  <div class="single-card">
    <div class="box">
      <img :src="img" alt="card-desc" />
      <h3>{{ title }}</h3>
      <div class="archetype">{{ archetype }}</div>
    </div>
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
  font-family: "Trebuchet MS", "Lucida Sans Unicode", "Lucida Grande",
    "Lucida Sans", Arial, sans-serif;
}
.box {
  text-align: center;
  margin-top: 20px;
  padding-bottom: 100px;
  background-color: orange;
  img {
    width: 100%;
  }

  h3 {
    color: white;
    font-size: 2rem;
  }
  .archetype {
    font-size: 1.5rem;
  }
}
</style>
