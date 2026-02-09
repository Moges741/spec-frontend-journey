<script setup>
import { useToggle } from '../composables/useToggle.js'

const { state: showCard, toggle } = useToggle()
</script>

<template>
  <div>
    <button @click="toggle">
      {{ showCard ? "Hide Card" : "Show Card" }}
    </button>

    <div v-if="showCard" class="card">
      <h3>Reusable Toggle Card</h3>
      <p>This card is controlled by useToggle composable.</p>
    </div>
  </div>
</template>

<style>
button {
  padding: 8px 14px;
  margin: 10px 0;
  cursor: pointer;
}

.card {
  border: 1px solid #ccc;
  padding: 15px;
  border-radius: 8px;
}
</style>
