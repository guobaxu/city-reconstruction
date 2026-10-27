# MatrixCity

[数据集列表](README.md)

- **类型 / 视角**：合成城市；航拍和街景
- **模态**：RGB、相机位姿、深度、法线、材质属性、点云
- **核查日期**：2026-10-22

## 场景与规模

| 场景版本 | 地图面积 | 视角 |
|---|---|---|
| small_city | 2.7 km² | 航拍、街景 |
| big_city | 25.3 km² | 航拍、街景 |

街景普通训练集采集间隔为 5 m，密集训练集为 1 m。图像数量、分辨率及下载体积需按版本、视角和数据包分别统计。来源：[官方数据结构说明](https://github.com/city-super/MatrixCity#data-structure)。

## 数据内容与格式

RGB 为 PNG；深度和法线使用 EXR。深度为 Z-depth，单位为 cm；另有 float32 深度包。Small City 还提供 diffuse、metallic、roughness、specular 和航拍 / 街景点云。[官方格式说明](https://github.com/city-super/MatrixCity#data-color-space)

相机位姿保存为 JSON 中的 camera-to-world 矩阵。原始块目录与整理后的 pose 目录采用不同位置尺度，使用前应核对坐标单位。[位姿说明](https://github.com/city-super/MatrixCity#pose-file-structure)

## 获取方式

- [官方仓库与下载说明](https://github.com/city-super/MatrixCity#data-download)
- [Hugging Face 数据目录](https://huggingface.co/datasets/BoDai/MatrixCity/tree/main)

## 使用该数据集的已收录论文

| 论文 | 使用范围 | 评估用途 |
|---|---|---|
| [CityGaussian](../papers/citygaussian.md) | Small City 全城航拍；街景 Block_A | 新视角合成、渲染速度 |
| [CityGaussianV2](../papers/citygaussian-v2.md) | 航拍与街景；仓库指定 small_city | 渲染、几何重建 |
| [CityGS-X](../papers/citygs-x.md) | Small City 的 Aerial 航拍场景 | 渲染、表面重建；[原文 §4.1](https://arxiv.org/html/2503.23044v1) |
| [AnyCity](../papers/anycity.md) | Stage I 几何骨架训练 | [§4.1](https://arxiv.org/html/2605.19949v1) |
| [MetroGS](../papers/metrogs.md) | Aerial、Street | 渲染、几何重建；[§5.1、表 2、附录 A](https://arxiv.org/html/2511.19172v1) |


## 待补充

各数据包图像数、分辨率、下载体积、数据授权条款及本地下载状态。
