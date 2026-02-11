<script setup>
const { data, pending, error } = await useFetch(
  'https://dummyjson.com/quotes'
)
</script>

<template>
  <div class="p-6">
    <h1 class="text-2xl font-bold mb-6">Quotes</h1>

    <div v-if="pending">Loading...</div>
    <div v-else-if="error">Error loading quotes</div>

    <div v-else class=" grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
      <NuxtLink
        v-for="q in data.quotes"
        :key="q.id"
        :to="`/quotes/${q.id}`"
      >
        <QuotesCard
        :quote="q.quote" 
        :author="q.author" 
      />
      </NuxtLink>
    </div>
  </div>
</template>
