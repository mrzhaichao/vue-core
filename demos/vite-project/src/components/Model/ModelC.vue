<script setup lang="ts">

defineProps<{modelName: string, modelAge: number|string}>()

const emit = defineEmits(['update:modelName', 'update:modelAge'])

const nameInput = (event: Event) => {
    const value = (event.target as HTMLInputElement).value
    emit('update:modelName', value)
}

const ageInput = (event: Event) => {
    const value = (event.target as HTMLInputElement).value
    emit('update:modelAge', value)
}

</script>
<template>
<input type="text" :value="modelName" @input="nameInput">
<input type="text" :value="modelAge" @input="ageInput">
</template>