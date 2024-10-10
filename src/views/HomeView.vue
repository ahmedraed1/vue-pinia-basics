<template>
  <main>
    <h1>Home</h1>
    <div>
      <p>Counter: {{ count }}</p>
      <p>Double counter: {{ doubleCount }}</p>
      <button @click="increment">Increment</button>
    </div>
  </main>
</template>
<script setup>
import { computed } from 'vue'

// getting the store
// vue-pinia-basics/src/stores/counter.js
import { useCounterStore } from '@/stores/counter'

// using the store
const store = useCounterStore()
const count = computed(() => store.count)
const doubleCount = computed(() => store.doubleCount)
const increment = () => store.increment();
</script>