<template>
    <select id="select">
        <option value="volvo">Alive</option>
        <option value="saab">Deceased</option>
        <option value="opel">Presumed dead</option>
    </select>
    <div class="p-5">
        prova
    </div>
</template>

<script>
export default {
    name: 'SelectComp',
}
</script>

<style lang="scss" scoped>
select {
    margin: 2em;
}
</style>