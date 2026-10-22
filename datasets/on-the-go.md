# On-the-go

[数据集列表](README.md)

- **别名**：NeRF On-the-go Dataset
- **类型 / 视角**：真实场景；随手采集的多视图序列，包含室内外场景
- **模态**：RGB、相机内参与位姿、训练与评估划分
- **核查日期**：2026-10-22

## 内容与规模

共 12 段序列，包括 10 个室外场景、2 个室内场景。动态干扰包含行人、骑行者、婴儿车、玩具、车辆、机器人及有轨电车等；官网给出的遮挡比例约为 5%–30%。[官方数据介绍](https://rwn17.github.io/nerf-on-the-go/)

图像总数、各场景原始分辨率、覆盖面积和下载体积待核实。

## 数据格式

- `images/`：原始图像。
- `transforms.json`：由 COLMAP 信息转换而来的相机位姿和内参，采用 Blender 风格格式。
- `split.json`：训练和评估划分，包含 clutter / clean 分类。

来源：[官方数据结构说明](https://github.com/cvg/nerf-on-the-go#dataset-structure-and-configuration-files)。特征和下采样图像由处理流程另行生成。

## 获取方式

- [数据官网](https://rwn17.github.io/nerf-on-the-go/)
- [官方数据 ZIP](https://cvg-data.inf.ethz.ch/on-the-go.zip)
- [下载脚本](https://github.com/cvg/nerf-on-the-go/blob/master/scripts/download_on-the-go.sh)

下载脚本还会生成下采样图像，统计时需区分原始与处理后的文件。

## 使用该数据集的已收录论文

| 论文 | 使用场景 | 评估用途 |
|---|---|---|
| [DroneSplat](../papers/dronesplat.md) | Mountain、Fountain、Corner、Patio、Spot、Patio-High | 动态干扰消除 |

## 待补充

各场景图像数量与分辨率、独立几何真值、数据体积、授权条件及本地下载状态。
