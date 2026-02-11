<script setup>
defineProps({
    title: String,
    price: String,
    category: String,
    thumbnail: String,
    brand: String
})
</script>
<template>
    <div class="product">
        <div>
            <img :src="thumbnail" alt="image">
        </div>
      <div>
          <div class="text-center font-bold">
            <p > {{title }}</p>
            <p class="text-green-600">${{ price }}</p>
        </div>
        <div class="brand-category">
            <p>Brand : {{ brand }}</p>
            <p>Category : {{ category }}</p>
        </div>
      </div>
    </div>

</template>

<style>
.product{
    /* background-color: gray; */
    padding: 30px;
    border: none;
    box-shadow: 3px 4px 5px rgba(0, 0, 0, 0.3);
    border-radius: 10px;
}
.brand-category{
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    margin-top: 20px;
    background-color: #d9d7d3;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 3px 4px 5px rgba(0, 0, 0, 0.3);

}

</style>