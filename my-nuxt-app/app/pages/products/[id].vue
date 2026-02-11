<script setup>
const route = useRoute()
const id = route.params.id
const { data: product, pending, error } =
  await useFetch(`https://dummyjson.com/products/${id}`)
</script>

<template>
  <div class="p-6">

    <p v-if="pending">Loading...</p>

    <p v-else-if="error">Error loading product</p>

    <div v-else-if="product">
      <h1 class="text-2xl font-bold">{{ product.title }}</h1>
     <div class="flex">
        <img v-for="image in product.images" :src="image" class="w-64 mt-4" />
     </div>
      <p class="mt-2">{{ product.description }}</p>
      <p class="font-bold mt-2">${{ product.price }}</p>
        <p class="text-sm text-gray-500 mt-1">Brand: {{ product.brand }}</p>          
    </div>

  </div>
</template>
