<template>
  <div class="main-container">
    <Select />
    <CardsWhiteBorder />
  </div>
</template>

<script>
import Select from "./Select.vue";
import CardsWhiteBorder from "./CardsWhiteBorder.vue";
export default {
  name: "MainContainer",
  components: {
    Select,
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
