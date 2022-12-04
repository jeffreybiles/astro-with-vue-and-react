<template>
  <div className="vue-component">
    <Hello />
    <div>
      {{$count}}
    </div>
    <button @click="() => count.set($count + 1)">
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

import { count } from '../stores/count'
import { useStore } from '@nanostores/vue'

const $count = useStore(count)
</script>

<style scoped>
.slot {
  border: 1px solid black;
  padding: 4px;
}
</style>