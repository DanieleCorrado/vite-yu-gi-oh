<script>
import SingleCard from './SingleCard.vue';
import { store } from '../store';

export default {
    name: "AppMain",
    components: {
      SingleCard
    },
    data() {
      return {
        store
      }
    }
}

</script>

<template>
  
  <section id="container">


    <div id="list">

      <div id="card-number">
        <h4>Found {{ store.cardsList.length }} cards</h4>
      </div>

      <div id="cards">

        <!-- carta -->

        <SingleCard v-for="card in store.cardsList" :details="card"/>

      </div>

    </div>

  </section>


</template>

<style lang="scss" scoped>

#container {
  width: 90%;
  margin: 0 auto;
  margin-top: 50px;
  background-color: white;
  padding: 20px 0;

  #list {
    color: white;
    width: 95%;
    margin: 0 auto;

    #card-number {
      background-color: black;
      padding: 10px;
    }

    #cards {

      display: flex;
      flex-wrap: wrap;
    }

  }
}


</style>
