# MetroGS

[论文列表](README.md) · [数据集列表](../datasets/README.md)

- **完整标题**：MetroGS: Efficient and Stable Reconstruction of Geometrically Accurate High-Fidelity Large-Scale Scenes
- **会议**：CVPR 2026（官方仓库标注）；预印本发表于 2025 年
- **论文**：[arXiv:2511.19172](https://arxiv.org/abs/2511.19172)
- **项目页**：[MetroGS](https://m3phist0.github.io/MetroGS/)
- **代码**：[官方 GitHub 仓库](https://github.com/M3phist0/MetroGS)
- **标签**：大规模场景重建、分布式 2DGS、几何重建、外观建模
- **状态**：已核查官方仓库、论文方法与实验设置及补充材料；未复现
- **核查日期**：2026-10-27

## 研究笔记

基于分布式 2DGS，以 pointmap 辅助初始化和稀疏补偿增密改善覆盖，再结合单目深度与多视图约束渐进优化几何，通过深度引导的外观建模处理光照差异。精读重点：几何稳定性、多 GPU 通信及显存开销。

## 使用的数据集

| 数据集 | 实验范围 | 用途 | 证据 |
|---|---|---|---|
| [MatrixCity](../datasets/matrixcity.md) | Aerial、Street | 渲染与几何评估 | §5.1、表 2、附录 A |
| [GauU-Scene](../datasets/gauu-scene.md) | Russian Building、Residence、Modern Building | 渲染与几何评估 | §5.1、表 1 |
| [Mill19](../datasets/mill19.md) | Building、Rubble | 补充渲染评估 | 附录 C.3、表 6 |
| [UrbanScene3D](../datasets/urbanscene3d.md) | Residence、Sci-Art；发布版本待核实 | 补充渲染评估 | 附录 C.3、表 6 |

## 实验与复现资料

论文使用 4 张 RTX 3090，报告 PSNR、SSIM、LPIPS 及几何 Precision、Recall、F1。官方仓库提供安装、数据准备、训练、渲染和网格提取评估入口；尚未下载数据或运行实验。

## 来源与待核实事项

- [官方仓库：会议标注、使用说明与引用信息](https://github.com/M3phist0/MetroGS)
- [论文 v1：§4、§5.1、表 1–2、附录 A / C.3](https://arxiv.org/html/2511.19172v1)

GauU-Scene 保留论文场景名，与数据集官网名称的对应待核实；UrbanScene3D 的具体发布版本及各数据包划分待核实。当前代码与论文实验配置需在复现时固定版本核对。
