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
  title.value = 'test';
  console.log('title', title, title.value)
}

const updateAge = () => {
  info.age = info.age + 1
  console.log('info.age', info.age)
}

const updateAgeAndTitle = () => {
  // debug: 组件更新时排序
  info.age = info.age + 1;
  title.value = 'test2'
}

</script>

<template>
  <UserInfo :title="title" :info="info"  />
  <button @click="updateTitle"> 更新title </button>
  <button @click="updateAge"> 更新age </button>
  <button @click="updateAgeAndTitle"> 组件更新时排序 </button>
</template>

<style scoped>
</style>
