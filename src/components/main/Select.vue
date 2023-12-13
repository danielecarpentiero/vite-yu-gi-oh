<template>
  <select id="opzioni" name="opzioni">
    <option v-for="archetype in archetypes" value="opzione1">
      {{ store.archetype }}
    </option>
  </select>
</template>

<script>
import axios from "axios";
import { store } from "../../store";
export default {
  name: "Select",
  data() {
    return {
      store,
      apiURL: "https://db.ygoprodeck.com/api/v7/archetypes.php",
    };
  },
  created() {
    axios.get(this.apiURL).then((response) => {
      store.cards = response.data.archetypes;
    });
  },
};
</script>

<style scoped>
select {
  padding: 5px;
  padding-right: 50px;
  margin: 50px 100px;
}
</style>
