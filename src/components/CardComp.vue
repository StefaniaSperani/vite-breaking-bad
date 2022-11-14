<template>
    <div class="col mycard">
        <img src="" alt="">
        <h3></h3>
        <h2></h2>
        <div></div>
    </div>
</template>

<script>
export default {
    name: 'CardComp',
}
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;

.mycard {
    color: black;
    padding: 1em;
    background-color: $background;
}
</style>