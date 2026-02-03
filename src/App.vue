<script setup lang="ts">
import Header from './components/Header.vue'
import HeroSection from './components/HeroSection.vue'
import AboutSection from './components/AboutSection.vue'
import TechSection from './components/TechSection.vue'
import ResultSection from './components/ResultSection.vue'

import { onMounted } from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css'; // 必须引入 CSS 样式，否则元素会永远消失

onMounted(() => {
  AOS.init({
    duration: 1000, // 动画持续时间（毫秒）
    once: false,    // 是否只触发一次，设为 false 则每次滚动到这里都会有动画
    mirror: true,   // 向上滚动时是否也触发动画
    offset: 100     // 距离元素出现在视口多少像素时开始动画
  });
});
</script>

<template>
  <Header />
  <main>
    <HeroSection id="hero" />
    <AboutSection />
    <TechSection id="algorithm" />
    <ResultSection />
  </main>
  <footer class="footer">
    <div class="footer-content">
      <p>© 2026 灵犀智碳小队 - 基于深度学习技术的二氧化碳浓度重建项目</p>
      <div class="footer-links">
        <span>Vue 3 + TypeScript</span>
        <span>深度学习重建技术</span>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  padding: 60px 0;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
  background: #0a0f18;
  color: #475569;
  text-align: center;
}
.footer-content p {
  margin-bottom: 10px;
}
</style>
