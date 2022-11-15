<template>
    <div class="container">
        <select>
            <option selected value="">Select category</option>
            <option :value="cat" v-for="(cat, index ) in categoryOpt" :key="index">{{ cat }}
            </option>
        </select>

    </div>

</template>

<script>
export default {
    name: 'SelectComp',
    data() {
        return {
            categoryOpt: [
                'Breaking Bad',
                'Better Call Saul'
            ],
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

    option {
        text-transform: capitalize;
    }
}
</style>