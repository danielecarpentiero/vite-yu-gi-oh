<template>
  <div class="main">
    <MainContainer />
  </div>
</template>

<script>
import MainContainer from "./MainContainer.vue";
import axios from "axios";
import { store } from "../../store";
export default {
  name: "Main",
  components: {
    MainContainer,
  },
  data() {
    return {
      store,
      apiURL: "https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0",
    };
  },
  created() {
    axios.get(this.apiURL).then((response) => {
      store.cards = response.data.data;
    });
  },
};
</script>

<style scoped>
.main {
  background-color: #d48f38;
}
</style>
