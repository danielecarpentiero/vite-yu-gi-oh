<template>
  <div class="logo">
    <img :src="image" alt="yugioh logo" />
  </div>
</template>

<script>
export default {
  name: "HeaderLogo",
  data() {
    return {
      image: "src/components/header/logo.jpg",
    };
  },
};
</script>

<style scoped lang="scss">
.logo {
  width: 3%;
  img {
    width: 100%;
  }
}
</style>
