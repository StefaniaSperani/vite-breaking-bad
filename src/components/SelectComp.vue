<template>
    <div class="container">
        <select v-model="selected">
            <option disabled value="">Select category</option>
            <option value="">A</option>
            <option value="">B</option>
            <option value="">C</option>
        </select>

    </div>

</template>

<script>
export default {
    name: 'SelectComp',
    data() {
        return {
            selected: '',
        }
    },
}
</script>

<style lang="scss" scoped>
@use '../assets/style/general.scss' as *;

select {
    padding: 0.5em;
    margin: 1em 0.5em;
    border-radius: 8px;
}
</style>