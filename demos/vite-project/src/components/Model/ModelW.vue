<script setup lang="ts">
import { reactive } from 'vue'
import ModelC from './ModelC.vue';

const info = reactive({
    name: 'test',
    age: 1
})
</script>
<template>
    <div>
        name: {{ info.name }}
        age: {{ info.age }}
    </div>
    <ModelC v-model:model-name="info.name" v-model:model-age="info.age" />
</template>