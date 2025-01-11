<script setup>
import { ref } from 'vue'

let counter = ref(0)

function increment() {
  counter.value++
}

function decrement() {
  counter.value--
}
</script>

<template>
  <div>
    <h1>{{ counter }}</h1>
    <button @click="increment">+</button>
    <button @click="decrement">-</button>
  </div>
</template>

<style scoped></style>
