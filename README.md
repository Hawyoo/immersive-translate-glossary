# 沉浸式翻译 · 生物信息学中英术语库

面向英文生物医学论文和生信文档阅读，覆盖转录组、单细胞、多组学、统计分析及肿瘤间质生物学。首版共 **606 条英文词条**；其中包括部分英美拼写、单复数和连接符变体，不代表同等数量的独立概念。

## 下载与导入

1. 打开 [术语 CSV](glossaries/bioinformatics_zh-CN.csv)，点击 GitHub 文件页面的 **Download raw file** 下载原始 CSV 文件。
2. 在沉浸式翻译中进入你截图所示的“添加自定义术语库”，选择从 CSV 文件导入，上传下载的 CSV。
3. 目标语言使用简体中文。导入后先用一段熟悉的英文论文检查实际译文。

[CSV 原始文件直链](https://raw.githubusercontent.com/Hawyoo/immersive-translate-glossary/main/glossaries/bioinformatics_zh-CN.csv)

本仓库提供可手动导入的文件；提交到个人仓库不会自动加入沉浸式翻译的公共术语库，也不代表插件会自动同步更新。

## 文件格式

采用 UTF-8 编码、逗号分隔，表头严格为：

```csv
source,target,tgt_lng
single-cell RNA sequencing,单细胞RNA测序,zh-CN
batch effect,批次效应,zh-CN
mesenchymal stromal cells,间充质基质细胞,zh-CN
mesenchymal stem cells,间充质干细胞,zh-CN
```

CSV 只包含三个字段，不含分类标题、注释或解释段落。

## 覆盖范围

| 类别 | 英文词条数 |
|---|---:|
| 测序与转录组 | 107 |
| 单细胞预处理与整合 | 128 |
| 轨迹通讯及功能 | 70 |
| 空间与多组学 | 98 |
| 变异与免疫组库 | 40 |
| 统计与评估 | 84 |
| 肿瘤及间质生物学 | 79 |
| **合计** | **606** |

## 翻译约定

- 英文译为简体中文，每行目标语言均为 `zh-CN`。
- 常用全称优先，仅加入部分明确的专业缩写，例如 RNA-seq、scRNA-seq 和 ATAC-seq。没有把 MSC、PC 等可能有多个含义的缩写统一替换。
- 区分 mesenchymal stromal cells（间充质基质细胞）与 mesenchymal stem cells（间充质干细胞），不因缩写相同而合并。
- 区分 cell identity（细胞身份）、cell type（细胞类型）和 cell state（细胞状态）；区分 trajectory inference（轨迹推断）和 lineage tracing（谱系追踪）。
- normalization 译作“归一化”，scaling 译作“标准化缩放”；pseudobulk 统一译作“伪批量”。
- precision 在本专业词库中按分类评估语境译为“精确率”，recall 译为“召回率”。普通文本或其他专业语境可能需要不同译法。
- Seurat、SingleR、Harmony、Scanpy 等软件名称，以及基因符号和数据库编号未加入替换规则，建议保留原名。
- 本文件是为生信阅读整理的翻译约定，不是官方中文命名标准。术语匹配优先级、大小写和词形处理由插件及所选翻译引擎决定；并未在你的 Edge 插件中逐条测试。
- 词表用于帮助阅读，不替代原文语境判断；尤其不能把统计关联翻译成因果结论。

## 维护方式

直接编辑 `glossaries/bioinformatics_zh-CN.csv`。新增行遵循：

```text
英文术语,简体中文译法,zh-CN
```

避免重复的 source、空字段，以及含义不明确的孤立缩写。字段如含英文逗号、双引号或换行，按标准 CSV 规则使用双引号包裹；字段内双引号写成两个双引号。

## 格式及术语参考

- [沉浸式翻译官方术语库格式说明](https://github.com/immersive-translate/terms)：CSV 编码、三列表头、目标语言和重复词条规则。
- [Single-cell best practices：Data integration](https://www.sc-best-practices.org/cellular-structure/integration/)：数据整合、批次校正等英文概念。
- [Bioconductor：Analyzing RNA-seq data with DESeq2](https://bioconductor.org/packages/release/bioc/vignettes/DESeq2/inst/doc/DESeq2.html)：RNA-seq 差异分析等英文概念。

上述资料用于核对格式及英文概念；本仓库中文译法为整理后的约定，并非复制自这些来源的官方中译。
