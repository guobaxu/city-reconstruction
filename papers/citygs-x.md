# CityGS-X

[论文列表](README.md) · [数据集列表](../datasets/README.md)

- **完整标题**：CityGS-X: A Scalable Architecture for Efficient and Geometrically Accurate Large-Scale Scene Reconstruction
- **会议**：ICCV 2025（官方仓库标注）
- **作者**：Yuanyuan Gao、Hao Li、Jiaqi Chen、Zhengyu Zou、Zhihang Zhong、Dingwen Zhang、Xiao Sun、Junwei Han
- **论文**：[arXiv:2503.23044](https://arxiv.org/abs/2503.23044)
- **项目页**：[CityGS-X](https://lifuguan.github.io/CityGS-X/)
- **代码**：[官方仓库](https://github.com/gyy456/CityGS-X)
- **标签**：大规模场景重建、多 GPU 训练与渲染、层次混合表示、几何重建
- **状态**：已核查摘要、实验设置与补充材料；未复现
- **核查日期**：2026-10-22

## 研究笔记

以并行层次混合表示 PH²-3D 和批量多任务渲染支持多 GPU 扩展，并通过 RGB、深度、几何约束的渐进训练改善表面质量。对本课题的精读重点：表示与渲染如何分配到多 GPU、通信开销，以及几何质量与训练效率的权衡。

## 使用的数据集

| 数据集 | 实验范围 | 用途 | 证据 |
|---|---|---|---|
| [MatrixCity](../datasets/matrixcity.md) | Small City 的 Aerial 航拍场景 | 渲染与表面重建评估 | §4.1、§4.2、表 2 |
| [Mill19](../datasets/mill19.md) | Building、Rubble | 渲染评估与网格可视化 | §4.1、表 1、补充材料 |
| [UrbanScene3D](../datasets/urbanscene3d.md) | Residence、Sci-Art；具体发布版本待核实 | 渲染评估与网格可视化 | §4.1、表 1、补充材料 |

## 实验设置

论文默认使用 4 张 RTX 4090、batch size 4。Mill19 与 UrbanScene3D 图像下采样 4 倍；MatrixCity 下采样 1.2 倍。渲染指标为 PSNR、SSIM、LPIPS；MatrixCity 另报告几何 Precision、Recall、F1。

## 复现资料与待核实事项

官方仓库提供数据准备、训练、网格提取及评估命令，并链接额外复现资料。当前代码可能包含论文发表后的优化，复现时需固定版本；详细数据划分、UrbanScene3D 发布版本及实际运行开销待核实。

## 来源

- [论文 §4.1、§4.2 与补充材料](https://arxiv.org/html/2503.23044v1)
- [官方仓库：会议、数据准备与复现入口](https://github.com/gyy456/CityGS-X)
- [官方项目页](https://lifuguan.github.io/CityGS-X/)
