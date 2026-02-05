<script setup>
defineProps({
    name: String,
    role: String
})

</script>


<template>
    <div class="card">
        <strong>Name : {{ name }}</strong>
         <p>Role : {{ role }}</p>
    </div>

</template>

<style>
.card{
    border: 1px solid #448c83;
    padding: 10px;
    margin: 10px;
    border-radius: 5px;
    box-shadow: 3px 3px 7px rgba(54, 146, 136, 0.1);
}
.card strong{
    margin: 0;
    font-size: 18px;
}
.card p{
    margin: 5px 0 0;
    font-size: 15px;
    color: #6c6a6a;
}
</style>