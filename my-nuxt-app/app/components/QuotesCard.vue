<script setup>
defineProps({
  quote: String,
  author: String
})
</script>
<template>
<div class="quote">
     <p>{{ quote }}</p>
    <p class="author">{{ author }}</p>

</div>
   
</template>

<style>
.quote{
    background-color: rgb(157, 154, 150);
    border: 2px solid rgb(168, 166, 166);
    box-shadow: 2px 2px 5px rgba(0, 0, 0, 0.3);
    border-radius: 10px;
    padding: 20px 20px 0;
}
.author{
    text-align: right;
    font-style: italic;
    margin-top: 30px;
    margin: 0;
}
</style>