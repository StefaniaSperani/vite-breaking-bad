<template>
    <section class="d-flex p-2">
        <img src="public\images\breaking_bad.6d275852.jpg" alt="Logo">
        <h1>Breaking Bad API</h1>
    </section>
</template>

<script>
import SelectComp from './SelectComp.vue';

export default {
    name: "HeaderComp",
    components: { SelectComp }
}
</script>

<style lang="scss" scoped>
img {
    width: 2%;
    margin: 0.5em;
}

h1 {
    display: inline;
}
</style>