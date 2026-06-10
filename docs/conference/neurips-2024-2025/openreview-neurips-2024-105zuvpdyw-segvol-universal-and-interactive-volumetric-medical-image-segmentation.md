---
title: "SegVol: Universal and Interactive Volumetric Medical Image Segmentation"
title_zh: SegVol：通用交互式三维医学图像分割大模型
authors: "Yuxin Du, Fan BAI, Tiejun Huang, Bo Zhao"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=105ZuvpdyW"
tags: ["query:abdk-seg"]
score: 8.0
evidence: SegVol是一个三维医学图像分割基础模型，使用9万无标注和6千标注CT体积训练，可分割200余类解剖结构，涵盖腹部器官，直接面向腹部CT多器官分割任务。
tldr: 针对三维医学图像分割缺乏通用基础模型的问题，本文提出SegVol，一个基于大规模CT数据训练的通用交互式分割框架。模型使用9万个无标注和6千个标注CT体积进行训练，支持通过文本或空间提示分割超过200种解剖结构。创新性的zoom-out-zoom-in滑动窗口策略在保证全局感受野的同时实现高效推理。在多个腹部器官分割基准上，SegVol展现出强大的零样本和微调性能，为全监督腹部CT多器官分割提供了先进的深度学习基座。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1059, \"height\": 1031, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1433, \"height\": 752, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1420, \"height\": 477, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1282, \"height\": 490, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1267, \"height\": 756, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1394, \"height\": 900, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1405, \"height\": 959, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1129, \"height\": 803, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1423, \"height\": 513, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1427, \"height\": 974, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1338, \"height\": 2162, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1313, \"height\": 2166, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1324, \"height\": 2175, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1416, \"height\": 1662, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1429, \"height\": 1678, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1416, \"height\": 1664, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1426, \"height\": 462, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-105zuvpdyw/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1400, \"height\": 1678, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-105zuvpdyw/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1319, \"height\": 322, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-105zuvpdyw/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1414, \"height\": 946, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-105zuvpdyw/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 986, \"height\": 216, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-105zuvpdyw/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1382, \"height\": 1321, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-105zuvpdyw/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1373, \"height\": 336, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-105zuvpdyw/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1359, \"height\": 1457, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-105zuvpdyw/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1427, \"height\": 974, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-105zuvpdyw/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1425, \"height\": 169, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-105zuvpdyw/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1465, \"height\": 672, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-105zuvpdyw/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 692, \"height\": 2378, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-105zuvpdyw/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1301, \"height\": 1832, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-105zuvpdyw/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1462, \"height\": 174, \"label\": \"Table\"}]"
motivation: 现有医学图像分割模型通常是任务特定、器官特定的，缺乏三维通用基础分割模型，且用户交互困难。
method: 构建基于ViT的大规模三维分割模型SegVol，采用zoom-out-zoom-in策略，结合语义和空间提示实现通用交互分割。
result: 在腹部CT等多器官分割任务上，SegVol实现了200+解剖结构的准确分割，零样本和微调结果均领先。
conclusion: SegVol作为通用三维医学分割基础模型，显著推动了腹部器官全监督分割等任务的性能上限与临床易用性。
---

## Abstract
Precise image segmentation provides clinical study with instructive information. Despite the remarkable progress achieved in medical image segmentation, there is still an absence of a 3D foundation segmentation model that can segment a wide range of anatomical categories with easy user interaction. In this paper, we propose a 3D foundation segmentation model, named SegVol, supporting universal and interactive volumetric medical image segmentation. By scaling up training data to 90K unlabeled Computed Tomography (CT) volumes and 6K labeled CT volumes, this foundation model supports the segmentation of over 200 anatomical categories using semantic and spatial prompts. To facilitate efficient and precise inference on volumetric images, we design a zoom-out-zoom-in mechanism. Extensive experiments on 22 anatomical segmentation tasks verify that SegVol outperforms the competitors in 19 tasks, with improvements up to 37.24\% compared to the runner-up methods. We demonstrate the effectiveness and importance of specific designs by ablation study. We expect this foundation model can promote the development of volumetric medical image analysis. The model and code are publicly available at https://github.com/BAAI-DCAI/SegVol.

---

## 论文详细总结（自动生成）

# SegVol: 通用交互式三维医学图像分割大模型 论文总结

## 1. 研究动机与核心问题
- **核心问题**：现有医学图像分割方法多为任务或器官专用模型，缺乏一个能覆盖多种解剖结构、支持自然用户交互的**三维通用分割基础模型**。尤其面临标签空间不一致、标注数据稀缺、复杂结构（如肿瘤）分割能力差以及推理计算成本高等挑战。
- **整体含义**：本文旨在构建一个“Segment Anything”式的三维医学分割基础模型 **SegVol**，通过对大规模CT数据的预训练与微调，实现对 **200+ 解剖类别** 的通用、交互式分割，大幅降低使用门槛并提升在开放场景下的鲁棒性。

## 2. 方法论与关键技术
- **数据集构建**：
  - 收集了 **25 个公开CT分割数据集**，涵盖腹部、胸部、头颈、骨盆等区域，共 **6K 已标注CT体积**，标签超过 150K 个分割掩膜。
  - 为缓解“部分标签”问题，利用 **Felzenswalb-Huttenlocher (FH)** 无监督算法生成伪标签以补充未标注类别，并通过多步后处理（滤除极小区域、膨胀/腐蚀等）降低噪声。
  - 额外收集 **90K 无标注CT** 用于自监督预训练。
- **模型架构**：
  - **图像编码器**：采用 **3D ViT**（12层，768维隐藏向量），输入尺寸为 (D,H,W) 体积，经补丁嵌入后提取特征。
  - **文本编码器**：使用 **冻结的CLIP文本编码器**，将解剖名称转换为文本嵌入，以实现“语义提示”并通过跨数据集统一标签空间。
  - **空间提示编码器**：对点 (point) 和边界框 (bbox) 进行位置编码，输出空间提示嵌入。
  - **掩膜解码器**：通过自注意力与双交叉注意力融合图像嵌入和提示嵌入，经转置卷积与插值生成预测掩膜。文本信息通过一条**并行强化分支**进一步增强。
- **Zoom-out-Zoom-in 机制**：
  - **Zoom-out**：将整个体积下采样后进行全局粗分割，得到低分辨率掩膜。
  - **Zoom-in**：根据粗掩膜确定感兴趣区域 (ROI)，在原始高分辨率体积上使用滑窗进行精细分割，最后将细化结果回填至粗掩膜。
  - 训练阶段通过“多尺寸训练”模拟两种视野，使模型同时适应全局与局部推理。
- **训练策略**：
  - **预训练**：在 96K CT 上用 SimMIM 方法训练图像编码器，掩蔽图像建模损失 \(L_{\text{pre-training}}\)。
  - **微调**：在 25 个标注数据集上结合二值交叉熵损失与 Dice 损失进行全参数微调（文本编码器冻结），损失函数为 \(L_{\text{fine-tuning}} = L_{\text{BCE}} + L_{\text{Dice}}\)。
  - 训练时，对每例样本随机生成多种提示类型组合（point, bbox, text 及它们的复合），并混合使用真实标注与伪标签的监督信号。

## 3. 实验设计与对比方法
- **主要评估任务**：
  - **22 项三维分割任务**，覆盖器官与病灶，包括 **AMOS22** (15个腹部器官)、**Universal Lesion Segmentation Challenge 23 (ULS23)**（三类病灶）、**SegTHOR**（4个胸部器官）等外测数据集。
- **对比方法**：
  - 典型SAM类交互模型：**SAM (point/bbox)**、**MedSAM**、**SAM-Med2D**、**SAM-Med3D**。
  - 传统专用分割模型：**3DUX-Net**、**SwinUNETR**、**nnU-Net**（在论文补充实验中对比）。
- **评估指标**：Dice 相似系数，报告中位数、四分位数等统计信息以体现分布。
- **消融实验**：
  - **Zoom-out-zoom-in 机制**：对比仅缩放、常规滑窗与所提方案。
  - **训练数据规模**：从 1 个数据集逐步增加到 25 个，锚定 BTCV 验证集。
  - **多提示组合**：对比纯文本、纯空间、文本+空间等不同提示模式的性能。

## 4. 资源与算力
- **硬件**：使用 **8 块 NVIDIA A100-SXM4-40GB GPU**。
- **训练时长**：
  - 预训练阶段：约 **20 × 8 GPU 小时** （即 160 GPU小时）。
  - 微调阶段：约 **300 × 8 GPU 小时** （即 2400 GPU小时），共270个epoch，batch size = 32，输入裁剪尺寸为 (32, 256, 256)。
- 推理时延对比显示，zoom-out-zoom-in 机制平均每例耗时仅 **190 毫秒**，远低于全分辨率滑窗（约3331毫秒），性能还更优。

## 5. 实验规模与充分性
- 实验设计较为全面，包含：
  - **主对比实验**：在 3 个外测数据集共 22 项分割任务上与 5 种 SAM 类方法横向对比，提供详细统计分布。
  - **补充对比**：与 3 种顶尖任务专用模型在 10 个器官/病灶任务上比较。
  - **消融实验**：针对 zoom-out-zoom-in、数据规模、提示类型分别进行定量分析。
  - **扩展研究**：Cross‑modality 泛化（在 MRI 上测试）、小样本微调、语义歧义消除定性展示。
- 实验设置公平：所有对比方法均为开源，测试时模型冻结，采用统一的后处理与评估协议。
- 实验数量充足，统计报告较详细（中位数、四分位数、小提琴图），消融和案例分析增强了结论可信度。

## 6. 主要结论与发现
- SegVol 在 **19/22 项任务上超越所有对比的 SAM 类方法**，部分任务领先第二名高达 **37.24%**（平均 Dice 在 AMOS22 上较 SAM-Med2D 提升 19.25%）。
- 与 nnU‑Net 等任务专用方法相比，SegVol 在**病灶分割**上展现明显优势（平均 Dice 高出 14.76%），且跨数据集泛化性更强。
- 语义提示可有效消除空间提示的歧义，复合提示（如“bbox+text”）相较纯文本或纯空间提示大幅提升分割精度。
- 数据规模定律在三维医学分割中成立，随着训练数据增加，SegVol 性能持续提升，尚未饱和。

## 7. 论文优点
- **首创性**：提出首个支持语义+空间提示的通用三维医学图像分割基础模型，类别覆盖超 200 种。
- **工程系统性**：整合 25 个异构公开数据集并引入伪标签机制，解决了部分标签障碍。
- **高效推理设计**：zoom-out-zoom-in 机制在保持高精度的同时将推理时间从滑窗的秒级降至毫秒级，实用性强。
- **开放与可复现**：模型与代码开源，所有数据均为公开资源，实验设定详细，便于复现。
- **泛化能力**：仅在 CT 上训练即可直接分割 MRI，展示出对解剖结构的深层理解。

## 8. 不足与局限
- **MR 性能待提升**：尽管显示跨模态泛化能力，但未在 MRI 上进行微调，分割精度显著低于 CT，未来需多模态联合训练。
- **复杂语义理解不足**：目前仍难以处理需要复杂空间关系和逻辑推理的“指代表达分割”，尚未充分利用自然语言描述包含的细粒度信息。
- **伪标签噪声**：FH 算法生成的伪标签质量有限，虽经后处理但仍可能引入噪声，影响部分类别分割质量。
- **像素级扩展**：模型主要面向类别级分割，未深入探讨实例级分割或极少样本的自适应问题。
- **微小病灶**：在处理 ULS23 的 patch 状病灶时，其优势不明显，性能与 MedSAM 接近，对极小目标的定位精度尚有提升空间。

（完）
