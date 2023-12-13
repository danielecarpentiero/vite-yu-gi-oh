<template>
  <select
    @change="$emit('select')"
    v-model="store.selectedArchetype"
    id="archetypeSelect"
    name="archetypes"
  >
    <option selected value="">Choose an archetype</option>
    <option v-for="pippo in store.archetypes">
      {{ pippo.archetype_name }}
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
      length: 0,
      apiURL: "https://db.ygoprodeck.com/api/v7/archetypes.php",
    };
  },
  created() {
    axios.get(this.apiURL).then((response) => {
      store.archetypes = response.data;
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
