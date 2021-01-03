<template>
  <div>
      <h1>Event & Methods</h1>
      <button v-on:click="clickMe">clickMe</button>
      <button v-on:click="clickMe2('hello vue')">clickMe2</button>
      <button @click="clickMe3('hello blue')">clickMe3</button>
      <h3>{{getTimeStamp()}}</h3>
  </div>
</template>

<script>
export default {
    name: 'demo2',
    mounted () {
        this.initial()
    },
    methods: {
        clickMe () {
            alert('hi')
        },
          clickMe2 (message) {
            alert(message)
        },
          clickMe3 (message) {
            alert(message)
        },
        getTimeStamp () {
            return Date()
        },
        initial () {
            console.log('init function')
        }
    }
}
</script>

<style>

</style>
