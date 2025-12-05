<script setup lang="ts">
import {  ref } from 'vue';
const appDesc = ref(import.meta.env.VITE_APP_DESC || '')
</script>

<template>
  <div class="w-full rounded-2xl z-10 p-5 text-center">
    <el-text>{{ appDesc }}  © 2024 <a href="https://beian.miit.gov.cn/" target="_blank" class="text-blue-700">苏ICP备16049927号</a></el-text>
  </div>
</template>

<style scoped>

</style>
