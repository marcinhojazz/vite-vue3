<script setup>
import { useCounterStore } from './stores/CounterStore';

const counter = useCounterStore();

</script>

<template>
  <h2>Welcome to pinia</h2>
  <div>
    {{ counter.count }}
    <button @click="counter.increment">Add</button>
  </div>
  
</template>