<template>
    <div class="col mycard">
        <img :src="item.img" :alt="item.name" class="img-fluid">
        <h4>{{ item.name }}</h4>
        <h3>{{ item.status }}</h3>
        <div></div>
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
    height: 500px;

    img {
        width: 218px;
        height: 310px;
        object-fit: cover;
    }

    h4 {
        color: #fff;
    }
}
</style>