# CityNeRF / BungeeNeRF 数据

[数据集列表](README.md)

- **核查日期**：2026-10-22
- **类型**：多尺度城市视图，包含 Google Earth Studio 渲染内容
- **内容**：RGB 图像、处理后的相机位姿、可编辑的相机轨迹文件

## 公开场景

官方数据区提供 `multiscale_google_56Leonard` 与 `multiscale_google_Transamerica` 两个预处理包，可从远景到近景观察城市建筑。[数据说明与下载](https://github.com/city-super/BungeeNeRF#data)

## 格式与使用

相机轨迹可由 Google Earth Studio 导出 JSON；处理流程涉及坐标变换与场景尺度归一化。图像数、分辨率、包体积及影像使用条款需分别核实。

此条与另一发布来源的 GoogleEarth 数据分开记录，避免仅按影像平台名称合并不同数据包。

## 使用该数据集的已收录论文

| 论文 | 使用范围 / 用途 | 证据 |
|---|---|---|
| [AnyCity](../papers/anycity.md) | 表 1 中的 CityNerf 评估；具体场景清单待核实 | [正文与附录](https://arxiv.org/html/2605.19949v1) |
