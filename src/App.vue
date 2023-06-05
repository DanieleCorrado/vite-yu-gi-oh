<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import { store } from './store';
import axios from 'axios';

export default {
  components: {
    AppHeader,
    AppMain
  },
  data() {
      return {
        store
      }
    },
    methods: {
      getCards() {
        axios.get(store.apiURL).then(cards => {
          store.cardsList = cards.data.data;
        }).catch(error => {
          console.log(error);
        })
      }
    },
    created() {
      this.getCards();
    }
}
</script>

<template>

  <AppHeader />
  <AppMain/>
  
</template>

<style lang="scss" scoped>

@use './styles/generals.scss' as *;

</style>
