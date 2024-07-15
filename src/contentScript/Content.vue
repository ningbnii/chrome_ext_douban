<!-- src/content/Content.vue -->
<template>
  <!-- tailwindCss:一个按钮，浮动在屏幕右侧，屏幕中间位置 -->
  <div class="fixed right-0 top-1/2 transform -translate-y-1/2">
    <button @click="goToZlib" class="bg-blue-500 text-white px-4 py-2 rounded-full">去下载</button>
  </div>
</template>

<script setup>
let title = ''
try {
  // 获取.article-title的值
  title = document.querySelector('.article-title').textContent.trim()
} catch (error) {
  try {
    title = document.querySelector('.title-wrapper .title').textContent.trim()
  } catch (error) {}
}

const goToZlib = () => {
  // 打开新窗口
  window.open(`https://zh.singlelogin.re/s/${title}?`)
}
</script>

<style></style>
