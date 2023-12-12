<template>
  <header>
    <HeaderLogo />
    <h1>Yu-Gi-Oh Api</h1>
  </header>
</template>

<script>
import HeaderLogo from "./HeaderLogo.vue";
export default {
  name: "Header",
  components: {
    HeaderLogo,
  },
  // Your component's logic goes here
};
</script>

<style scoped lang="scss">
header {
  padding-left: 50px;
  display: flex;
  width: 100%;
  align-items: center;
  h1 {
    font-size: 3rem;
  }
}
</style>
