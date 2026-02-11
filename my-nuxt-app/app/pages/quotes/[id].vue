<script setup>
const {id} = useRoute().params

const { data, pending, error } = await useFetch(
  `https://dummyjson.com/quotes/${id}`
)
</script>

<template>
  <div class="p-6">
    <NuxtLink
      to="/quotes"
      class="text-blue-500 underline mb-4 inline-block"
    >
      ← Back
    </NuxtLink>

    <div v-if="pending">Loading quote...</div>
    <div v-else-if="error">Error loading quote</div>

    <div v-else class="border p-6 rounded shadow">
      <p class="text-xl font-semibold mb-2">
        "{{ data.quote }}"
      </p>

      <p class="text-gray-500">
        — {{ data.author }}
      </p>

      <p class="text-sm mt-2 text-gray-400">
        Quote ID: {{ data.id }}
      </p>
    </div>
  </div>
</template>
