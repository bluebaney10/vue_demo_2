<template>
  <div id="app">
    <h1>{{title}}</h1>
    <h2>{{count}}</h2>
    <button @click="onClickAdd">Add</button>
  </div>
</template>
<script>
export default {
  name: 'blue',
  data () {
    return {
      title: 'BLUE BANEY',
      count: 0
    }
  },
  methods: {
      onClickAdd(){
       this.count = this.count + 1;
      }
  }
}
</script>