<script setup>
import UserCard from './components/UserCard.vue';
import CounterApp from './components/CounterApp.vue';
import More from './components/More.vue';
import PasswordStrength from './components/PasswordStrength.vue';
import {ref} from 'vue';
const name = ref('');
const club = ref("SPEC");
const handleProfileView = (name) => {
  alert(`Viewing profile of ${name}`);
}
        // practice
        const message = ref('Hello Vue 3!');  
        const isInPool = ref(true);
        const handlePool = () =>{
          isInPool.value = !isInPool.value;
        }
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
    <UserCard name="Beka" role="Developer" status="online" @view-profile="handleProfileView"/>
    <UserCard name="Abel" role="Designer" status="offline" @view-profile="handleProfileView"/>
    <UserCard name="Daniel" role="Manager" status="online" @view-profile="handleProfileView"/>
    </div>

  </div>


  <div>
    <h2>Practice</h2>
    <input type="text" v-model="message" placeholder="write">
    <p>{{ message }}</p>

    <p v-if="isInPool">It is in Pool ....</p>
    <p v-if="!isInPool">jump into pool ....</p>
    <button @click="handlePool">{{isInPool ? "in pool" : "jump"}}</button>
  </div>

<CounterApp/>
<More/>
<PasswordStrength />
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
