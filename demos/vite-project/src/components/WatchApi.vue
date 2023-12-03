/**
* watch api 调试 
*/
<script setup lang='ts'>
import { ref, watch, reactive } from 'vue'

const val = ref(0);
const valChange = () => val.value++;

const info = reactive({
  a: {
    b: 1,
    c: 2
  },
  d: 1
})

const changeInfo = () => {
  info.a.b++;
}

watch(info, (val) => {
  console.log('watch:reactive', val)
})

watch([info, val], (arr) => {
  console.log('watch:array', arr, arr[0].d)
})

// watch(val, (newVal, oldVal) => {
//   console.log('watch:ref', val.value, newVal, oldVal)
// })

// watch(() => {
//   return val.value
// }, (val, prev) => {
//   console.log('watch:fn', val, prev)
// })

// watch(val, (newVal, oldVal) => {
//   console.log('watch:ref:post', val.value, newVal, oldVal)
// }, {flush: 'post'})

// watch(val, (val) => {
//   console.log('watch:ref:immediate', val)
// }, {
//   immediate: true
// })

</script>
<template>
  <div>{{ val }}</div>
  <button @click="valChange">change val</button>
  <div>
    info.a.b: {{ info.a.b }}
  </div>
  <button @click="changeInfo">change info</button>
</template>