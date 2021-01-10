<template>
    <div id="demo13">
        <h2>{{ 1234 | currency('THB')}}</h2>
        <h2>{{ 2000000000 | bytes}}</h2>
        <h2>{{ 'bluebaney' | capitalize({onlyFirstLetter: true}) }}</h2>
        <h2>{{ 'bluebaney' | uppercase}}</h2>
        <h2>{{ [1,2,3] | reverseArray}}</h2>
    </div>
</template>

<script>
export default {
    name: 'demo13',
    filters: {
        reverseArray (value) {
            return value.slice().reverse()
        }
    }
}
</script>

<style>

</style>
