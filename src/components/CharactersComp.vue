<template>
    <div class="container bg-light p-5">
        <div class="found">Found {{ charList.length }} characters</div>
        <div class="container">
            <div class="row d-flex align-items-center justify-content-center gap-3">
                <CardComp :item="item" v-for="item in charList" :key="item.id" />
            </div>
        </div>
    </div>
</template>

<script>
import CardComp from './CardComp.vue';

export default {
    name: "CharactersComp",
    props: [
        'charList',
    ],
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

.container {
    padding: 1.6em;
}
</style>