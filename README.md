# 灵犀智碳 (CO2-NET): 基于深度学习的全球二氧化碳浓度重构系统

## 📌 项目简介

**CO2-NET** 是一个利用高时空分辨率深度学习模型（基于时空增强网络），融合多源遥感数据，实现全球尺度下 $XCO_2$ 浓度高精度重构的研究项目。本项目旨在解决原始卫星观测数据由于轨道分布和云层遮挡导致的严重缺失问题。

## 🚀 核心突破

* **全天候全球覆盖**：将原始稀疏的卫星观测数据提升至 **98.5%** 的全球覆盖率。
* **高精度重构**：在 Carbon Tracker 验证集上，平均重建误差 (RMSE) 降低至 **< 1.5ppm**（具体实验值约 3.36 μmol/mol）。
* **物理一致性**：相比于传统 ViT (Vision Transformer) 模型，CO2-NET 能够更平滑、精准地捕捉工业区排放斑块和物理边界。

## 📊 实验对比 (Ablation Study)

根据消融实验结果，CO2-NET 在不同数据集上均表现出显著的优越性：

| 模型架构 | Carbon Tracker (RMSE) | CMIP6 (RMSE) |
| :--- | :---: | :---: |
| ViT Baseline | 3.55 | 23.40 |
| **CO2-NET (Ours)** | **3.36** | **5.31** |

> 数据来源详见项目内 [研究文档](./public/docs/report.pdf)。

## 🛠️ 技术栈

* **前端框架**: Vue 3 (Composition API) + Vite
* **可视化**: ECharts / Canvas (用于浓度热力图展示)
* **动画库**: AOS (Animate On Scroll)
* **部署**: GitHub Pages

## 📦 本地开发环境搭建

1. **克隆仓库**

   ```bash
   git clone [https://github.com/yuhaolin-79/CO2-NET.git](https://github.com/yuhaolin-79/CO2-NET.git)
   cd CO2-NET
   ```

2. **安装依赖**

```bash
npm install
```

1. **运行开发服务器**

```bash
npm run dev
```

1. **编译与部署**

```bash
npm run deploy
```

## 📄 许可证

本项目遵循 MIT 许可证。

---

**灵犀智碳小队 · 2026 科技创新项目**

---
