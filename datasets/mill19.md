# Mill19

[数据集列表](README.md)

- **类型 / 视角**：真实场景；无人机航拍
- **模态**：RGB 图像、相机内参与位姿
- **核查日期**：2026-10-22

## 场景与规模

| 场景 | 发布形式 | 图像数量 / 分辨率 / 体积 |
|---|---|---|
| Building | 独立场景下载包 | 待核实 |
| Rubble | 独立场景下载包 | 待核实 |

## 数据内容与格式

发布格式包含训练和验证图像目录 `train/rgbs`、`val/rgbs`，以及对应的 `metadata` 相机信息。相机元数据包含图像宽高、内参与 camera-to-world 位姿；`coordinates.pt` 记录坐标原点和尺度。[数据结构说明](https://github.com/cmusatyalab/mega-nerf#data)

独立几何真值点云的提供情况待核实。相机重建得到的稀疏点云与独立几何真值应分开记录。

## 获取方式

[场景下载入口与数据说明](https://github.com/cmusatyalab/mega-nerf#data)分别提供 Building、Rubble 数据包。

## 使用该数据集的已收录论文

| 论文 | 使用场景 | 评估用途 |
|---|---|---|
| [CityGaussian](../papers/citygaussian.md) | Building、Rubble | 新视角合成、渲染效率 |

## 待补充

各场景精确图像数量、原始分辨率、磁盘体积、几何真值、授权条款及本地下载状态。
