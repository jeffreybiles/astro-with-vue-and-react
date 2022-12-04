<template>
  <div className="vue-component">
    <Hello />
    <div>
      {{count}}
    </div>
    <button @click="() => count = count + 1">
      + 1
    </button>
    <div style="border:1px solid black; padding: 4px;">
      <slot />
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import Hello from './AnotherComponent.vue'

const count = ref(0)
</script>

<style scoped>
.slot {
  border: 1px solid black;
  padding: 4px;
}
</style>