<template>
    <div class="mycard text-center">
        <img :src="item.img" :alt="item.name" class="img-fluid">
        <h4 class="fs-5">{{ item.name }}</h4>
        <h3 class="fs-4">{{ item.category }}</h3>
        <h3 class="fs-6">{{ item.status }}</h3>
    </div>
</template>

<script>
export default {
    name: 'CardComp',
    props: [
        'item',
    ]
}
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/variables' as *;

.mycard {
    color: black;
    padding: 1em;
    background-color: $background;
    width: 220px;
    height: 500px;

    img {
        width: 218px;
        height: 310px;
        object-fit: cover;
    }

    h4 {
        color: #fff;
        padding: 0.3em;
        font-weight: 700;
        text-transform: uppercase;
        height: 70px;
    }

    h3 {
        color: $font-color;
    }
}
</style>