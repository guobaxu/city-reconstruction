# Mill19

[数据集列表](README.md) · [论文列表](../papers/README.md)

- **类型**：真实无人机航拍
- **关注场景**：Building、Rubble
- **数据入口**：Mega-NeRF 发布的数据与相机信息
- **核查日期**：2026-10-22

## 使用该数据集的论文

| 论文 | 使用场景 | 评估用途 |
|---|---|---|
| [CityGaussian](../papers/citygaussian.md) | Building、Rubble | 新视角合成、渲染效率 |

## 获取与准备

- [Mega-NeRF 官方数据说明与场景下载](https://github.com/cmusatyalab/mega-nerf#data)
- [CityGaussian 数据准备说明](https://github.com/Linketic/CityGaussian/blob/main/doc/data_preparation.md#prepare-mill19--urbanscene3d-datasets)

原始数据按文档放入 `data/mill19`，随后转换为 COLMAP 风格。当前文档建议使用作者提供的 COLMAP 结果，图像下采样倍率为 4.0。

## 几何与使用边界

CityGaussian 文档表示 Mill19 未提供其评估所需的真值点云，因此未纳入其几何评估包。COLMAP 稀疏点云是重建输入，不能直接当作独立几何真值。

## 待补充

精确图像数量、分辨率、磁盘体积、原始数据授权条款、下载与复现状态；Mega-NeRF 原论文可后续独立建档。
