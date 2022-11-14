<template>
    <div class="container bg-light p-5">
        <div class="found">Found TOT characters</div>
        <div class="row ">
            <div class=" col-2 d-flex flex-row">
                <CardComp />
            </div>

        </div>

    </div>
</template>

<script>
import CardComp from './CardComp.vue';

export default {
    name: "CharactersComp",
    components: {
        CardComp
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;

.found {
    padding: 1em;
    background-color: #000;
    height: 50px;
    font-weight: 700;
}
</style>