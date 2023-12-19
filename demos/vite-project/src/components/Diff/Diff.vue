<script setup lang="ts">
import { ref } from 'vue'

const arr = ref([
    {
        id: 0,
        name: 0
    },
    {
        id: 1,
        name: 1
    },
    {
        id: 2,
        name: 2
    },
    {
        id: 3,
        name: 3
    },
])

let initLength = 4

const addItem = () => {
    arr.value.push({
        id: initLength,
        name: initLength
    })
    initLength++;
}

const removeItem = () => {
    const index = (Math.random() * arr.value.length) | 0;
    arr.value.splice(index, 1);
}

const shuffle = () => {
    arr.value.sort(() => Math.random() - 0.5)
}

</script>
<template>
<div class="container">
    <div v-for="item in arr"
        :key="item.id"
    >
        {{ item.name }}
    </div>
</div>
<div class="btns">
    <button @click="addItem">add item</button>
    <button @click="removeItem">remove item</button>
    <button @click="shuffle">shuffle item</button>
</div>
</template>