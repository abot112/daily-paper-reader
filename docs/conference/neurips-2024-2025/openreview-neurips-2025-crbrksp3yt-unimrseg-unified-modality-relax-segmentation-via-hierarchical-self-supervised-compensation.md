---
title: "UniMRSeg: Unified Modality-Relax Segmentation via Hierarchical Self-Supervised Compensation"
title_zh: 统一模态松弛分割网络：通过分层自监督补偿实现
authors: "Xiaoqi Zhao, Youwei Pang, Chenyang Yu, Lihe Zhang, Huchuan Lu, Shijian Lu, Georges El Fakhri, Xiaofeng Liu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=CrBRKsP3yT"
tags: ["query:abdk-seg"]
score: 4.0
evidence: 提出统一模态松弛分割网络（UniMRSeg），通过分层自监督补偿处理缺失模态，是一种适用于医学影像的深度学习分割模型。
tldr: 针对多模态分割中模态缺失导致性能下降的问题，本文提出统一模态松弛分割网络UniMRSeg，通过分层自监督补偿机制在输入、特征和输出三个层次弥合模态间表示差异。该方法无需为每种模态组合训练独立模型，降低了部署成本，在多个医学影像分割数据集上展现出对模态缺失的鲁棒性，为多模态医学影像分析提供了灵活高效的解决方案。实验证实，UniMRSeg在脑肿瘤分割等任务中取得了与完整模态相当的性能。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-crbrksp3yt/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1439, \"height\": 772, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-crbrksp3yt/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 702, \"height\": 313, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-crbrksp3yt/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1436, \"height\": 843, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-crbrksp3yt/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1421, \"height\": 728, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-crbrksp3yt/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1454, \"height\": 334, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1448, \"height\": 507, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1444, \"height\": 214, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 731, \"height\": 407, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 646, \"height\": 142, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 649, \"height\": 192, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1450, \"height\": 563, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1450, \"height\": 644, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 659, \"height\": 106, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-crbrksp3yt/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 620, \"height\": 177, \"label\": \"Table\"}]"
motivation: 多模态分割在临床中常面临模态缺失问题，现有方法需为每种模态组合训练单独模型，部署复杂。
method: 提出分层自监督补偿，通过模态重建和表示对齐，在输入、特征、输出三层统一处理模态缺失。
result: 在多个医学影像数据集上，UniMRSeg对模态缺失具有高鲁棒性，性能接近完整模态训练。
conclusion: UniMRSeg为多模态医学分割提供了统一且高效的模型，显著降低了实际部署中的模型维护成本。
---

## Abstract
Multi-modal image segmentation faces real-world deployment challenges from incomplete/corrupted modalities degrading performance. While existing methods address training-inference modality gaps via specialized per-combination models, they introduce  high deployment costs by requiring exhaustive model subsets and model-modality matching. In this work, we propose a unified modality-relax segmentation network (UniMRSeg) through hierarchical self-supervised compensation (HSSC). Our approach hierarchically bridges representation gaps between complete and incomplete modalities across input, feature and output levels. 
First, we adopt modality reconstruction with the hybrid shuffled-masking augmentation, encouraging the model to learn the intrinsic modality characteristics and generate meaningful representations for missing modalities through cross-modal fusion.  
Next, modality-invariant contrastive learning implicitly compensates the feature space distance among incomplete-complete modality pairs.  Furthermore, the proposed lightweight reverse attention adapter explicitly compensates for the weak perceptual semantics in the frozen encoder. Last, UniMRSeg is fine-tuned under the hybrid consistency constraint to ensure stable prediction under all modality combinations without large performance fluctuations. Without bells and whistles, UniMRSeg significantly outperforms the state-of-the-art methods under diverse missing modality scenarios on MRI-based brain tumor segmentation, RGB-D semantic segmentation, RGB-D/T salient object segmentation.  The code will be released at \url{https://github.com/Xiaoqi-Zhao-DLUT/UniMRSeg}.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

- **研究动机**：视觉多模态图像分割（如脑肿瘤MRI、RGB-D/RGB-T场景理解）在实际部署中常因传感器故障、临床约束等出现模态不完整或缺失，导致分割性能严重下降。
- **现有方法局限**：主流方案为每种可能的模态组合训练独立模型或专用分支，不仅引入高昂的部署与维护成本，还需额外的模态识别步骤，难以实现统一的推理。
- **本文目标**：提出**统一模态松弛分割网络 (UniMRSeg)**，仅用一组参数即能处理任意模态组合输入，并从输入、特征、输出三个层次进行自监督补偿，弥合完整模态与缺失模态之间的表示差异，在保证高精度的同时大幅降低部署复杂度。

### 2. 论文提出的方法论

核心思想是**分层自监督补偿 (Hierarchical Self-Supervised Compensation, HSSC)**，通过三阶段训练逐步消除模态缺失带来的表示偏差：

- **阶段一：多粒度模态重建（输入层补偿）**
  - **数据扰动**：对完整多模态输入随机执行模态丢弃（50%概率）、模态混洗、空间掩码三种操作，破坏固定模态顺序并模拟缺失效应。
  - **重建任务**：将扰动后的数据送入3D U‑Net风格的重建网络，恢复原始完整模态，损失函数为 L1 + SSIM，以自监督方式学习跨模态内在特征和融合能力。

- **阶段二：模态不变对比学习（特征层补偿）**
  - **表示构建**：对同一样本生成完整模态版本与随机缺失版本，通过编码器提取多级特征并全局平均池化得到向量集。
  - **对比学习**：以完整样本与其缺失版本为正对，不同源样本为负对，在编码器5个特征层级联合优化 NT‑Xent 损失，拉近同一样本不同模态组合的特征空间距离；同时施加 Dice 分割损失，引导特征向语义分割目标聚类。

- **阶段三：不完整模态自适应微调（输出层补偿）**
  - **逆向注意力适配器 (Reverse Attention Adapter)**：在冻结的编码器各阶段旁路加入轻量适配器，利用3D Swin Transformer捕捉跨模态高响应互注意力，通过逆向注意力图突出缺失模态与完整模态的差异信息，补偿弱感知语义。
  - **混合一致性约束**：对完整模态与所有可能缺失组合（MRI下14种）同时前向传播，强制其特征级（L1距离）和预测级（Dice损失）与完整模态参考保持一致，只微调解码器和适配器参数。
  - **最终目标**：使模型在推理时，无论输入何种模态组合，都能输出接近完整模态质量的稳定预测。

### 3. 实验设计

- **数据集与场景**：
  - **脑肿瘤分割**：BraTS2020（369例，4模态MRI：Flair、T1ce、T1、T2，3个肿瘤区域），训练/验证/测试分割为315/17/37。
  - **RGB‑D显著物体分割**：训练集 NJUD (1485) + NLPR (700)，测试集 STERE (1000对)。
  - **RGB‑T显著物体分割**：训练集 VT5000 (2500)，测试集 VT1000 (1000对)。
  - **RGB‑D语义分割**：SUN‑RGBD (37类，5285训练/5050测试)。

- **基准对比方法**：
  - 脑肿瘤：NestedFormer, SFusion, ShaSpec, PASSION, RFNet, mmFormer, M3AE, M3FeCon。
  - 显著物体与语义分割：SSLSOD, CAVER, PopNet, GateNet, LSNet, CONTRINET, TokenFusion, CMX, CMXNeXt, MaskMentor。
  - 统一采用缺失模态设定（MRI缺失填0，RGB‑D/T缺失拷贝另一模态），部分方法运用深度估计、知识蒸馏等。

- **评价指标**：Dice（脑肿瘤）、S‑measure（显著物体检测）、IoU（语义分割），同时报告各模态组合的性能均值及标准差。

### 4. 资源与算力

- **硬件与优化器**：所有实验在**一块 NVIDIA A800 GPU**上完成，使用 AdamW 优化器，初始学习率 1e‑4，权重衰减 1e‑5，训练 300 个 epoch，采用热身调度。
- **其他细节**：论文未提供单次训练的具体时长（小时/天级）的总算力消耗，仅说明统一骨干网络和轻量适配器，参数量与FLOPs在文中已与对比方法进行效率比较（如参数87MB vs. RFNet 34MB, mmFormer 106MB等），但未量化总体训练计算量。

### 5. 实验数量与充分性

- **实验规模**：涵盖4个不同任务、多种模态组合（MRI 15种，RGB‑D 3种，RGB‑T 3种），对比了多达十余种前沿方法。
- **消融研究**：
  - 逐组件消融：验证三种数据扰动、对比学习、分割约束、适配器、预测一致性等各自贡献。
  - 三阶段设计 vs 统一单阶段训练。
  - 逆向注意力适配器内部（逆向注意力、互注意力、3D Swin Transformer）及编码器冻结策略。
  - 层次补偿机制的单级、两级、三级组合消融。
  - 对推理时模态混洗顺序鲁棒性测试。
  - 可视化特征层响应，展示补偿过程。
- **公平性**：复现方法均采用公开代码，缺失模态处理保持一致；附录补充了BraTS2020、BraTS2018不同数据划分下的对比，结果稳定一致。实验设计充分、客观，多角度验证了方法的有效性。

### 6. 论文的主要结论与发现

- UniMRSeg 以 **单一模型、统一参数** 即可应对任意模态缺失，在所有对比方法中获得最高的平均分割精度和最低的性能标准差。
- 三阶段分层补偿机制（输入级重建、特征级对比学习、输出级适配与一致性蒸馏）具有**强互补性**，共同将缺模态性能提升至接近全模态上界，且优于仅用某个层面的补偿。
- 逆向注意力适配器通过“反向”强调差异语义，能准确弥补缺失模态带来的弱感知区域，配合互注意力与3D Swin Transformer进一步增强了跨模态建模能力。
- 模态混洗与多粒度掩码迫使模型学习模态无关的表征，提升了对输入顺序和缺失模式的鲁棒性。

### 7. 优点

- **实用性强**：统一框架消除了多模型部署与模态识别的需求，大幅降低实际系统维护成本。
- **方法论创新**：首次将像素级重建、对比学习与知识蒸馏自监督范式有机整合为分层的模态补偿方案，而非孤立使用。
- **适配器设计巧妙**：轻量逆向注意力适配器冻结编码器，仅微调少量参数实现有效补偿，兼具效率与效果。
- **实验全面**：覆盖医学图像与自然图像、2D与3D、多类任务和大量基准方法，消融和可视化详尽，结果具有说服力。
- **性能突出**：在多种缺失场景下均取得最优均值与最小方差，泛化性出色。

### 8. 不足与局限

- **训练流程复杂**：三阶段训练增加了流程控制和时间成本，论文也指出简化训练是未来方向（如课程学习、参数高效微调）。
- **算力需求未明确**：虽仅用一块A800，但多阶段训练的总时间未汇报，实际复现门槛未知。
- **模态混洗依赖**：虽然实验中验证了混洗带来的鲁棒性，但在某些严格有序输入的场景下可能引入不必要的扰动。
- **极端缺失情况**：单一模态输入时性能仍明显低于全模态（如表1），多模态补偿能力存在上限。
- **社会影响与伦理**：论文标注无负面社会影响，但医学图像分割直接关联临床辅助诊断，若模型用于高风险决策，需进一步验证安全性和公平性。

（完）
