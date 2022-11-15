<template>
  <header>
    <HeaderComp title="Breaking Bad Api" />
  </header>
  <main>
    <SelectComp @filterCategory="filterChar" />
    <CharactersComp :charList="filteredCategory" :loading="loading" />

  </main>

</template>

<script>
import "@fontsource/montserrat"
import CharactersComp from "./components/CharactersComp.vue";
import HeaderComp from "./components/HeaderComp.vue";
import SelectComp from "./components/SelectComp.vue";
import axios from 'axios'



export default {
  components: {
    HeaderComp,
    SelectComp,
    CharactersComp
  },
  data() {
    return {
      apiURL: 'https://www.breakingbadapi.com/api/characters',
      charList: [],
      loading: true,
      searchCat: ''
    }
  },
  computed: {
    filteredCategory() {
      return this.charList.filter((char) => {
        if (char.category.toLowerCase().includes(this.searchCat.toLowerCase())) {
          return true;
        }
      })
    }
  },
  methods: {
    getChar() {
      axios.get(this.apiURL).then(
        (response) => {
          this.charList = response.data;
          this.loading = false;
        }
      ).catch((error) => {
        this.loading = false;
        console.log(error);
      })
    },
    filterChar(value) {
      this.searchCat = value
    }
  },
  created() {
    this.getChar()
  }
}
</script>

<style lang="scss" scoped>

</style>
