<template>
  <header>
    <HeaderComp />
  </header>
  <main>
    <SelectComp />
  </main>

</template>

<script>
import "@fontsource/montserrat"
import HeaderComp from "./components/HeaderComp.vue";
import SelectComp from "./components/SelectComp.vue";
export default {
  components: {
    HeaderComp,
    SelectComp,
  }
}
</script>

<style lang="scss" scoped>

</style>
