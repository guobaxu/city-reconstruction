# 大规模场景重建研究资料库

记录论文、数据集和两者之间的使用关系。首批整理 CityGaussian 系列；核查日期：2026-10-22。

## 两个检索入口

- [论文列表：从论文查看所用数据集](papers/README.md)
- [数据集列表：从数据集查看使用它的论文](datasets/README.md)

每篇论文、每个数据集各有一份 Markdown 笔记，可在编辑器、GitHub 或支持 Markdown 的笔记工具中阅读。全文检索示例：

```bash
cd /media/gx/workspace/city-reconstruction
rg 'MatrixCity|几何|街景' papers datasets
```

## 维护约定

1. 新增论文时复制 [论文模板](templates/paper.md)，填写实际使用的数据集、版本、场景与证据。
2. 新增数据集时复制 [数据集模板](templates/dataset.md)，记录下载入口、模态、真值及使用限制。
3. 同步更新两个列表与详情页中的反向链接。关联表示已核实的实验使用；仅在引言中引用不算使用。
4. 分开记录论文实验、当前代码支持和后续复现实验，避免将仓库支持范围当成原论文范围。
5. 数据集列表和详情页以数据集本身的内容与统计为主；论文相关信息只放在“使用该数据集的已收录论文”列或章节，方法特定的预处理与实验差异写入论文详情。
6. 缺失信息标记“待核实”，不要猜测同名场景的身份；统计数字需注明版本和统计范围。

## 当前收录

2 篇方法论文、4 个数据集。CityGaussian V1 与 V2 分别建档；数据集的原始论文保留外部入口，后续可独立扩充。这里只保存资料和链接，尚未下载图像、模型或论文 PDF，也未执行复现实验。

## 首批资料来源

- [CityGaussian 官方仓库](https://github.com/Linketic/CityGaussian)
- [当前 main 分支数据准备文档](https://github.com/Linketic/CityGaussian/blob/main/doc/data_preparation.md)
- [V1 论文 §4.1](https://arxiv.org/html/2404.01133v3)
- [V2 论文 §5.1](https://arxiv.org/html/2411.00771v2)

网页会更新；各条目的日期表示最近人工核查时间，不代表下载链接已实际完成下载验证。
