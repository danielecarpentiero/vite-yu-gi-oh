<template>
  <div class="cards-white-border">
    <FoundCards />
    <InnerList />
  </div>
</template>

<script>
import FoundCards from "./FoundCards.vue";
import InnerList from "./InnerList.vue";
export default {
  name: "CardsWhiteBorder",
  components: {
    FoundCards,
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
