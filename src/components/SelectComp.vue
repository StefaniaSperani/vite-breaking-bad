<template>
    <select id="select">
        <option value="volvo">Alive</option>
        <option value="saab">Deceased</option>
        <option value="opel">Presumed dead</option>
    </select>
</template>

<script>
export default {
    name: 'SelectComp',
}
</script>

<style lang="scss" scoped>
@use '../assets/style/general.scss' as *;

.select {
    margin: 2em;
}
</style>