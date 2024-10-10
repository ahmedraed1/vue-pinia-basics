<template>
  <div class="about">
    <h1>This is an about page</h1>
    <h3>This is from Pinia store</h3>
    <p>Counter: {{ count }}</p>
    <p>Double counter: {{ doubleCount }}</p>
  </div>
</template>

<script setup>
import { useCounterStore } from '@/stores/counter'
import { computed } from 'vue';


const store = useCounterStore()
const count = computed(() => store.count)
const doubleCount = computed(() => store.doubleCount)
</script>

<style>
</style>
