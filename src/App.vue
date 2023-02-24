<template>
  <LandingPage></LandingPage>
</template>

<script>
import LandingPage from './components/LandingPage.vue'

export default {
  name: 'App',
  components: {
    LandingPage
  },
  async created() {
        const indexedDB = window.indexedDB;
        if (!indexedDB) {
            console.log("IndexedDB could not be found in this browser.");
        }
        const request = indexedDB.open("mainDb", 1);
        console.log(">>>>>request: ", request);
    },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
}

</style>
