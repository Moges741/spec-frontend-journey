<script setup>
defineProps({
  name: String,
  email: String
})
</script>

<template>
  <div class="p-4 border rounded shadow hover:bg-gray-50">
    <h2 class="font-bold text-lg">{{ name }}</h2>
    <p class="text-gray-600">{{ email }}</p>
  </div>
</template>
