# UrbanScene3D

[数据集列表](README.md) · [论文列表](../papers/README.md)

- **类型**：原数据集包含多种场景；本库记录 CityGaussian 使用的真实航拍部分
- **关注版本**：UrbanScene3D-V1
- **关注场景**：Residence、Sci-Art
- **原始论文**：Capturing, Reconstructing, and Simulating: the UrbanScene3D Dataset（ECCV 2022）
- **核查日期**：2026-10-22

## 使用该数据集的论文

| 论文 | 使用范围 | 评估用途 |
|---|---|---|
| [CityGaussian](../papers/citygaussian.md) | V1 的 Residence、Sci-Art | 新视角合成、渲染效率 |

## 获取与准备

- [UrbanScene3D 官方仓库](https://github.com/Linxius/UrbanScene3D)
- [UrbanScene3D-V1 下载区](https://github.com/Linxius/UrbanScene3D#urbanscene3d-v1)
- [Mega-NeRF 相机位姿及图像整理说明](https://github.com/cmusatyalab/mega-nerf#data)
- [CityGaussian 准备说明](https://github.com/Linketic/CityGaussian/blob/main/doc/data_preparation.md#prepare-mill19--urbanscene3d-datasets)

CityGaussian 明确要求 V1，原始数据放入 `data/urban_scene_3d`；当前文档图像下采样倍率为 4.0。Mega-NeRF 还提供其他场景的位姿，不表示这些场景也用于 CityGaussian 原论文。

## 几何与使用边界

该数据未纳入 CityGaussian 的几何真值评估包。原始 UrbanScene3D 另有自己的评估数据及工具，不能将“未纳入 CityGaussian 评估包”理解为所有版本都没有几何资料。

官方仓库标明仅供非商业使用，并要求引用及限制再分发，使用前应阅读其 [Copyright](https://github.com/Linxius/UrbanScene3D#copyright)。

## 待补充

各场景精确图像清单、数据量、位姿版本、下载与复现状态。
