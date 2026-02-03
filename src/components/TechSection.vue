<template>
  <section id="algorithm" class="tech-section">
    <div class="container">
      <h2 class="section-title" data-aos="fade-up">核心技术路线</h2>
      
      <div class="model-intro" data-aos="fade-up">
        <p>
          项目创新性地提出了基于 <strong>ST-UNet (Spatio-Temporal U-Net)</strong> 的二氧化碳浓度重建模型，
          通过融合卫星遥感、地面观测与气象再分析数据，解决了全球 $CO_2$ 数据在时空上的高度稀疏性问题。
        </p>
      </div>

      <div class="tech-grid">
        <div class="tech-card" data-aos="zoom-in" data-aos-delay="100">
          <div class="tech-icon">融合</div>
          <h4>多源数据融合</h4>
          <p>整合 OCO-2 卫星数据、ERA5 气象数据及底图地理信息，构建多维输入特征空间。</p>
        </div>

        <div class="tech-card" data-aos="zoom-in" data-aos-delay="200">
          <div class="tech-icon">架构</div>
          <h4>ST-UNet 建模</h4>
          <p>利用跳跃连接（Skip Connections）捕获多尺度空间特征，并引入时间序列注意力机制。</p>
        </div>

        <div class="tech-card" data-aos="zoom-in" data-aos-delay="300">
          <div class="tech-icon">精度</div>
          <h4>1° 高分辨率</h4>
          <p>实现全球范围内经纬度 1° × 1° 的精细化重建，误差率较传统模型降低 15% 以上。</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.tech-section {
  padding: 100px 20px;
  background: #0a0f18; /* 回到深色背景，形成视觉交替 */
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.section-title {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 40px;
}

.model-intro {
  text-align: center;
  max-width: 800px;
  margin: 0 auto 60px;
  color: #94a3b8;
  font-size: 1.2rem;
  line-height: 1.8;
}

.tech-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
}

.tech-card {
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.05);
  padding: 40px;
  border-radius: 20px;
  text-align: center;
  transition: transform 0.3s ease;
}

.tech-card:hover {
  transform: translateY(-10px);
  background: rgba(46, 204, 113, 0.05);
  border-color: rgba(46, 204, 113, 0.3);
}

.tech-icon {
  width: 60px;
  height: 60px;
  background: #2ecc71;
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 24px;
  font-weight: bold;
  color: #fff;
}

.tech-card h4 {
  font-size: 1.4rem;
  margin-bottom: 16px;
  color: #fff;
}

.tech-card p {
  color: #94a3b8;
  font-size: 1rem;
  line-height: 1.6;
}
</style>