# CityGaussianV2

[论文列表](README.md) · [数据集列表](../datasets/README.md)

- **完整标题**：CityGaussianV2: Efficient and Geometrically Accurate Reconstruction for Large-Scale Scenes
- **会议**：ICLR 2025
- **论文**：[arXiv:2411.00771](https://arxiv.org/abs/2411.00771)
- **项目页**：[CityGaussianV2](https://dekuliutesla.github.io/CityGaussianV2/)
- **代码**：[官方仓库](https://github.com/Linketic/CityGaussian)
- **标签**：大规模场景重建、2DGS、几何重建、并行训练、压缩
- **状态**：已核查摘要与实验数据设置；未复现
- **核查日期**：2026-10-22

## 研究笔记

基于 2DGS 改善大场景表面重建与训练效率，调整增密机制并优化并行训练流程。后续精读重点：几何质量和渲染质量的权衡、几何评估裁剪与对齐、显存及模型规模。

## 使用的数据集

| 数据集 | 论文中的范围 | 用途 | 证据 |
|---|---|---|---|
| [MatrixCity](../datasets/matrixcity.md) | 航拍、街景 | 渲染与几何评估 | 论文 §5.1 |
| [GauU-Scene](../datasets/gauu-scene.md) | Residence、Russian Building、Modern Building | 渲染与几何评估 | 论文 §5.1、附录表 5–6 |

关注指标：PSNR、SSIM、LPIPS，以及几何 Precision、Recall、F1；效率指标包括训练时间、显存、模型大小等。

## 论文与仓库差异

当前 README 的 GauU-Scene 结果名称为 LFLS、SMBU、Upper Campus。这里保留论文的原始命名；两套名称的逐项对应待核实。GauU-Scene 的 Residence 与 UrbanScene3D 的 Residence 不能仅因同名而合并。

Mill19 和 UrbanScene3D 出现在共享仓库的数据准备文档中，但本条论文的数据设置列出的是 MatrixCity 和 GauU-Scene。

## 来源

- [论文 §5.1 与附录，arXiv v2](https://arxiv.org/html/2411.00771v2)
- [官方 README 结果表](https://github.com/Linketic/CityGaussian)
