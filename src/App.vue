<template>
  <div id="app">
   <Header/>
    <Content/>
   <Footer @onClock="onClock" title="Copyright 2021 by Blue Baney Ltd." color="red"/>
    <div class="clock">{{time}}</div>
 </div>
</template>

<script>
import Header from '@/components/layout/Header'
import Footer from '@/components/layout/Footer'
import Content from '@/components/layout/Content'
import moment from 'moment'

export default {
  name: 'app',
  methods: {
      onClock (value) {
        this.time = moment(value).format('MM/DD/YYYY hh:mm:ss')
      }
  },
  data () {
      return {
          time: ''
      }
  },
  components: {
      Header,
      Footer,
      Content
  }
}
</script>

<style scoped>
.content{
    color:violet;
}
.clock{
    font-size: 12px;
}

</style>
