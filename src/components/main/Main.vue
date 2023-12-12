<template>
  <div class="main">
    <MainContainer />
  </div>
</template>

<script>
import MainContainer from "./MainContainer.vue";
export default {
  name: "Main",
  components: {
    MainContainer,
  },
};
</script>

<style scoped>
.main {
  background-color: #d48f38;
}
</style>
