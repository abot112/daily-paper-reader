---
title: "Mamba Goes HoME: Hierarchical Soft Mixture-of-Experts for 3D Medical Image Segmentation"
title_zh: Mamba入驻HoME：面向3D医学图像分割的分层软混合专家
authors: "Szymon Plotka, Gizem Mert, Maciej Chrabaszcz, Ewa Szczurek, Arkadiusz Sitek"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=ztgYn0Uk94"
tags: ["query:abdk-seg"]
score: 8.0
evidence: 使用分层软混合专家的3D医学图像分割架构；直接适用于腹部CT多器官分割
tldr: 提出HoME层，一种基于Mamba主干的分层软混合专家方法，用于高效3D医学图像分割。该架构通过自适应专家路由处理长上下文，可直接应用于全监督腹部CT多器官分割任务，在医学图像分割中展现出有效性。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-ztgyn0uk94/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 684, \"height\": 895, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ztgyn0uk94/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1445, \"height\": 426, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ztgyn0uk94/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 870, \"height\": 408, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ztgyn0uk94/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1440, \"height\": 1622, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ztgyn0uk94/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1444, \"height\": 1097, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ztgyn0uk94/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1450, \"height\": 573, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ztgyn0uk94/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1442, \"height\": 585, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ztgyn0uk94/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1448, \"height\": 576, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ztgyn0uk94/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1446, \"height\": 548, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ztgyn0uk94/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1448, \"height\": 546, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ztgyn0uk94/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1447, \"height\": 550, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-ztgyn0uk94/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1427, \"height\": 1068, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1023, \"height\": 440, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1309, \"height\": 412, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 521, \"height\": 440, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 520, \"height\": 439, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 876, \"height\": 394, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 875, \"height\": 270, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 445, \"height\": 260, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 445, \"height\": 315, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1446, \"height\": 341, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1052, \"height\": 618, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1447, \"height\": 404, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1168, \"height\": 417, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 734, \"height\": 464, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1447, \"height\": 316, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1446, \"height\": 255, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1163, \"height\": 272, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1163, \"height\": 251, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1449, \"height\": 296, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1448, \"height\": 241, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1448, \"height\": 342, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1445, \"height\": 286, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1165, \"height\": 299, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1449, \"height\": 407, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1448, \"height\": 410, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1447, \"height\": 409, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-ztgyn0uk94/table-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1447, \"height\": 407, \"label\": \"Table\"}]"
motivation: 3D医学图像分割面临长上下文建模和模态差异挑战。
method: 基于Mamba设计两级令牌路由层：局部软混合专家和全局专家聚合。
result: 在多个3D医学分割数据集上取得高效性能。
conclusion: 为3D医学分割提供了有效的长序列建模方案，适用于腹部器官分割。
---

## Abstract
In recent years, artificial intelligence has significantly advanced medical image segmentation. Nonetheless, challenges remain, including efficient 3D medical image processing across diverse modalities and handling data variability. In this work, we introduce Hierarchical Soft Mixture-of-Experts (HoME), a two-level token-routing layer for efficient long-context modeling, specifically designed for 3D medical image segmentation. Built on the Mamba Selective State Space Model (SSM) backbone, HoME enhances sequential modeling through adaptive expert routing. In the first level, a Soft Mixture-of-Experts (SMoE) layer partitions input sequences into local groups, routing tokens to specialized per-group experts for localized feature extraction. The second level aggregates these outputs through a global SMoE layer, enabling cross-group information fusion and global context refinement. This hierarchical design, combining local expert routing with global expert refinement, enhances generalizability and segmentation performance, surpassing state-of-the-art results across datasets from the three most widely used 3D medical imaging modalities and varying data qualities. The code is publicly available at https://github.com/gmum/MambaHoME.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **研究动机**：三维医学图像分割（CT、MRI、超声）是诊断和手术规划的基础，但面临两大挑战：高效处理高分辨率长序列数据，以及跨模态、跨数据分布的泛化能力。
- **核心问题**：现有方法存在局限：CNN感受野有限，难以捕获全局依赖；Vision Transformer 计算复杂度高（二次方），不适合体积数据；Mamba 等状态空间模型虽以线性复杂度建模长序列，但缺乏对数据局部模式的显式适应能力。
- **整体含义**：论文旨在提出一种**高效且能同时捕捉局部‑全局空间层次**的架构，将 Mamba 的长序列建模能力与混合专家（MoE）的模块化自适应路由相结合，以提升三维医学图像分割的精度、效率与泛化性。

## 2. 方法论

### 2.1 核心思想
- 提出 **Hierarchical Soft Mixture‑of‑Experts（HoME）层**，实现两级令牌路由：
  1. **局部级**：对输入序列分组，每组独立进行软路由，分配到多个局部专家，提取组内特征。
  2. **全局级**：聚合各组输出，再次通过软路由分配给全局专家，实现跨组信息融合。
- 将 HoME 嵌入到 **Mamba‑HoME 块**中，并与下采样结合，形成 U 形编解码器网络（Mamba‑HoME），专用于三维医学图像分割。

### 2.2 关键技术细节
- **Mamba 层**：利用连续时间循环形式，输入依赖参数 \(A, B, C\)，实现 \(O(Nd)\) 的线性复杂度和长程依赖建模。
- **HoME 层流程**（图1）：
  - **分组槽分配**（Grouped Slot Assignment）：将输入序列分为 \(G_i\) 组，每组 \(K_i\) 个令牌。各组独立计算令牌与可学习槽嵌入的点积，经过 softmax 得到软分配权重，然后聚合得到槽表示 \(\tilde{x}\)。此步骤降低峰值内存并保持局部性。
  - **第一级局部专家处理**：每个组内的槽表示通过路由网络（MLP + softmax）分配给 \(E_{1,i}\) 个局部前馈网络专家，产出组内细化的输出 \(y^{(1)}\)。
  - **第二级全局专家处理**：将所有组的槽输出展平后，传给 \(E_{2,i}\) 个全局专家，经路由和加权求和得到全局上下文表示 \(y^{(2)}\)。
  - **输出重建**：使用注意力权重将 \(y^{(2)}\) 映射回原始令牌序列，去除填充，得到最终输出。
- **Mamba‑HoME 块**（图1b）：输入体积 → 门控空间卷积（GSC）→ DyT 归一化 → Mamba（扁平化为1D）→ DyT → HoME → 残差连接，最后 reshape 回体素形式。
- **网络结构**：4级编码器（每组令牌数 \(K\) 递减，专家数 \(E\) 递增），各层堆叠多个 Mamba‑HoME 块，瓶颈后接解码器，通过跳跃连接和上采样块恢复分辨率。
- **归一化**：使用 Dynamic Tanh（DyT）替代 LayerNorm，利用 tanh 的有界性稳定梯度，减少计算开销，据称训练和推理速度提升约6%。

### 2.3 复杂度
- Mamba 部分 \(O(BNd)\)，HoME 部分 \(O(B G_i (E_{1,i}+E_{2,i}) L_i d)\)，总体与序列长度成线性关系，优于 Transformer 的二次方复杂度。

## 3. 实验设计

### 3.1 数据集与场景
- **预训练**：AbdomenAtlas 1.1（8,788 CT 扫描，25类腹部器官）+ TotalSegmentator MRI（616 MRI 扫描，对齐22类），用于监督预训练。
- **训练/微调/测试**：
  - PANORAMA（CT，胰腺与 PDAC 分割，1,964 训练 / 334 测试）
  - AMOS（CT+MRI，15类腹部器官，240训练/120测试，含单模态及跨模态设置）
  - FeTA 2022（胎儿脑 MRI，7类组织，120例，5折交叉验证）
  - MVSeg（3D 超声，二尖瓣瓣叶分割，110训练/30验证/40测试）
  - 内部 CT 数据集（60例 PDAC 与胰腺，仅测试）
- 涵盖三种主要模态（CT, MRI, US）及多种解剖部位，数据质量差异大（噪声、分辨率、对比度）。

### 3.2 对比方法与基准
- 对比8种最新方法：SegMamba（直接基线）、uC 3DU‑Net、Swin SMT、VoCo‑B、SuPreM、Hermes、Swin UNETR、VSmTrans。部分方法使用预训练权重（如 VoCo‑B、SuPreM）。
- 评估指标：各器官/病灶的 Dice 相似系数（DSC）、平均 DSC（mDSC）、95% Hausdorff 距离（mHD95）；部分任务还报告敏感性和特异性。

### 3.3 实验设置细节
- 统一使用 Anisotropic/Isotropic 重采样、强度裁剪与 min‑max 归一化、随机数据增强（旋转、翻转、缩放、噪声等）。
- 优化器：AdamW，初始学习率 1e‑4，余弦退火，权重衰减 1e‑5，batch size=2，FP32 训练。
- 推理采用滑动窗口（overlap 0.5，高斯权重融合）。

## 4. 资源与算力

- **硬件**：8 × NVIDIA H100 80 GB GPU（预训练），单张 H100 用于下游训练和推理。
- **训练时长**：预训练阶段约 **7 天**（8 GPU），各下游任务训练 300‑500 epoch 不等。
- **模型参数量与显存**：最优配置 170.1M 参数，推理时显存占用约 11.1 GB，比多数 Transformer 方法低，但推理速度比 SegMamba 慢约 30%（延迟约 1770 ms 标准化的 1.5 倍）。

## 5. 实验数量与充分性

论文进行了**大量且多维度**的实验，整体充分且具备可比性：

- **5 个数据集 × 多组对比**：主实验覆盖 CT、MRI、超声、胎儿 MRI，每种对比 8‑9 个方法，并提供预训练版本。
- **消融实验**（附录 D）：
  - 专家数量（4种配置）
  - 组大小（K）（4种）
  - 每个专家的槽数（S=1,2,4,8）
  - 归一化方法（DyT vs. LayerNorm）
  - HoME 层的必要性（定性对比图）
- **泛化分析**：单模态训练、CT→MRI 迁移、联合多模态训练、跨模态迁移至超声，均提供详细表格。
- **统计检验**：使用 Wilcoxon 符号秩检验（p<0.05）验证显著性。
- 所有实验均在统一框架下复现，预训练模型与从头训练分别报告，确保了客观与公平。

## 6. 主要结论与发现

- Mamba‑HoME 在所有公开数据集和内部数据集上均**达到最优或次优性能**，尤其在小目标（PDAC）和边界精度（HD95）上优势明显。
- 预训练可进一步提升效果（如 PANORAMA 上 mDSC 从 77.5% 提至 78.2%，PDAC DSC 从 54.8% 提至 56.7%）。
- 模型在 CT、MRI、US 间展现出较强的跨模态泛化能力，表明其学习到了模态无关的层次特征。
- 相较于 Transformer 方法，Mamba‑HoME 在长序列处理上保持线性复杂度，显存占用低，兼具精度与效率。

## 7. 优点

- **新颖的层次化 MoE 设计**：将令牌分组与两级路由相结合，有效模拟局部到全局的空间层次，提升了分割质量。
- **Mamba + MoE 的创新融合**：首次在三维医学图像中将状态空间模型与软混合专家深度集成，平衡了长程依赖与局部适应性。
- **计算效率**：线性复杂度使其能处理百万级令牌，且显存占用较低，利于高分辨率实际部署。
- **全面的实验验证**：涵盖三种模态、多个解剖结构、多种训练策略，对比丰富，消融详尽，结论可靠。
- **开源代码与可复现性**：提供了代码和详细实现说明，方便社区复现与扩展。

## 8. 不足与局限

- **未探索超大规模预训练**：当前预训练仅使用约 9,400 例扫描，未验证在 >10,000 甚至 >200,000 级别上的伸缩性。
- **缺乏自监督预训练研究**：仅实验了监督预训练，未探索自监督学习对大模型能力的进一步挖掘潜力。
- **参数量较大**（170.1M），虽显存小但推理延迟稍高（比基线慢约 30%），在实时性要求极高的场景可能需要进一步优化。
- **专家数和槽数等超参数需按阶段设定**，尚未证明可自动配置，可能需要对不同任务手动调参。
- **实验局限于医学图像分割**，未展示在其他长序列任务（如视频、点云）中的通用性。
- **内部 CT 数据集较小**（60 例），且未披露其具体来源细节，可能引入一定的选择偏差。

（完）
