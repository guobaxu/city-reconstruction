# DroneSplat Dataset

[数据集列表](README.md)

- **类型 / 视角**：真实室外场景；无人机航拍
- **模态**：RGB 图像序列
- **采集设备**：DJI Mavic Pro 3
- **核查日期**：2026-10-22

## 内容与规模

| 项目 | 说明 |
|---|---|
| 完整采集规模 | 24 段序列，包含动态与静态场景 |
| 原始分辨率 | 1920 × 1080、3840 × 2160 |
| 动态干扰 | 车辆、行人、婴儿车、风吹旗帜等 |
| 动态程度 | 低、中、高三级 |
| 当前公开范围 | 官方仓库标明提供 2 个场景；下载包具体清单待核实 |

规模与采集信息来源：[数据说明 §6.1](https://arxiv.org/html/2503.16964v1#S6.SS1)。

## 获取方式

- [数据介绍](https://bityia.github.io/DroneSplat/)
- [Google Drive 下载目录](https://drive.google.com/drive/folders/1DWm-foUQC2QBsrr3QC6Tx8bDmWTfgAzu?usp=sharing)
- [公开数据范围说明](https://github.com/BITyia/DroneSplat#data-preparation)

完整采集规模与当前公开数据包范围分别记录。尚未实际下载核验文件。

## 使用该数据集的已收录论文

| 论文 | 使用范围 | 评估用途 |
|---|---|---|
| [DroneSplat](../papers/dronesplat.md) | 6 个动态场景、2 个静态场景；名称见论文详情 | 动态干扰消除、有限视角重建 |

## 待补充

完整场景清单、每段图像数量、位姿格式、独立几何真值、下载体积及数据授权条件。代码许可证与数据授权条件应分别核实。
