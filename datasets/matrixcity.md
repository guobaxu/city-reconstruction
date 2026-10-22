# MatrixCity

[数据集列表](README.md) · [论文列表](../papers/README.md)

- **类型**：合成城市；航拍和街景
- **本库关注版本**：small_city
- **数据内容**：RGB、相机位姿；官方另提供深度、法线、材质属性及点云等
- **数据集原始论文**：MatrixCity: A Large-scale City Dataset for City-scale Neural Rendering and Beyond（ICCV 2023）；入口见官方仓库
- **核查日期**：2026-10-22

## 使用该数据集的论文

| 论文 | 使用范围 | 评估用途 |
|---|---|---|
| [CityGaussian](../papers/citygaussian.md) | Small City 全城航拍；街景 Block_A | 新视角合成、渲染速度 |
| [CityGaussianV2](../papers/citygaussian-v2.md) | 航拍与街景；仓库准备文档指定 small_city | 渲染、几何重建 |

## 获取与准备

- [官方仓库及下载说明](https://github.com/city-super/MatrixCity)
- [Hugging Face 数据目录](https://huggingface.co/datasets/BoDai/MatrixCity/tree/main)
- [CityGaussian 预处理说明](https://github.com/Linketic/CityGaussian/blob/main/doc/data_preparation.md#prepare-matrixcity-dataset)

按项目文档将航拍原始数据放入 `data/matrix_city/aerial`，使用作者 COLMAP 结果或从头准备。当前文档的图像下采样倍率为航拍 1.2、街景 1.0。V1 论文的航拍设置记为宽度 1600，比较实验时应核对实际输出分辨率。

## 几何与版本注意事项

CityGaussian 为该数据提供几何评估真值包，见数据准备文档。下载时区分 small_city、big_city、深度与图像包；不同位姿文件的坐标尺度及深度格式以官方说明为准。授权条件以数据集原始发布方为准。

## 待补充

实际下载体积、各实验使用的精确图像清单、许可条款核对、下载与复现状态。
