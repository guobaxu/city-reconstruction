# DroneSplat

[论文列表](README.md) · [数据集列表](../datasets/README.md)

- **完整标题**：DroneSplat: 3D Gaussian Splatting for Robust 3D Reconstruction from In-the-Wild Drone Imagery
- **会议**：CVPR 2025（Highlight）
- **作者**：Jiadong Tang、Yu Gao、Dianyi Yang、Liqi Yan、Yufeng Yue、Yi Yang
- **论文**：[arXiv:2503.16964](https://arxiv.org/abs/2503.16964)
- **项目页**：[DroneSplat](https://bityia.github.io/DroneSplat/)
- **代码**：[官方仓库](https://github.com/BITyia/DroneSplat)
- **标签**：无人机重建、3DGS、动态干扰消除、稀疏视角
- **状态**：已核查摘要、实验设置与补充材料数据说明；未复现
- **核查日期**：2026-10-22

## 研究笔记

结合自适应局部与全局掩码消除动态干扰，利用多视图几何先验和体素约束改善有限视角重建。对本课题的参考价值在于真实航拍中的动态物体处理；分块扩展到城市规模的能力需另行评估。

## 使用的数据集

| 数据集 | 实验范围 | 用途 | 证据 |
|---|---|---|---|
| [DroneSplat Dataset](../datasets/dronesplat.md) | 动态：Cultural Center、TangTian、Pavilion、Simingshan、Intersection、Sculpture；静态：Exhibition Hall、Plaza | 动态干扰消除；静态场景各 6 个输入视角 | §4.1、图 6、图 8 |
| [On-the-go](../datasets/on-the-go.md) | Mountain、Fountain、Corner、Patio、Spot、Patio-High | 动态干扰消除 | §4.1、图 7 |
| [UrbanScene3D](../datasets/urbanscene3d.md) | PolyTech、ArtSci；具体发布版本待核实 | 两个真实场景，各 6 个输入视角 | §4.1、图 9 |

主要指标为 PSNR、SSIM、LPIPS。补充材料还在 Simingshan、Sculpture 上验证动态与稀疏视角同时存在的情况。

## 发布范围与待核实事项

仓库仅标明提供自建数据集的 2 个场景，不应据此推断完整 24 段序列都可下载。UrbanScene3D 的场景名称按原文保留，不与已有 V1 场景强行映射。

## 来源

- [论文 §4.1、§6.1 及实验图表](https://arxiv.org/html/2503.16964v1)
- [官方仓库数据准备说明](https://github.com/BITyia/DroneSplat#data-preparation)
- [官方项目页](https://bityia.github.io/DroneSplat/)
