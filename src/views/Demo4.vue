<template>
  <div id="demo4">
      <h2>{{firstname}}</h2>
      <h2>{{lastname}}</h2>
       <h2>{{fullname}}</h2>
  </div>
</template>

<script>
export default {
    name: 'Demo4',
    methods: {
        getrandomno1: function () {
            return Math.random()
        }
    },
    data () {
        return {
            firstname: 'blue',
            lastname: 'baney'
        }
    },
    computed: {
        fullname () {
            return this.firstname + ' ' + this.lastname
        },
        getrandomno () {
            return Math.random()
        }
    }
}
</script>

<style>

</style>
