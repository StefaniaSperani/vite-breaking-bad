<template>
  <header>
    <HeaderComp />
  </header>
  <main>
    <SelectComp />
    <CharactersComp />
  </main>

</template>

<script>
import "@fontsource/montserrat"
import CharactersComp from "./components/CharactersComp.vue";
import HeaderComp from "./components/HeaderComp.vue";
import SelectComp from "./components/SelectComp.vue";
export default {
  components: {
    HeaderComp,
    SelectComp,
    CharactersComp
  }
}
</script>

<style lang="scss" scoped>

</style>
