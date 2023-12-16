/**
* provide 源码解析 debug
*/
<script setup lang="ts">
import { ref, provide } from 'vue'
import Center from './Center.vue'

const count = ref(0)
const changeCount = () => count.value++

provide('count', count)

</script>
<template>
  <div>
    provide
  </div>
  <Center />
  <button @click="changeCount">Change Count</button>
</template>