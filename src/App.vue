<template>
  <header>
    <HeaderComp title="Breaking Bad Api" />
  </header>
  <main>
    <SelectComp />
    <CharactersComp :charList="charList" />
  </main>

</template>

<script>
import "@fontsource/montserrat"
import CharactersComp from "./components/CharactersComp.vue";
import HeaderComp from "./components/HeaderComp.vue";
import SelectComp from "./components/SelectComp.vue";
import axios from 'axios'
/*
"char_id": 1,
"name": "Walter White",
"img": "",
"status": "Presumed dead",
*/
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
    }
  },
  methods: {
    getChar() {
      axios.get(this.apiURL).then(
        (response) => {
          this.charList = response.data;
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
