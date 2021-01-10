<template>
    <div id="demo12">
        <h1 ref="title">Waitting for chang by Ref</h1>
        <input
        ref="input1"
        type="text"
        placeholder="This will be focused automatically"
        />
    </div>
</template>

<script>
export default {
    name: 'demo12',
    mounted () {
       // this.$refs.title.textContent = 'Blue change Ref'
        // this.$refs.input1.focus()
        this.$refs.input1.value = '12345...'
    }
}
</script>

<style>

</style>
