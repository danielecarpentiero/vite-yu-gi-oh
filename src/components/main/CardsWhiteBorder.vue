<template>
  <div class="cards-white-border">
    <InnerList />
  </div>
</template>

<script>
import InnerList from "./InnerList.vue";
export default {
  name: "CardsWhiteBorder",
  components: {
    InnerList,
  },
};
</script>

<style scoped>
.cards-white-border {
  width: 90%;
  margin: 0 auto;
  background-color: white;
  padding: 40px;
}
</style>
