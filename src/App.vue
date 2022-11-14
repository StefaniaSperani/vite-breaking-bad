<template>
  <header>
    <HeaderComp title="Breaking Bad Api" />
  </header>
  <main>
    <SelectComp />
    <div v-if="loading">
      <LoadingComp />
    </div>
    <div v-if="!loading">
      <CharactersComp :charList="charList" />
    </div>

  </main>

</template>

<script>
import "@fontsource/montserrat"
import CharactersComp from "./components/CharactersComp.vue";
import HeaderComp from "./components/HeaderComp.vue";
import SelectComp from "./components/SelectComp.vue";
import LoadingComp from './components/LoadingComp.vue';
import axios from 'axios'



export default {
  components: {
    HeaderComp,
    SelectComp,
    CharactersComp,
    LoadingComp
  },
  data() {
    return {
      apiURL: 'https://www.breakingbadapi.com/api/characters',
      charList: [],
      loading: true
    }
  },
  methods: {
    getChar() {
      axios.get(this.apiURL).then(
        (response) => {
          this.charList = response.data;
          this.loading = false;
        }
      )
    }
  },
  created() {
    this.getChar()
  }
}
</script>

<style lang="scss" scoped>

</style>
