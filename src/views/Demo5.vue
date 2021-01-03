<template>
  <div id="demo5">
      <img v-bind:src="imageUrl" v-bind:height="height">
      <a :href="link">blue</a>
      <div :class="error">Error</div>
      <div :class="[error,important]">Error</div>
      <div :class="[false ? error : '',important]">Error</div>
      <div :style="{color,fontSize}">Binding styles</div>
      <div :style="{color:colors}">Binding styles</div>
      <div :style="styleObject">Binding styles Object</div>
      <button @click="isActive=!isActive">Active Style</button>
     <div :style="isActive ? styleObject : '' ">Binding styles Object</div>
  </div>
</template>

<script>
export default {
    name: 'demo5',
    data () {
        return {
            imageUrl: 'https://images.daznservices.com/di/library/GOAL/67/ed/thomas-partey-arsenal-2020_1a1h8hhdz7xw611hds7hueajs4.jpg?t=2129690261&quality=60&w=600',
            height: 100,
            link: '#',
            error: 'errorTxt',
            important: 'important',
            color: 'green',
            fontSize: '30px',
            colors: 'blue',
            styleObject: {
                backgroundColor: 'yellow',
                color: 'green'
            },
            isActive: false
        }
    }
}
</script>

<style>
.errorTxt{
    color:red;
}
.important{
    font-weight: 900;
}
</style>
