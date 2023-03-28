<script>
import axios from 'axios';
import { store } from './store';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

export default {
  name: 'Yu-Gi-Oh',
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
    callApi() {
      if (this.store.searchStatus !== '') {
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php', {
          params: {
            archetype: this.store.searchStatus
          }
        })
          .then((response) => {
            this.store.cards = response.data.data;
            this.store.cardsCut = this.store.cards.slice(0, 40);
          })
          // .catch((error) => {
          //   console.log(error);
          //   this.store.cardsCut = [];
          // })
      } else {
        axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php')
          .then((response) => {
            this.store.cards = response.data.data;
            this.store.cardsCut = this.store.cards.slice(0, 40);
          })
      }
    }
  },
  created() {
    this.callApi();
  }
}
</script>

<template>
  <AppHeader></AppHeader>
  <AppMain @search="callApi"></AppMain>
</template>

<style>
body {
  height: 100vh;
}

#app {
  height: 100%;
}
</style>
