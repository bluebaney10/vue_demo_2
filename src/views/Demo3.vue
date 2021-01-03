<template>
  <div>
      <h1>Data</h1>
      <button @click="count++; isLogged=true;">Count ++</button>
      <div>{{count}}</div>
      <div>{{message}}</div>
      <input type="text" placeholder="start input" v-model="message">
      <h2 v-if="isLogged">Ya Blue</h2>
      <div>{{account}}</div>
      <div>{{courses[0]}}</div>
      <ul><li v-for="(item, index) in courses" :key="index">{{index+1}}. {{item}}</li>
      </ul>

  </div>
</template>

<script>
export default {
    name: 'Demo3',
    mounted () {
        this.message = 'Hello Blue'
    },
    data () {
        return {
          count: 0,
          message: '',
          isLogged: false,
          account: {
              username: 'admin',
              password: '1234'
          },
          courses: [
              'angular',
              'react'
          ]
        }
    }
}
</script>

<style>
li{
    color:red;
    list-style: none;
}
</style>
