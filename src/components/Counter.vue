<script setup>
import { useCounterStore } from '../stores/CounterStore';

const counter = useCounterStore();

</script>

<template>
  <div>
    {{ counter.showCount }}
    <button @click="counter.increment">Counter Add</button>
  </div>
</template>