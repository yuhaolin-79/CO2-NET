<template>
  <section class="hero-container">
    <div class="background-overlay"></div>

    <div class="content" data-aos="fade-up">
      <div class="badge">
        <component :is="Leaf" :size="16" class="icon" />
        <span>灵犀智碳小队 · 2026 科技创新项目</span>
      </div>
      
      <h1 class="title">
        基于深度学习的<br />
        <span class="gradient-text">二氧化碳全球浓度重建</span>
      </h1>
      
      <p class="description">
        利用高时空分辨率深度学习模型，融合多源遥感数据，
        实现全球尺度下的 CO<sub>2</sub> 浓度高精度重构，助力全球碳中和决策。
      </p>

      <div class="actions">
        <button class="btn-primary" @click="scrollDown">
          探索技术细节
        </button>
        <button class="btn-outline">
          查看研究文档
        </button>
      </div>
    </div>

    <div class="scroll-indicator">
      <component :is="ChevronDown" class="mouse-icon" />
    </div>
  </section>
</template>

<script setup>
import { Leaf, ChevronDown } from 'lucide-vue-next';
import { onMounted } from 'vue';
import AOS from 'aos';
import 'aos/dist/aos.css';

onMounted(() => {
  AOS.init({ duration: 1000 });
});

const scrollDown = () => {
  window.scrollTo({ top: window.innerHeight, behavior: 'smooth' });
};
</script>

<style scoped>
.hero-container {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  background-color: #0a0f18; /* 深色科技底色 */
  color: #fff;
  overflow: hidden;
  text-align: center;
}

.background-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: radial-gradient(circle at center, rgba(46, 204, 113, 0.15) 0%, transparent 70%);
  z-index: 1;
}

.content {
  z-index: 2;
  max-width: 800px;
  padding: 0 20px;
}

.badge {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  background: rgba(255, 255, 255, 0.1);
  padding: 8px 16px;
  border-radius: 20px;
  font-size: 14px;
  margin-bottom: 24px;
  border: 1px solid rgba(255, 255, 255, 0.1);
}

.title {
  font-size: 3.5rem;
  font-weight: 800;
  line-height: 1.2;
  margin-bottom: 24px;
}

.gradient-text {
  background: linear-gradient(90deg, #2ecc71, #27ae60);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.description {
  font-size: 1.2rem;
  color: #cbd5e1;
  margin-bottom: 40px;
  line-height: 1.6;
}

.actions {
  display: flex;
  gap: 16px;
  justify-content: center;
}

.btn-primary {
  background: #2ecc71;
  color: #fff;
  border: none;
  padding: 12px 32px;
  border-radius: 8px;
  font-weight: 600;
  cursor: pointer;
  transition: transform 0.2s;
}

.btn-primary:hover {
  transform: translateY(-2px);
  background: #27ae60;
}

.btn-outline {
  background: transparent;
  border: 1px solid #fff;
  color: #fff;
  padding: 12px 32px;
  border-radius: 8px;
  cursor: pointer;
}

.scroll-indicator {
  position: absolute;
  bottom: 30px;
  animation: bounce 2s infinite;
}

@keyframes bounce {
  0%, 20%, 50%, 80%, 100% {transform: translateY(0);}
  40% {transform: translateY(-10px);}
  60% {transform: translateY(-5px);}
}
</style>