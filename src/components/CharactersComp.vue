<template>
    <div class="container bg-light p-5">
        <div class="found" v-if="!loading">Found {{ charList.length }} characters</div>
        <div class="container">
            <div v-if="loading">
                <LoadingComp />
            </div>
            <div v-if="!loading">
                <div class="row d-flex align-items-center justify-content-center gap-3">
                    <CardComp :item="item" v-for="item in charList" :key="item.id" />
                </div>
            </div>

        </div>
    </div>
</template>

<script>
import CardComp from './CardComp.vue';
import LoadingComp from './LoadingComp.vue';

export default {
    name: "CharactersComp",
    props: [
        'charList',
        'loading'
    ],
    components: {
        CardComp,
        LoadingComp
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

.container {
    padding: 1.6em;
    min-height: 100vh;
}
</style>