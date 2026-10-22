# 大规模场景重建研究资料库

记录论文、数据集和两者之间的使用关系。已收录 CityGaussian 系列、DroneSplat 与 CityGS-X；核查日期：2026-10-22。

[数据集列表](#数据集列表) · [论文列表](#论文列表)

## 数据集列表

| 数据集 | 类型 / 视角 | 场景与规模 | 数据内容 | 使用该数据集的已收录论文 |
|---|---|---|---|---|
| [MatrixCity](datasets/matrixcity.md) | 合成；航拍、街景 | Small City：2.7 km²；Big City：25.3 km² | RGB、相机位姿、深度、法线、材质属性、点云等 | [CityGaussian](papers/citygaussian.md)、[CityGaussianV2](papers/citygaussian-v2.md)、[CityGS-X](papers/citygs-x.md) |
| [Mill19](datasets/mill19.md) | 真实；无人机航拍 | Building、Rubble，共 2 个场景；详细规模待核实 | RGB、相机参数与位姿 | [CityGaussian](papers/citygaussian.md)、[CityGS-X](papers/citygs-x.md) |
| [UrbanScene3D](datasets/urbanscene3d.md) | 真实与合成；城市航拍 | V1 下载区列出 Residence、Campus、Sci-Art、Square、Hospital | 图像、合成场景路径、模拟器、评估资料等 | [CityGaussian](papers/citygaussian.md)、[DroneSplat](papers/dronesplat.md)、[CityGS-X](papers/citygs-x.md) |
| [GauU-Scene](datasets/gauu-scene.md) | 真实；无人机航拍 | 官网 Table 2：6 个场景，4,693 张图像，6.668 km² | RGB、LiDAR 点云 | [CityGaussianV2](papers/citygaussian-v2.md) |
| [DroneSplat Dataset](datasets/dronesplat.md) | 真实；无人机航拍 | 完整采集 24 段序列；当前标明公开 2 个场景 | RGB，1920 × 1080 / 3840 × 2160 | [DroneSplat](papers/dronesplat.md) |
| [On-the-go](datasets/on-the-go.md) | 真实；室内外多视图 | 12 段序列：10 个室外、2 个室内 | RGB、相机内参与位姿、数据划分 | [DroneSplat](papers/dronesplat.md) |

统计范围与来源见各数据集详情。不同版本和数据包分别统计，未核实的信息标记为待核实。

## 论文列表

| 论文 | 会议 / 年份 | 研究重点 | 使用的数据集 | 阅读 / 复现状态 |
|---|---|---|---|---|
| [CityGaussian（V1）](papers/citygaussian.md) | ECCV 2024 | 3DGS、大场景分块训练、LoD 实时渲染 | [MatrixCity](datasets/matrixcity.md)、[Mill19](datasets/mill19.md)、[UrbanScene3D-V1](datasets/urbanscene3d.md) | 已核查摘要与数据设置；未复现 |
| [CityGaussianV2](papers/citygaussian-v2.md) | ICLR 2025 | 2DGS、大场景几何重建、并行训练 | [MatrixCity](datasets/matrixcity.md)、[GauU-Scene](datasets/gauu-scene.md) | 已核查摘要与数据设置；未复现 |
| [DroneSplat](papers/dronesplat.md) | CVPR 2025 Highlight | 3DGS、动态干扰消除、有限视角重建 | [DroneSplat Dataset](datasets/dronesplat.md)、[On-the-go](datasets/on-the-go.md)、[UrbanScene3D](datasets/urbanscene3d.md) | 已核查摘要与数据设置；未复现 |
| [CityGS-X](papers/citygs-x.md) | ICCV 2025 | 多 GPU 训练与渲染、层次混合表示、几何重建 | [MatrixCity](datasets/matrixcity.md)、[Mill19](datasets/mill19.md)、[UrbanScene3D](datasets/urbanscene3d.md) | 已核查摘要与数据设置；未复现 |

会议年份按官方仓库标注；阅读状态不表示已精读全文。

## 阅读与检索

每篇论文、每个数据集各有一份 Markdown 笔记，可在编辑器、GitHub 或支持 Markdown 的笔记工具中阅读。全文检索示例：

```bash
cd /media/gx/workspace/city-reconstruction
rg 'MatrixCity|几何|街景' papers datasets
```

## 维护约定

1. 新增论文时复制 [论文模板](templates/paper.md)，填写实际使用的数据集、版本、场景与证据。
2. 新增数据集时复制 [数据集模板](templates/dataset.md)，记录下载入口、模态、真值及使用限制。
3. 同步更新首页的两个列表、独立列表页与详情页中的反向链接。关联表示已核实的实验使用；仅在引言中引用不算使用。
4. 分开记录论文实验、当前代码支持和后续复现实验，避免将仓库支持范围当成原论文范围。
5. 数据集列表和详情页以数据集本身的内容与统计为主；论文相关信息只放在“使用该数据集的已收录论文”列或章节，方法特定的预处理与实验差异写入论文详情。
6. 缺失信息标记“待核实”，不要猜测同名场景的身份；统计数字需注明版本和统计范围。

## 当前收录

4 篇方法论文、6 个数据集。CityGaussian V1 与 V2 分别建档；后续可继续扩充论文与数据集条目。这里只保存资料和链接，尚未下载图像、模型或论文 PDF，也未执行复现实验。

## 资料来源

- [CityGaussian 官方仓库](https://github.com/Linketic/CityGaussian)
- [当前 main 分支数据准备文档](https://github.com/Linketic/CityGaussian/blob/main/doc/data_preparation.md)
- [V1 论文 §4.1](https://arxiv.org/html/2404.01133v3)
- [V2 论文 §5.1](https://arxiv.org/html/2411.00771v2)
- [DroneSplat 官方仓库](https://github.com/BITyia/DroneSplat)
- [DroneSplat 论文与数据设置](https://arxiv.org/html/2503.16964v1)
- [CityGS-X 官方仓库](https://github.com/gyy456/CityGS-X)
- [CityGS-X 论文与数据设置](https://arxiv.org/html/2503.23044v1)

网页会更新；各条目的日期表示最近人工核查时间，不代表下载链接已实际完成下载验证。
