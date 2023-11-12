<template>
    <div>title: {{ title }}</div>
    <div class="user-info">
        <p class="name">name: {{ info.name }}</p>
        <p class="age">age: {{ info.age }}</p>
    </div>
</template>
<script setup lang="ts">
    defineProps<{info: {name: string, age: number}, title: string}>();
</script>