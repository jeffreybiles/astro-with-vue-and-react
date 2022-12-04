<template>
  <div className="vue-component">
    <div>
      {{count}}
    </div>
    <button @click="() => count = count + 1">
      + 1
    </button>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const count = ref(0)
</script>

<style scoped>

</style>