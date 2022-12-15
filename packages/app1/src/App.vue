<script setup lang="ts">
import { defineAsyncComponent } from 'vue';
const RemoteApp = defineAsyncComponent(() => import('app2/App'));
</script>

<template>
  <div class="app1-container">
    <h1>Hello App1</h1>
    <RemoteApp></RemoteApp>
  </div>
</template>

<style lang="scss" scoped>
.app1-container {
  h1 {
    background: green;
  }
}
</style>
