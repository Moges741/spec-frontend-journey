<script setup>
const props = defineProps({
    name: String,
    role: String,
    status: String
})
const emit = defineEmits(['view-profile']);
const handleClick = () => {
    emit('view-profile', props.name);

}
</script>


<template>
    <div class="card" :class="status ==='online'? 'online-card': 'offline-card' ">
        <strong>Name : {{ name }}</strong>
         <p>Role : {{ role }}</p>
         <p v-if="status === 'online'">🟢 Online</p>
         <p v-else>🔴 Offline</p>
         <button class="view-btn" @click="handleClick">View Profile</button>

    </div>

</template>

<style>
.card{
  border: 1px solid #448c83;
  padding: 12px;
  margin: 12px;
  border-radius: 8px;
  box-shadow: 3px 3px 7px rgba(54, 146, 136, 0.1);
  transition: 0.3s;
}

.card strong{
  margin: 0;
  font-size: 18px;
}

.card p{
  margin: 5px 0 0;
  font-size: 15px;
  color: #6c6a6a;
}
.online-card {
  border-color: #22c55e;
  box-shadow: 0 0 8px rgba(34, 197, 94, 0.3);
}

.offline-card {
  border-color: #ef4444;
  box-shadow: 0 0 8px rgba(239, 68, 68, 0.25);
}

/* Button */
.view-btn{
  margin-top: 10px;
  padding: 6px 12px;
  border: none;
  background: #448c83;
  color: white;
  border-radius: 5px;
  cursor: pointer;
}

.view-btn:hover{
  opacity: 0.9;
}
</style>