# GauU-Scene

[数据集列表](README.md)

- **类型 / 视角**：真实城市场景；无人机航拍
- **模态**：RGB、LiDAR 点云
- **采集设备**：Matrix 300 无人机、Zenmuse L1 LiDAR
- **核查日期**：2026-10-22

## 场景与规模

以下统计取自[官网 Dataset Information 的 Table 2](https://saliteta.github.io/CUHKSZ_SMBU/)，对应官网列出的六场景范围。

| 场景 | 面积（km²） | 图像数量 | 原始数据（GB） |
|---|---:|---:|---:|
| Lower Campus | 1.020 | 670 | 12.5 |
| Upper Campus | 0.923 | 715 | 13.5 |
| HAV（He Ao Village） | 0.815 | 424 | 7.8 |
| LFLS | 1.467 | 1,106 | 19.8 |
| SMBU | 0.908 | 563 | 16.2 |
| SZIIT | 1.557 | 1,215 | 22.3 |
| 合计 | 6.668 | 4,693 | 92.1 |

图像分辨率为 5472 × 3648。原始数据体积指 DJI 原始数据，不包含后处理点云；不等于整理后的训练包大小。官网摘要与统计表的面积口径存在差异，这里采用 Table 2 的六场景统计。

## 数据内容与坐标

提供 RGB 图像与 LiDAR 点云；点云为 PLY 格式，地理坐标参考为 WGS 84 / UTM zone 50N（EPSG:32650）。[官方数据介绍](https://saliteta.github.io/CUHKSZ_SMBU/)

## 获取方式

[官方网站与数据下载入口](https://saliteta.github.io/CUHKSZ_SMBU/)。实际下载时应核对场景清单及数据包版本。

## 使用该数据集的已收录论文

| 论文 | 论文中的场景名称 | 评估用途 |
|---|---|---|
| [CityGaussianV2](../papers/citygaussian-v2.md) | Residence、Russian Building、Modern Building | 新视角合成、几何重建 |

论文与当前代码中的场景名称差异及待核实映射见[论文详情](../papers/citygaussian-v2.md)。

## 待补充

数据包版本、点云统计校验、相机参数与位姿格式、授权条件及本地下载状态。
