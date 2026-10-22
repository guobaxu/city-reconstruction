# UrbanScene3D

[数据集列表](README.md)

- **类型 / 视角**：真实与合成城市场景；航拍
- **数据内容**：图像、合成场景路径、模拟器及几何评估资料
- **核查日期**：2026-10-22

## 版本与场景

官方单独保留 UrbanScene3D-V1 下载区，列出 Residence、Campus、Sci-Art、Square、Hospital；完整数据下载另有入口。不同发布版本的规模需分别统计。[版本与场景目录](https://github.com/Linxius/UrbanScene3D#urbanscene3d-v1)

## 数据内容与统计

| 内容 | 说明 |
|---|---|
| 合成图像 | 官方采集程序提供 4 个合成场景；分辨率为 6000 × 4000，FOV 为 60° |
| 合成路径 | 包含图像名、位置与姿态；使用 UE 左手坐标系，Z 轴向上，单位 cm |
| 真实图像 | 包含 GPS 信息；相机参数需按设备标定 |
| 模拟器 | 包含合成场景和真实场景的重建结果 |
| 几何评估 | 提供采样点、真实场景加密评估数据与配套工具 |

来源：[官方数据格式、采集与评估说明](https://github.com/Linxius/UrbanScene3D)。各版本的图像总数、面积和下载体积待核实。

## 获取与授权

- [官方仓库与完整数据下载](https://github.com/Linxius/UrbanScene3D)
- [UrbanScene3D-V1 下载区](https://github.com/Linxius/UrbanScene3D#urbanscene3d-v1)

仅限非商业使用，要求引用并限制再分发，具体以官方 [Copyright](https://github.com/Linxius/UrbanScene3D#copyright) 为准。

## 使用该数据集的已收录论文

| 论文 | 使用范围 | 评估用途 |
|---|---|---|
| [CityGaussian](../papers/citygaussian.md) | V1 的 Residence、Sci-Art | 新视角合成、渲染效率 |
| [DroneSplat](../papers/dronesplat.md) | PolyTech、ArtSci；发布版本待核实，各 6 个输入视角 | 有限视角重建；[原文 §4.1、图 9](https://arxiv.org/html/2503.16964v1) |
| [CityGS-X](../papers/citygs-x.md) | Residence、Sci-Art；发布版本待核实 | 渲染评估、网格可视化；[原文 §4.1](https://arxiv.org/html/2503.23044v1) |
| [AnyCity](../papers/anycity.md) | Stage II 混合训练；场景与版本待核实 | [§4.1](https://arxiv.org/html/2605.19949v1) |


## 待补充

各版本图像清单、原始相机信息、覆盖面积、磁盘体积及本地下载状态。
