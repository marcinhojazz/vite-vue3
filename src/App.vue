<script setup>
import Counter from './components/Counter.vue'
import TimeLine from './components/TimeLine.vue'
</script>

<template>
  <div>
    <div>
      <h2>Pinia + Composition API</h2>
      <Counter />
    </div>
    <div>
      <h2>Timeline Component DeviX'</h2>
      <TimeLine /> 
    </div>
  </div>
  
</template>

<style>
div {
  display: grid;

  gap: 22px;
}
</style>