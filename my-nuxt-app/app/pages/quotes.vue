<script setup>
const { data, pending, error } = await useFetch('https://dummyjson.com/quotes')
</script>

<template>
  <div class="p-6">
    <h1 class="text-2xl font-bold mb-4 text-center">Quotes</h1>

    <!-- Loading -->
    <p v-if="pending" class="text-gray-600 text-center">Loading quotes...</p>

    <!-- Error -->
    <p v-if="error" class="text-red-500 text-center">Failed to fetch quotes!</p>

    <!-- Quotes Grid -->
    <div v-if="data" class=" grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
      <QuotesCard
        v-for="q in data.quotes" 
        :key="q.id" 
        :quote="q.quote" 
        :author="q.author" 
      />
    </div>
  </div>
</template>
