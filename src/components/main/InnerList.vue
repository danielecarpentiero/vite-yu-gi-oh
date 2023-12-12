<template>
  <div class="inner-list">
    <ul>
      <li
        v-for="card in store.cards"
        :img="card.card_images[0].image_url"
        :title="card.name"
        :archetype="card.archetype"
      ></li>
    </ul>
  </div>
</template>

<script>
import SingleCard from "./SingleCard.vue";
import { store } from "../../store";
export default {
  name: "InnerList",
  components: {
    SingleCard,
  },
  data() {
    return {
      store,
    };
  },
};
</script>

<style scoped>
.inner-list {
  li {
    height: 100px;
  }
}
</style>
