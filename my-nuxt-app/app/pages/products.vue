<script setup>

const {data, pending, error} = useFetch('https://dummyjson.com/products')
</script>

<template>
    <h2 class="text-center font-bold mb-4 mt-4">Products</h2>

    <p v-if="pending" class="text-gray-500">waiting to fetch data</p>
    <p>failed fetch data</p>





</template>