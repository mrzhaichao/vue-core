/**
* demo - 调试验证data ref props 更细流程
*/

<script setup lang="ts">
import UserInfo from './UserInfo.vue';
import { ref, reactive } from "vue"

const title = ref("Hello World");
const info = reactive({
  name: 'chao',
  age: 18
});

const updateTitle = () => {
  title.value = "Hello Vite"
}

const updateAge = () => {
  info.age = info.age + 1
}

</script>

<template>
  <UserInfo :title="title" :info="info"  />
  <button @click="updateTitle"> 更新title </button>
  <button @click="updateAge"> 更新age </button>
</template>

<style scoped>
</style>
