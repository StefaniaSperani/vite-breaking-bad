<template>
    <div class="mycard text-center">
        <div class="image-wrapper">
            <img :src="item.img" :alt="item.name" class="img-fluid">
        </div>
        <h4 class="fs-5">{{ item.name }}</h4>
        <h3 class="fs-4 category">{{ item.category }}</h3>
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

    .image-wrapper {
        display: flex;
        align-items: center;
        justify-content: center;
        width: 190px;
        height: 300px;
    }

    img {
        width: 218px;
        height: 310px;
        object-fit: cover;
    }

    .category {
        padding-top: 0.3em;
    }

    h4 {
        color: #fff;
        padding: 0.5em;
        font-weight: 700;
        text-transform: uppercase;
        height: 70px;
    }

    h3 {
        color: $font-color;
        height: 57px;
    }
}
</style>