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

<template>
  <div class="inner-list">
    <ul>
      <li v-for="card in store.cards">
        <SingleCard
          :img="card.card_images[0].image_url"
          :title="card.name"
          :archetype="card.archetype"
        />
      </li>
    </ul>
  </div>
</template>

<style scoped>
.inner-list {
  ul {
    display: flex;
    flex-wrap: wrap;
    li {
      width: calc((100% / 5) - 40px);
      list-style-type: none;
      padding: 0 20px;
    }
  }
}
</style>
