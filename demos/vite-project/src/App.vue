<script setup lang="ts">
import RefPropUpdate from './components/RefPropUpdate.vue';
import Computed from './components/Computed.vue';
import WatchApi from './components/WatchApi.vue';
import Provide from './components/Provide/Provide.vue'
import ModelW from './components/Model/ModelW.vue'
</script>

<template>
  <!-- <RefPropUpdate />
  <Computed />
  <WatchApi /> -->
  <!-- <Provide /> -->
  <ModelW />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>