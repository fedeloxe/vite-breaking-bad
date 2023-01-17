<script>
import axios from 'axios';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppCard from './components/AppSingleCard.vue';
import { store } from './store.js';

export default {
  components: {
    AppHeader,
    AppMain,
    AppSingleCard,

  },
  data() {
    return {
      store
    }
  },
  methods: {
    getCharacters() {
      axios.get(store.url).then((response) => {
        store.charactersList = response.data.data
        setTimeout(() => {
          store.loading = false
        }, 100)
      })

    }
  }
}

</script>

<template>
  <AppHeader />
  <AppMain />
  <AppSingleCard />

</template>

<style lang="scss" >
@use './styles/generals.scss'
</style>
