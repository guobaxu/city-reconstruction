# GauU-Scene

[数据集列表](README.md) · [论文列表](../papers/README.md)

- **类型**：真实无人机采集；RGB 与 LiDAR
- **内容**：城市及校园图像、点云；CityGaussian 文档说明下载内容包含 RGB 与 COLMAP 结果
- **核查日期**：2026-10-22

## 使用该数据集的论文

| 论文 | 论文中的场景名称 | 评估用途 |
|---|---|---|
| [CityGaussianV2](../papers/citygaussian-v2.md) | Residence、Russian Building、Modern Building | 新视角合成、几何重建 |

## 场景命名与版本

CityGaussian 当前 README 展示 LFLS、SMBU、Upper Campus；V2 论文使用上表的名称。两套名称的逐项映射待核实，暂不按结果数值猜测。论文中的 Residence 也不自动等同于 UrbanScene3D 的 Residence。

数据集官网现已扩充场景；其当前完整数据规模不能直接当作 CityGaussianV2 使用子集的规模。

## 获取与准备

- [GauU-Scene 官方网站、论文和下载入口](https://saliteta.github.io/CUHKSZ_SMBU/)
- [CityGaussian 对应数据准备说明](https://github.com/Linketic/CityGaussian/blob/main/doc/data_preparation.md#prepare-gauu-scene-dataset)
- [V2 论文 §5.1 及附录](https://arxiv.org/html/2411.00771v2)

项目文档还提供处理后数据的网盘入口；建议按该文档跳转以保留最新链接。当前图像下采样倍率为 3.4175。LiDAR 真值可用于几何评估，CityGaussian 提供配套真值点云、裁剪区域和对齐资料。

## 待补充

论文与代码场景名映射、使用子集的图像数和范围、下载体积、授权条件、下载与复现状态。
