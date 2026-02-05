<script setup>
import UserCard from './components/UserCard.vue';
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

    <p>DAY 3 : Component and Props</p>
    <div class="userCard">
    <UserCard name="Beka" role="Developer"/>
    <UserCard name="Abel" role="Designer"/>
    <UserCard name="Daniel" role="Manager"/>
    </div>

  </div>
</template>

<style scoped>
.userCard{
  display: flex;
  gap: 10px;

}
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
