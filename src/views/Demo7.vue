<template>
<div id="demo7">
    <Clock>
     <span style="color:red;">เวลาปัจจุบัน :</span>
    </Clock>
    <Clock>
     <span style="color:green;">Current time :</span>
    </Clock>
    <Clock>
   </Clock>

     <Clock>
         <span style="color:orange;">Current time :</span>
         <template v-slot:header>
             <h1>Header</h1>
         </template>
         <template v-slot:footer>
            <h3>footer</h3>
         </template>
    </Clock>
</div>
</template>

<script>
import Clock from '@/components/helpers/Clock'

export default {
    name: 'Demo7',
    components: {
        Clock
    }
}
</script>

<style>

</style>
