<script setup>
import {ref} from 'vue';
const name = ref('');
const club = ref("SPEC");
         
         
</script> 

<template>
  <div>
    <p>DAY 1: getting started</p>
    <h1>Hello SPEC Developers </h1>
    <p>DAY 2 : Interpolation and Input binding </p>
    
    <h4>This is from {{ club }}</h4>
    <input v-model="name" placeholder="write Ur name"/>
    <h2 v-if="name !== ''">Hello {{ name }}!</h2>


    
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
