<template>
  <section id="results" class="results-section">
    <div class="container">
      <h2 class="section-title" data-aos="fade-up">研究成果展示</h2>
      
      <div class="stats-grid" data-aos="fade-up">
        <div class="stat-item">
          <span class="stat-value">98.5%</span>
          <span class="stat-label">全球覆盖率</span>
        </div>
        <div class="stat-item">
          <span class="stat-value">< 1.5ppm</span>
          <span class="stat-label">平均重建误差 (RMSE)</span>
        </div>
        <div class="stat-item">
          <span class="stat-value">1° × 1°</span>
          <span class="stat-label">空间分辨率</span>
        </div>
      </div>

      <div class="comparison-grid">
        <div class="img-container" data-aos="fade-right">
          <h4 class="img-caption">原始卫星观测 (ViT)</h4>
          <div class="img-wrapper">
             <img src="../assets/images/vit_sparse_full.png" alt="Raw Data">
          </div>
          <p class="img-desc">受轨道分布和云层遮挡影响，全球观测数据存在严重缺失。</p>
        </div>

        <div class="img-container" data-aos="fade-left">
          <h4 class="img-caption highlighted">CO2-NET 重建结果</h4>
          <div class="img-wrapper highlight-border">
             <img src="../assets/images/co2net_refined_full.png" alt="Reconstructed Data">
          </div>
          <p class="img-desc">模型实现了高时空连续性的全球二氧化碳浓度全覆盖重构。</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* 1. 基础布局与标题 */
.results-section {
  padding: 100px 20px;
  background: #0f172a; 
  overflow: hidden; /* 必须保留：防止 AOS 动画导致页面左右晃动 */
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.section-title {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 60px;
  color: #ffffff; /* 确保标题可见 */
}

/* 2. 数据指标卡片样式 (找回消失的效果) */
.stats-grid {
  display: flex;
  justify-content: space-around;
  margin-bottom: 80px;
  gap: 20px;
}

.stat-item {
  text-align: center;
  flex: 1;
  padding: 30px;
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.05);
  border-radius: 12px;
  transition: all 0.3s ease;
}

.stat-item:hover {
  background: rgba(255, 255, 255, 0.05);
  transform: translateY(-5px);
}

.stat-value {
  display: block;
  font-size: 2.5rem;
  font-weight: 800;
  color: #2ecc71; /* 亮绿色指标 */
  margin-bottom: 10px;
}

.stat-label {
  color: #94a3b8;
  font-size: 1rem;
}

/* 3. 图片对比网格布局 */
.comparison-grid {
  display: flex;
  justify-content: space-between;
  gap: 40px;
  align-items: flex-start;
}

.img-container {
  flex: 1;
  min-width: 0;
  text-align: center;
}

.img-wrapper {
  background: rgba(15, 23, 42, 0.5);
  border-radius: 16px;
  padding: 15px;
  border: 1px solid rgba(255, 255, 255, 0.05);
  margin-bottom: 20px;
  transition: all 0.3s ease;
}

.img-wrapper:hover {
  transform: translateY(-5px);
  border-color: rgba(46, 204, 113, 0.3);
}

.img-wrapper img {
  width: 100%;
  height: auto;
  display: block;
  border-radius: 8px;
}

/* 4. 文字描述与高亮 */
.img-caption {
  font-size: 1.25rem;
  margin-bottom: 15px;
  color: #f8fafc;
}

.highlighted {
  color: #2ecc71 !important;
  font-weight: bold;
}

.highlight-border {
  border: 2px solid #2ecc71;
  box-shadow: 0 0 30px rgba(46, 204, 113, 0.15);
}

.img-desc {
  color: #94a3b8;
  font-size: 0.95rem;
  line-height: 1.6;
  padding: 0 10px;
}

/* 5. 响应式适配 */
@media (max-width: 992px) {
  .stats-grid {
    flex-wrap: wrap;
  }
  .stat-item {
    min-width: 250px;
  }
  .comparison-grid {
    flex-direction: column;
  }
}
</style>