# AnyCity

[论文列表](README.md) · [数据集列表](../datasets/README.md)

- **完整标题**：Feed-Forward Gaussian Splatting from Sparse Aerial Views
- **方法名**：AnyCity
- **发表状态**：arXiv 2026 预印本；本次未确认会议接收信息
- **首次提交**：2026-05-19
- **作者**：Dongli Wu、Zhuoxiao Li、Tongyan Hua、Yinrui Ren、Xiaobao Wei、Rongjun Qin、Wufan Zhao
- **论文**：[arXiv:2605.19949](https://arxiv.org/abs/2605.19949)
- **代码 / 项目页**：本次未找到可核实的官方入口
- **标签**：稀疏航拍、无位姿输入、前馈 3DGS、生成先验
- **状态**：已核查摘要、实验设置与附录；未复现
- **核查日期**：2026-10-22

## 研究笔记

以观测支持的几何骨架为基础，通过门控残差补全弱观测区域，结合视频先验和稠密到稀疏蒸馏，单次前馈输出高斯场景。精读重点：补全区域的几何真实性、训练成本及跨城市泛化。

## 使用的数据集

| 数据集 | 使用范围 / 阶段 | 原文依据 |
|---|---|---|
| [MatrixCity](../datasets/matrixcity.md) | Stage I：几何骨架训练 | §4.1 |
| [GoogleEarth](../datasets/googleearth.md) | Stage II 混合训练语料；新视角评估 | §4.1、表 1 |
| [UrbanScene3D](../datasets/urbanscene3d.md) | Stage II；具体场景与版本待核实 | §4.1 |
| [BlendedMVS](../datasets/blendedmvs.md) | Stage II；航拍子集清单待核实 | §4.1 |
| [DL3DV](../datasets/dl3dv.md) | Stage II；航拍子集清单待核实 | §4.1 |
| [CityNeRF](../datasets/citynerf.md) | 新视角评估 | 表 1 |
| [自采城市航拍（未公开）](../datasets/anycity-real-world.md) | 仅零样本评估 | §4.1、附录 B / F |

## 实验与待核实事项

表 1 比较 2、4、16 个输入视角。代码、精确子集及场景划分清单待核实。附录 B 的 Comparison protocol 将上下文和目标视角写为同一模条件，存在文字歧义，复现时需核对作者说明。

## 来源

- [arXiv 题录与摘要](https://arxiv.org/abs/2605.19949)
- [正文 §4.1、表 1、附录 B / F（v1）](https://arxiv.org/html/2605.19949v1)
