/**
* 调试computed api
*/

<script setup lang="ts">
import { ref, computed } from 'vue'
const val = ref(0)
const doubelVal = computed(() => val.value*2)
const changeVal = () => val.value++;
</script>
<template>
  <div>
    <div>curVal {{ val }}</div>
    <div>doubelVal {{ doubelVal }}</div>
    <button @click="changeVal">changeVal</button>
  </div>
</template>