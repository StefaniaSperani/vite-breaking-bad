<template>
    <div class="spinner">
        <i class="fa-solid fa-spinner fa-2xl"></i>
    </div>
</template>

<script>
export default {
    name: 'LoadingComp',
}
</script>

<style lang="scss" scoped>
@use '../assets/style/general' as *;

.spinner {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);

    color: #000;
    text-align: center;
    animation: spinner 2s infinite linear;

    @keyframes spinner {
        0% {
            transform: rotate(0deg);
        }

        100% {
            transform: rotate(360deg);
        }
    }


}
</style>