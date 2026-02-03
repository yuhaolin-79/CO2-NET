<template>
  <nav :class="{ 'nav-scrolled': isScrolled }">
    <div class="nav-content">
      <div class="logo">灵犀智碳</div>
      <div class="menu">
        <a href="#hero">首页</a>
        <a href="#background">项目背景</a>
        <a href="#algorithm">核心技术</a>
        <a href="#results">研究成果</a>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const isScrolled = ref(false);
const handleScroll = () => {
  isScrolled.value = window.scrollY > 50;
};

onMounted(() => window.addEventListener('scroll', handleScroll));
onUnmounted(() => window.removeEventListener('scroll', handleScroll));
</script>

<style scoped>
nav {
  position: fixed;
  top: 0;
  width: 100%;
  padding: 20px 0;
  z-index: 1000;
  transition: all 0.3s ease;
}
.nav-scrolled {
  background: rgba(10, 15, 24, 0.8);
  backdrop-filter: blur(10px);
  padding: 15px 0;
  border-bottom: 1px solid rgba(255, 255, 255, 0.1);
}
.nav-content {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 40px;
}
.logo {
  font-size: 1.5rem;
  font-weight: bold;
  background: linear-gradient(90deg, #2ecc71, #27ae60);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.menu a {
  margin-left: 30px;
  color: #fff;
  opacity: 0.8;
  transition: opacity 0.3s;
}
.menu a:hover {
  opacity: 1;
  color: #2ecc71;
}
</style>