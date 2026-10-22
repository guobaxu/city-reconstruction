# CityGaussian（V1）

[论文列表](README.md) · [数据集列表](../datasets/README.md)

- **完整标题**：CityGaussian: Real-time High-quality Large-Scale Scene Rendering with Gaussians
- **会议**：ECCV 2024（官方仓库标注）
- **论文**：[arXiv:2404.01133](https://arxiv.org/abs/2404.01133)
- **项目页**：[CityGaussian](https://dekuliutesla.github.io/citygs/)
- **代码**：[官方仓库](https://github.com/Linketic/CityGaussian)；原始实现见 [V1-Original 分支](https://github.com/Linketic/CityGaussian/tree/V1-Original)
- **标签**：大规模场景重建、3DGS、分块训练、LoD、新视角合成
- **状态**：已核查摘要与实验数据设置；未复现
- **核查日期**：2026-10-22

## 研究笔记

通过全局高斯先验、分块优化和数据选择扩展场景规模，再用多层细节表示支持实时渲染。后续精读重点：块划分与融合、训练视图分配、不同观察尺度下的质量和速度。

## 使用的数据集

| 数据集 | 实验范围 | 用途 / 设置 | 证据 |
|---|---|---|---|
| [MatrixCity](../datasets/matrixcity.md) | Small City 全城航拍；另测街景 Block_A | 图像质量与速度；航拍图像宽度调至 1600 | 论文 §4.1 |
| [Mill19](../datasets/mill19.md) | Building、Rubble | 真实场景渲染；图像下采样 4 倍 | 论文 §4.1；Mega-NeRF 场景归属 |
| [UrbanScene3D](../datasets/urbanscene3d.md) | Residence、Sci-Art | 真实场景渲染；图像下采样 4 倍 | 论文 §4.1；仓库指定 V1 |

主要记录的评估维度：PSNR、SSIM、LPIPS、FPS。

## 版本边界

当前 main 同时承载 V2 及后续更新。main 中出现 GauU-Scene 不表示 V1 原论文使用了它；V2 中将 CityGS 作为基线的实验也不自动记入 V1 原论文的数据列表。

## 来源

- [论文 §4.1，arXiv v3](https://arxiv.org/html/2404.01133v3)
- [官方仓库版本说明](https://github.com/Linketic/CityGaussian)
- [Mega-NeRF 数据说明](https://github.com/cmusatyalab/mega-nerf#data)
- [当前仓库数据准备说明](https://github.com/Linketic/CityGaussian/blob/main/doc/data_preparation.md)
