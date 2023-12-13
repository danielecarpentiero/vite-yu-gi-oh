<template>
  <div class="main">
    <Select @selectedArchetype="select" />
    <MainContainer />
  </div>
</template>

<script>
import MainContainer from "./MainContainer.vue";
import axios from "axios";
import { store } from "../../store";
import Select from "./Select.vue";
export default {
  name: "Main",
  components: {
    MainContainer,
    Select,
  },
  data() {
    return {
      store,
      apiURLOffset:
        "https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0",
      apiURL: "https://db.ygoprodeck.com/api/v7/cardinfo.php",
    };
  },
  methods: {
    select() {
      if (this.store.selectedArchetype === "") {
        axios.get(this.apiURLOffset).then((response) => {
          this.store.cards = response.data.data;
        });
      } else {
        axios
          .get(this.apiURL, {
            params: {
              archetype: this.store.selectedArchetype,
            },
          })
          .then((response) => {
            this.store.cards = response.data.data;
          });
      }
    },
  },
  created() {
    this.select();
  },
};
</script>

<style scoped>
.main {
  background-color: #d48f38;
}
</style>
