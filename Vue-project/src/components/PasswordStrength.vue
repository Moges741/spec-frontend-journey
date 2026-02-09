<script setup>
import { ref, watch } from 'vue'

const password = ref('')
const strength = ref('')
watch(password, (newPassword) => {

  if (newPassword.length < 6) {
    strength.value = 'Weak'
    return
  }
  const hasNumber = /\d/.test(newPassword)
  const hasSymbol = /[!@#$%^&*(),.?":{}|<>]/.test(newPassword)
  if (hasNumber && hasSymbol) {
    strength.value = 'Strong'
  } else {
    strength.value = 'Medium'
  }

})
</script>

<template>
  <div class="container">
    <h2>Password Strength Checker</h2>

    <input
      v-model="password"
      type="password"
      placeholder="Enter password"
    />

    <p v-if="password">
      Strength:
      <strong :class="strength">
        {{ strength }}
      </strong>
    </p>
  </div>
</template>

<style>
.container {
  max-width: 400px;
  margin: auto;
  padding: 20px;
}

input {
  width: 100%;
  padding: 10px;
  margin-top: 10px;
}

.Weak { color: red; }
.Medium { color: orange; }
.Strong { color: green; }
</style>
