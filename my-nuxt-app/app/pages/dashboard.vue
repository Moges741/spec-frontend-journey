<script setup>
const { data: users, pending, error } = await useFetch('https://jsonplaceholder.typicode.com/users')
</script>

<template>
  <div class="p-6">
    <h1 class="text-2xl font-bold mb-4">User Dashboard</h1>

    <!-- Loading -->
    <p v-if="pending">Loading users...</p>

    <!-- Error -->
    <p v-if="error" class="text-red-500">Failed to load users!</p>

    <!-- Users List -->
    <div v-if="users" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
      <UserCard 
        v-for="user in users" 
        :key="user.id" 
        :name="user.name" 
        :email="user.email" 
      />
    </div>
  </div>
</template>
