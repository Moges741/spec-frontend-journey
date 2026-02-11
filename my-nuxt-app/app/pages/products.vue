<script setup>
import ProductCard from '~/components/productCard.vue';


const {data, pending, error} = useFetch('https://dummyjson.com/products')
</script>

<template>
    <h2 class="text-center font-bold mb-4 mt-4">Products</h2>

    <p v-if="pending" class="text-gray-500 text-center">waiting for fetch products</p>
    <p v-if="error" class="text-center text-red-500">failed to fetch products</p>
<div v-if="data" class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 ml-2 mr-2 gap-4">
    <ProductCard
    v-for="p in data.products"
    :title="p.title"
    :price="p.price"
    :category="p.category"
    :thumbnail="p.thumbnail"
    :brand="p.brand"
    />
</div>




</template>