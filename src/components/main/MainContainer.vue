<template>
  <div class="main-container">
    <CardsWhiteBorder />
  </div>
</template>

<script>
import CardsWhiteBorder from "./CardsWhiteBorder.vue";
export default {
  name: "MainContainer",

  components: {
    CardsWhiteBorder,
  },
};
</script>

<style scoped lang="scss">
.main-container {
  margin: 0 auto;
  width: 100%;
}
</style>
