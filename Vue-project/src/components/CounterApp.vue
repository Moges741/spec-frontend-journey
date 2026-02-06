<script setup>
import {ref } from 'vue'
const count = ref(0);
const increase = () => {
    count.value++;
}
const decrease = () => { 
    if(count.value > 0) {
        count.value--;
    }
}


</script>
 <template>
    <h5>DAY 4: Counter App</h5>
<div class="counter">
<p>{{ count }}</p>
<div class="btn">
<button class="btn1" @click="decrease" :disabled="count <= 0" >  {{ count <= 0 ? '🚫' : '-' }}</button>
<button class="btn1" @click="increase">+</button> 

</div>
    
</div>


 </template>


<style>
.counter{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 20px;
    margin-top: 20px;
    border: 2px solid #2c2a2a;
    border-radius: 5px;
    padding: 10px ;
    font-size: 50px;
    font-weight: bold;
    /* width: 200px; */
    

}
.btn{
    display: flex;
    gap: 30px;
    justify-content: center;

}
/* disabled */
.inactive {

    color: red;
    cursor: not-allowed;
}
.btn1{
    padding: 10px;
    font-size: 20px;
    border-radius: 5px;
    border: none;
    background-color: #007BFF;
    color: white;
    cursor: pointer;
    width: 50px;
    height: 50px;
}

</style>