/**
* inject 调试
*/
<script setup lang="ts">
import { inject } from 'vue'

const count = inject('count')

</script>
<template>
<div>
    Inject count: {{ count }}
</div>
</template>