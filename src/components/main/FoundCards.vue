<template>
  <div class="found-cards">
    <h3>Found {{ store.cards.length }} cards</h3>
  </div>
</template>

<script>
import { store } from "../../store";
export default {
  name: "FoundCards",
  data() {
    return {
      store,
    };
  },
};
</script>

<style scoped>
.found-cards {
  width: 100%;
  background-color: black;
  padding: 20px;
  color: white;
  font-weight: 700;
  h3 {
    font-family: Verdana, Geneva, Tahoma, sans-serif;
  }
}
</style>
