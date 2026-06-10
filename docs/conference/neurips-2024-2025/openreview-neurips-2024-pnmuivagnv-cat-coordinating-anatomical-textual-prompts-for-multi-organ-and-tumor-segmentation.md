---
title: "CAT: Coordinating Anatomical-Textual Prompts for Multi-Organ and Tumor Segmentation"
title_zh: CAT：协调解剖-文本提示的多器官与肿瘤分割
authors: "Zhongzhen Huang, Yankai Jiang, Rongzhao Zhang, Shaoting Zhang, Xiaofan Zhang"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=pnmUiVAGnv"
tags: ["query:abdk-seg"]
score: 9.0
evidence: 提出CAT，协调解剖与文本提示进行多器官及肿瘤分割
tldr: 医学图像中多器官和肿瘤分割的挑战在于异常形态多变，现有单提示方法不足。CAT提出双提示框架，结合3D裁剪图像的解剖视觉提示和医学专有文本提示，协调互补信息。实验表明在多个数据集上达到最优分割性能，为多器官和肿瘤分割提供了统一的交互式解决方案。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-pnmuivagnv/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1447, \"height\": 438, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pnmuivagnv/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1441, \"height\": 534, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pnmuivagnv/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1439, \"height\": 691, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pnmuivagnv/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1444, \"height\": 305, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pnmuivagnv/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1440, \"height\": 385, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-pnmuivagnv/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1341, \"height\": 1987, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-pnmuivagnv/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1445, \"height\": 353, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-pnmuivagnv/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1452, \"height\": 367, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-pnmuivagnv/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1436, \"height\": 434, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-pnmuivagnv/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1438, \"height\": 195, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-pnmuivagnv/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1441, \"height\": 476, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-pnmuivagnv/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1446, \"height\": 331, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-pnmuivagnv/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1451, \"height\": 284, \"label\": \"Table\"}]"
motivation: 现有医学图像分割方法对多器官和肿瘤的异常形态处理不足，单提示方式无法满足复杂临床需求。
method: 提出双提示框架CAT，融合3D解剖视觉提示与医学增强文本提示，协调互补信息进行分割。
result: 实验显示在多器官和肿瘤分割任务上达到最先进性能，且优于单一提示方法。
conclusion: CAT通过协调双提示有效提升了多器官及肿瘤分割的准确率，为复杂医学分割提供新范式。
---

## Abstract
Existing promptable segmentation methods in the medical imaging field primarily consider either textual or visual prompts to segment relevant objects, yet they often fall short when addressing anomalies in medical images, like tumors, which may vary greatly in shape, size, and appearance. Recognizing the complexity of medical scenarios and the limitations of textual or visual prompts, we propose a novel dual-prompt schema that leverages the complementary strengths of visual and textual prompts for segmenting various organs and tumors. Specifically, we introduce $\textbf{\textit{CAT}}$, an innovative model that $\textbf{C}$oordinates $\textbf{A}$natomical prompts derived from 3D cropped images with $\textbf{T}$extual prompts enriched by medical domain knowledge. The model architecture adopts a general query-based design, where prompt queries facilitate segmentation queries for mask prediction. To synergize two types of prompts within a unified framework, we implement a ShareRefiner, which refines both segmentation and prompt queries while disentangling the two types of prompts. Trained on a consortium of 10 public CT datasets, $\textbf{\textit{CAT}}$ demonstrates superior performance in multiple segmentation tasks. Further validation on a specialized in-house dataset reveals the remarkable capacity of segmenting tumors across multiple cancer stages. This approach confirms that coordinating multimodal prompts is a promising avenue for addressing complex scenarios in the medical domain.

---

## 论文详细总结（自动生成）

# CAT：协调解剖-文本提示的多器官与肿瘤分割 论文深度总结

## 1. 研究动机与核心问题
- **背景**：医学图像中多器官与肿瘤分割面临异常形态多变、数据长尾分布等挑战。现有可提示分割方法通常仅依赖单一模态提示（文本或视觉），难以同时处理器官与多样化肿瘤。
- **核心问题**：
  - 文本提示虽可提供语义概念，但因数据稀缺导致视觉-文本对齐学习困难，对稀有异常（如肿瘤）泛化差。
  - 视觉提示（如边界框、点）虽直观，但缺乏对目标的通用概念描述，难以应对肿瘤形态的巨大变异（不同分期、密度、侵袭表现）。
- **整体含义**：提出一种**协调解剖-文本双提示**的自动分割模型，利用两种提示的互补性，提升多器官和肿瘤分割的鲁棒性与泛化能力。

## 2. 方法论
### 2.1 核心思想
- 设计**解剖提示（Anatomical Prompts）**：从3D CT图像中裁剪的解剖结构体积作为视觉提示，提供直观、视觉一致的参照。
- 设计**文本提示（Textual Prompts）**：调用GPT-4生成、经医生修正的富含医学知识的长文本描述，传达目标的综合概念。
- 通过**ShareRefiner**和**PromptRefer**模块融合两种提示，并在查询层面进行对比对齐，使分割查询聚焦对应提示。

### 2.2 关键技术细节
- **视觉骨干**：Swin UNETR 提取多尺度特征 `V`，并通过解码器生成高分辨率像素嵌入图 `O`。
- **提示编码器**：
  - 解剖编码器 `Enc_A` 将裁剪体积 `P_A` 编码为嵌入，线性投影得解剖查询 `Q_A`。
  - 文本编码器（Clinical-BERT）将文本 `P_T` 编码，取 `[CLS]` 输出经线性投影得文本查询 `Q_T`。
- **ShareRefiner**：
  - 对分割查询 `Q_S` 和文本查询 `Q_T` 使用软分配跨注意力（普通交叉注意力）。
  - 对解剖查询 `Q_A` 使用**硬分配**（Gumbel-Softmax + Straight-Through），确保每个解剖查询关注互不重叠的视觉区域，实现解耦。
  - 公式：硬分配相似度 `S_i_gumbel` 经 Gumbel-Softmax 后取 one-hot，再用 straight-through trick 计算 `S'`。
- **PromptRefer**：
  - 通过自定义注意力掩码，将特定提示查询组（如器官本身的解剖、文本查询）分配给对应分割查询，使分割查询仅与相关提示交互。
  - 输出 `O_S` 用于预测掩码。
- **对比对齐**：
  - 使用 InfoNCE 损失实现分割查询到提示查询（`L_s2p`）和提示查询之间（`L_p2p`）的对齐，促进知识融合。
- **训练策略**：
  - 解剖提示：从数据集掩码的边界框中随机采样同类实例作为正提示，排除本身。
  - 文本提示：正类别使用长描述，负类别随机抽取短模板短语。
- **最终损失**：`L_total = L_dice + L_cls + L_s2p + L_p2p`。

### 2.3 整体流程（文字版）
1. 输入3D CT体积 `I`，视觉骨干提取多尺度特征并生成像素嵌入图 `O`。
2. 解剖提示（裁剪体积）、文本提示分别编码并投影为 `Q_A`、`Q_T`。
3. 可学习分割查询 `Q_S` 与 `Q_A`、`Q_T` 一同送入 ShareRefiner，与多尺度特征交互（硬/软分配）得到 `Q'_S`、`Q'_A`、`Q'_T`。
4. PromptRefer 使用掩码引导交叉注意力更新 `Q'_S` 得到 `O_S`。
5. `O_S` 与 `O` 点积 + Sigmoid 生成 N 个二值掩码。
6. 计算分类、Dice 和对比损失。

## 3. 实验设计
### 3.1 数据集
- **训练集**：10个公开腹部CT数据集合成（BTCV、CT-ORG、AbdomenCT-1K、CHAOS、AMOS22、WORD、Pancreas-CT、LiTS、KiTS、MSD部分）。涵盖23个器官和6种异常。
- **测试集**：
  - 器官分割：FLARE22 外部测试集（13个器官）。
  - 肿瘤分割：MSD 中腹部相关肿瘤任务（肝、胰腺、肝血管、结肠）以及一个内部数据集（80例结肠癌，I-IV期）。
- **内部结肠癌数据集**：80例，标注分期（T1-T4），大小、形态各异。

### 3.2 Benchmark与对比方法
- **器官分割**：对比 SAM、MedSAM、SAM-Med2D、SAM-Med3D、SegVol、CT-SAM3D、Universal (CLIP驱动)、ZePT 等。
- **肿瘤分割**：对比 nnUNet、Swin UNETR、SAM-Med3D、SegVol、Universal、ZePT。
- 评估指标：Dice相似系数 (DSC) 和 95% Hausdorff 距离 (HD95)。

### 3.3 实验结果亮点
- **器官分割**：CAT 平均DSC达 86.8%，超过大部分纯视觉或纯文本提示模型，尤其在胰腺（+5.6% DSC vs Universal）、十二指肠等困难器官上提升显著。
- **肿瘤分割**：在 MSD 四类肿瘤上平均DSC 72.73%，全面优于 nnUNet、Swin UNETR 和文本提示模型。在内部结肠癌数据集上，T4期肿瘤DSC达57.37%，远高于对比方法（至少+7% DSC）。
- 可视化显示 CAT 能更完整覆盖复杂肿瘤（如侵袭邻近组织），减少误分割。

## 4. 资源与算力
- 文中明确提到：训练使用 **8 张 NVIDIA A100 GPU**。
- 未详细说明训练总时长、每GPU显存占用或 batch size 等具体配置，但提到使用 AdamW 优化器，初始学习率 1e-4，patch 尺寸 96³，数据增强（随机平移、缩放、尺度变换）。

## 5. 实验数量与充分性
- **主要实验数量**：
  - 2个公开测试集（器官、肿瘤各一） + 1个内部数据集，共3个测试场景。
  - 对比方法涵盖传统分割（nnUNet）、视觉提示（多种 SAM 变体）、文本提示（Universal, ZePT）三大类，总数超过10个。
  - 消融实验：逐步加入解剖/文本提示、硬分配、注意力掩码、对比损失等模块，共4组变体+5行结果（Table 3的9行消融）。
  - 定性分析：t-SNE可视化（提示分布）、热力图对比、分割结果可视化（多例）。
- **充分性评估**：实验设计覆盖器官和多种肿瘤，包含外部和内部数据，对比了最新基线，消融分解了每个关键组件的作用，定性分析辅助理解，实验充分且客观。对比时均使用统一训练数据和评估方式（对现有方法重新训练或使用官方权重），保证了公平性。

## 6. 主要结论与发现
- **双提示互补**：解剖提示提供外观细节，文本提示传达语义概念，两者协同有效解决单一提示的局限。
- **性能提升**：CAT 在多个多器官和肿瘤分割基准上取得 SOTA 性能，尤其在困难器官和变异肿瘤上提升明显。
- **泛化能力**：模型在未见过的肿瘤分期（T4）上表现优异，证明其对复杂临床场景的鲁棒性。
- **模块贡献**：硬分配用于解剖查询、PromptRefer 的掩码机制、对比对齐均对性能有正向贡献，且相互配合效果最佳。

## 7. 优点
- **创新性强**：首次在3D医学图像分割中系统性地协调解剖体积（视觉）和领域知识增强文本双重提示。
- **自动且无交互**：无需人工提供提示，全自动运行，更贴近临床实际。
- **架构设计精巧**：ShareRefiner 对不同查询采用差异化解耦策略，PromptRefer 实现精准提示分配。
- **实验扎实**：训练集涵盖10个公开数据集，测试覆盖外部数据和真实复杂肿瘤分期，与多个基线公平对比。
- **可解释性**：通过 t-SNE 和注意力热力图展示提示如何分离和聚焦，增强了模型透明性。

## 8. 不足与局限
- **解剖编码器依赖预训练模型**：解剖提示编码器基于现有 CT 预训练模型，其初始嵌入分布仍较混乱，可能限制性能上限；论文也承认需进一步研究更好的 CT 基础模型。
- **罕见病变与解剖变异风险**：当遇到极端罕见的病变类型或术后解剖结构剧变时，分割仍可能出错（结论部分提及）。
- **实验覆盖范围**：目前仅集中在腹部CT，未涉及其他部位（如脑、肺）或其他模态（MRI），泛化到更多场景有待验证。
- **资源需求**：训练需8张A100，具体时长未披露，对大模型训练的门槛未详细讨论。
- **内部数据集规模**：内部结肠癌数据集仅80例，尽管分期多样性，但样本量较小，结论普适性需更大规模验证。

（完）
