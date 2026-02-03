<template>
  <section id="background" class="section">
    <div class="container" data-aos="fade-up">
      <h2 class="section-title">研究背景与意义</h2>
      
      <div class="grid">
        <div class="card shadow-green">
          <h3>研究背景</h3>
          <p>
            由于卫星轨道限制及大气云层干扰，现有的 $CO_2$ 观测数据存在严重的<strong>时空缺失</strong>。
            全球仅有不到 2% 的区域拥有连续的地面站监测，这极大地限制了我们对全球碳源、碳汇分布的精准认知。
          </p>
        </div>

        <div class="card shadow-blue">
          <h3>科学意义</h3>
          <p>
            本项目通过深度学习算法，实现了全球尺度下 1° 精度的数据重建。
            这不仅填补了卫星观测的空白，更为<strong>碳中和目标</strong>的评估、国际减排协议的履行提供了不可或缺的数据底座。
          </p>
        </div>
      </div>
    </div>
  </section>
</template>


<style scoped>
.section {
  padding: 100px 20px;
  background: #0f172a; /* 稍浅一点的深色，增加层级感 */
}
.container {
  max-width: 1200px;
  margin: 0 auto;
}
.section-title {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 60px;
}
.grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
}
.card {
  background: rgba(255, 255, 255, 0.05);
  padding: 40px;
  border-radius: 16px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1); /* 平滑过渡 */
}
.card h3 {
  color: #2ecc71;
  margin-bottom: 20px;
  font-size: 1.5rem;
}
.card p {
  line-height: 1.8;
  color: #94a3b8;
}
/* 研究背景 - 绿色光圈 */
.shadow-green:hover {
  border-color: #2ecc71;
  box-shadow: 0 0 30px rgba(46, 204, 113, 0.2);
}
/* 科学意义 - 蓝色光圈（修复这里！） */
.shadow-blue:hover {
  border-color: #3498db; /* 蓝色边框 */
  box-shadow: 0 0 30px rgba(52, 152, 219, 0.3); /* 蓝色光圈 */
  transform: translateY(-5px);
}
</style>