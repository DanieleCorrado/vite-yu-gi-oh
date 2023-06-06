<script>
import { store } from '../store';

export default {
    name: "AppSearch",
    data() {
      return {
        store
      }
    }
}

</script>

<template>
  
  <section id="container">

    <select @change="$emit('search')" v-model="store.searchText">
      <option value="-1">Select card archetype</option>
      <option :value="idx" v-for="(archetype, idx) in store.cardsType" >{{ archetype.archetype_name }}</option>
    </select>

  </section>


</template>

<style lang="scss" scoped>

#container {
  width: 90%;
  margin: 20px auto;
}


</style>


