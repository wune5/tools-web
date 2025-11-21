<script setup lang="ts">
import { ref } from 'vue';
const appDesc = ref(import.meta.env.VITE_APP_DESC || '')
</script>

<template>
  <div class="w-full rounded-2xl z-10 p-5 text-center">
    <!-- 原有描述信息 -->
    <el-text v-if="appDesc" class="block mb-2">{{ appDesc }}</el-text>
    <!-- 版权声明和备案号 -->
    <div class="space-y-1"> <!-- 使用 Tailwind 的 space-y-1 创建垂直间距 -->
      <p class="text-sm text-gray-600 dark:text-gray-300">
        &copy; 2025 Your Company/Organization Name. All rights reserved.
      </p>
      <p class="text-xs text-gray-500 dark:text-gray-400">
        备案号：
        <a
          href="https://beian.miit.gov.cn/"
          target="_blank"
          rel="noopener noreferrer"
          class="text-blue-600 hover:underline dark:text-blue-400"
        >
          Your ICP Number
        </a>
      </p>
    </div>
    <!-- 如果你还想保留原有的 Tools-Web 链接，可以取消下面的注释 -->
    <!--
    <el-text class="block mt-2">
      © 2025
      <a href="https://github.com/naroat/tools-web" target="_blank" class="text-blue-700">Tools-Web</a>
    </el-text>
    -->
  </div>
</template>

<style scoped>
/* 如果不使用 Tailwind CSS，可以添加如下 CSS */
/*
.space-y-1 > * + * {
  margin-top: 0.25rem; /* 0.25rem 等于 Tailwind 的 space-y-1 */
}
*/
</style>
