<template>
    <section class="d-flex p-2">
        <img src="/public/images/breaking_bad.6d275852.jpg" alt="Logo">
        <h1>{{ title }}</h1>
    </section>
</template>

<script>

export default {
    name: "HeaderComp",
    props: {
        title: String
    }
}
</script>

<style lang="scss" scoped>
img {
    width: 2%;
    margin: 0.5em;
}

h1 {
    display: inline;
    font-weight: 700;
    margin: 0;
}
</style>