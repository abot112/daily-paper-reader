---
title: "LoMix: Learnable Weighted Multi-Scale Logits Mixing for Medical Image Segmentation"
title_zh: LoMix：医学图像分割中可学习的加权多尺度logit混合
authors: "Md Mostafijur Rahman, Radu Marculescu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=87c2JwNJa0"
tags: ["query:abdk-seg"]
score: 8.0
evidence: 引入LoMix，可学习多尺度logit混合模块，提升全监督医学图像分割训练
tldr: U型网络输出多尺度logit，但训练往往忽略粗细混合的互补线索。LoMix是一种受神经架构搜索启发的可微分模块，自动学习加权混合多尺度logit并引导训练。在多个医学分割数据集上，LoMix即插即用，持续提升Dice系数，表明混合尺度监督对精确分割至关重要。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-87c2jwnja0/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1435, \"height\": 423, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-87c2jwnja0/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1304, \"height\": 484, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-87c2jwnja0/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1306, \"height\": 512, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-87c2jwnja0/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1310, \"height\": 487, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-87c2jwnja0/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1311, \"height\": 556, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-87c2jwnja0/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1434, \"height\": 589, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-87c2jwnja0/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1407, \"height\": 796, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-87c2jwnja0/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1443, \"height\": 570, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-87c2jwnja0/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1443, \"height\": 572, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-87c2jwnja0/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1444, \"height\": 572, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-87c2jwnja0/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1445, \"height\": 580, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-87c2jwnja0/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1443, \"height\": 572, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-87c2jwnja0/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1397, \"height\": 1785, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-87c2jwnja0/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1456, \"height\": 886, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-87c2jwnja0/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1107, \"height\": 752, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-87c2jwnja0/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1455, \"height\": 398, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-87c2jwnja0/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1453, \"height\": 682, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-87c2jwnja0/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1452, \"height\": 230, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-87c2jwnja0/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1183, \"height\": 712, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-87c2jwnja0/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1335, \"height\": 686, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-87c2jwnja0/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1452, \"height\": 239, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-87c2jwnja0/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1454, \"height\": 584, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-87c2jwnja0/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1456, \"height\": 586, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-87c2jwnja0/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1456, \"height\": 626, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-87c2jwnja0/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1456, \"height\": 198, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-87c2jwnja0/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1193, \"height\": 250, \"label\": \"Table\"}]"
motivation: U型网络多尺度logit蕴含互补信息，现有训练未有效利用混合尺度，导致分割细节丢失。
method: 提出LoMix模块，学习加权混合多尺度logit，并自动生成辅助监督以改善训练流程。
result: 在多个医学分割数据集上即插即用，LoMix显著提升Dice分数，超越单尺度监督基模型。
conclusion: LoMix证明了混合多尺度logit监督可有效增强分割模型，为医学图像分割训练提供新策略。
---

## Abstract
U-shaped networks output logits at multiple spatial scales, each capturing a different blend of coarse context and fine detail. Yet, training still treats these logits in isolation—either supervising only the final, highest-resolution logits or applying deep supervision with identical loss weights at every scale—without exploring mixed-scale combinations. Consequently, the decoder output misses the complementary cues that arise only when coarse and fine predictions are fused. To address this issue, we introduce LoMix (Logits Mixing), a Neural Architecture
Search (NAS)-inspired, differentiable plug-and-play module that generates new mixed-scale outputs and learns how exactly each of them should guide the training process. More precisely, LoMix mixes the multi-scale decoder logits with four lightweight fusion operators: addition, multiplication, concatenation, and attention-based weighted fusion, yielding a rich set of synthetic “mutant” maps. Every original or mutant map is given a softplus loss weight that is co-optimized with network parameters, mimicking a one-step architecture search that automatically discovers the most useful scales, mixtures, and operators. Plugging LoMix into recent U-shaped architectures (i.e., PVT-V2-B2 backbone with EMCAD decoder) on Synapse 8-organ dataset improves DICE by +4.2% over single-output supervision, +2.2% over deep supervision, and +1.5% over equally weighted additive fusion, all with zero inference overhead. When training data are scarce (e.g., one or two labeled scans, 5% of the trainset), the advantage grows to +9.23%, underscoring LoMix’s data efficiency. Across four benchmarks and diverse U-shaped networks, LoMiX improves DICE by up to +13.5% over single-output supervision, confirming that learnable weighted mixed-scale fusion generalizes broadly while remaining data efficient, fully interpretable, and overhead-free at inference. Our implementation is available at https://github.com/SLDGroup/LoMix.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

*   **核心问题**：当前主流的U型分割网络在解码器端会输出多个不同尺度的logit图，这些图分别蕴含了从粗到精的互补信息。然而，现有的训练策略要么只使用最后一层的输出（单输出监督），要么对中间层所有尺度的logit施加等权重的损失（深度监督）。这两种方式都忽略了将不同尺度logit进行混合所能产生的协同作用，导致分割模型无法充分利用多尺度信息，尤其是在处理大小差异巨大的器官时表现不佳。
*   **整体含义**：本文提出LoMix（Logits Mixing），其核心思想是**化被动为主动**，将训练过程中的多尺度logit视为一组可被动态组合与筛选的资产。通过一个受神经架构搜索启发、可学习的即插即用模块，自动探索并加权融合不同尺度的输出，以生成更具信息量的损失信号来指导网络训练，最终在不增加任何推理开销的情况下，显著提升医学图像分割的精度。

### 2. 论文提出的方法论

LoMix的核心思想是在训练时生成并融合多尺度logit的“变异体” (`mutant` maps)，并学习每个变异体对最终损失的贡献权重，以此作为额外的监督信号。

*   **问题形式化**：
    *   定义U型网络有 L 个解码器阶段，每个阶段输出的logit表示为 Z_l，上采样后得到 P_l。
    *   LoMix的目标是学习一组权重 w，用于线性组合原始logit图（P_orig）和融合logit图（P_mut）的损失。

*   **关键技术：组合变异模块 (CMM)**：
    *   CMM对任意两个或更多解码器阶段的输出logit子集 S 进行融合，生成 P_mut。
    *   采用**四种互补的融合算子**：
        1.  **像素级相加 (Addition)**：类似于“或”操作，聚合各尺度的置信度，增强模型认为正确的区域。
        2.  **像素级相乘 (Multiplication)**：类似于“与”操作，强调所有尺度都高度同意的区域，提升精度。
        3.  **通道拼接+1x1卷积 (Concatenation)**：通过学习一个线性权重矩阵，在像素级对不同logit进行最优线性组合。
        4.  **注意力加权融合 (Attention-Weighted Fusion, AWF)**：通过计算注意力分数，实现空间自适应的动态加权混合，让融合可以偏向在特定像素上更准确的那个尺度。
    *   这些操作引入了极少参数，且仅用于训练阶段。

*   **关键技术：受NAS启发的权重学习**：
    *   为每一个原始logit图 P_i 和每一个融合生成的变异logit图 P_s^{(op)} 分配一个可学习的标量参数 α。
    *   通过 Softplus 函数 (`w = ln(1 + e^α)`) 将 α 转换为严格为正的损失权重 w。这种设计独立、无约束，允许模型将无效输出的权重驱近于0，从而自动抑制噪声。
    *   这些权重参数与网络参数一起通过反向传播优化，无需额外的优化器或验证集搜索，实现“一步式”架构搜索。

*   **损失聚合**：
    *   总损失是所有原始和变异logit图损失的加权和：L_total = Σ (w_u * L_seg(P_u, Y))。
    *   这种加权是一种损失层面的动态集成，它保留了每个输出独立的监督信号，避免直接混合logit引发的梯度干扰。

### 3. 实验设计

*   **数据集与场景**：
    *   **多器官分割**：Synapse 8器官和13器官数据集。
    *   **心脏器官分割**：ACDC心脏MRI数据集。
    *   **病灶与肿瘤分割**：BUSI乳腺肿瘤超声、ISIC2018皮肤病灶、以及Kvasir/CVC-ClinicDB/CVC-ColonDB/ETIS-LaribPolypDB四个结肠息肉数据集。
    *   **少样本场景**：在仅使用Synapse 5%至40%训练数据（最少仅1个标注扫描）的低数据量条件下进行评测。
    *   **跨域泛化**：在Kvasir息肉数据上训练，在其他息肉数据集上测试。

*   **Benchmark**：
    *   主要网络架构为PVT-EMCAD-B2，并在多个SOTA分割网络上进行验证。
    *   对比的训练策略是：
        *   **单输出监督 (LL)**: 仅对最终层输出计算损失。
        *   **深度监督 (DS)**: 对所有中间层施加等权重的辅助损失。
        *   **MUTATION**: 一种先进的等权重相加混合监督方法。

*   **对比方法**：
    *   除训练策略外，在Synapse数据集上与UNet、Attention UNet、TransUNet、UNeXt、PVT-CASCADE等超过20种SOTA分割模型进行了性能对标。

### 4. 资源与算力

*   **计算资源**：所有实验均在**单张NVIDIA RTX A6000 GPU (48G 显存)** 上完成。
*   **软件框架**：PyTorch 1.11.0。
*   **训练细节**：优化器为AdamW，初始学习率1e-4。Synapse数据集训练300个epoch，ACDC数据集400个epoch，其余数据集200个epoch。论文未明确提及单次完整训练所需的总时长。

### 5. 实验数量与充分性

*   **实验数量巨大，覆盖面广，评估极为充分**。
    *   **主实验**：在**6种**不同的CNN和Transformer架构（UNet, AttnUNet, TransUNet, UNeXt, PVT-CASCADE, PVT-EMCAD）上，对比LoMix与LL、DS、MUTATION在8器官分割任务上的表现。
    *   **多任务/多数据集实验**：在另外**5个**医学分割任务（ACDC心脏、BUSI乳腺、ISIC皮肤、息肉等共7个数据集）上进行了验证。
    *   **少样本实验**：设置了4个不同训练数据比例（5%, 10%, 20%, 40%），证实其数据高效性。
    *   **消融研究**：包括融合算子组合（单算子到四算子）、固定权重 vs. 可学习权重、在不同主干网络上的增益对比、输入分辨率的影响、跨域泛化能力，以及**3D网络**上的可行性验证。
    *   **可解释性分析**：通过深入剖析损失权重的动态变化，揭示了不同融合算子随时间演化的重要性和角色。
    *   **公平性**：所有对比均使用相同的网络主干和实验设置，结果报告多次运行平均，性能提升显著且一致。

### 6. 论文的主要结论与发现

1.  **性能显著提升**：在PVT-EMCAD-B2上，LoMix在Synapse 8器官任务中将Dice系数提升至**85.07%**，远超单输出监督(+4.2%)和深度监督(+2.2%)，并优于其他SOTA模型。
2.  **极强的数据效率**：在数据极端稀缺（如仅用1个标注样本）时，LoMix将Dice大幅提升**+9.23%**，证明其在低数据量下有巨大优势。
3.  **通用性极强**：作为一个即插即用模块，LoMix在CNN、Transformer、轻量级和大型网络，以及2D和3D任务上均能带来一致的性能增益。
4.  **混合机制比单一机制更优**：消融实验证明，四种融合算子的组合使用和可学习权重是性能提升的关键。
5.  **可解释性强**：学习到的权重动态地表明，模型在训练初期更依赖粗尺度，随后自适应地转向更精细的空间加权融合。
6.  **零测试开销**：所有混合及权重学习操作仅在训练时进行，模型推理时的计算量、参数量和速度完全不变。

### 7. 优点

*   **创新性强**：首次将NAS思想与多尺度logit的动态损失混合相结合，提供了一种新颖的训练范式。
*   **方法优雅且易用**：模块即插即用，无需修改网络结构，仅通过改变损失计算方式就能嵌入到现有的任何分割框架中。
*   **无推理成本**：这是该方法的巨大实用优势，实现了“训练时多用计算换精度，推理时完全不变”的理想效果。
*   **评估扎实全面**：实验覆盖数据集、任务类型、baseline方法、消融维度均非常广泛，结论可信度高。
*   **良好的可解释性**：通过对softplus权重的可视化，揭示了模型内部的偏好和不同算子的作用，做到了“知其然，更知其所以然”。

### 8. 不足与局限

*   **训练侧计算与显存增加**：尽管测试端无开销，但在训练期间，生成并计算所有logit“变异体”损失会显著增加计算量和显存占用，可能对资源有限的用户构成挑战。
*   **扩展至3D的成本**：虽然原理上可扩展，但在处理3D医学图像时，多尺度logit和其变异体的显存消耗可能会剧烈膨胀，实际的适用性有待进一步验证。
*   **依赖多尺度结构**：LoMix的前提是网络本身具备清晰的多尺度输出结构（如U-Net），对于非U型的其他分割架构可能无法直接应用。
*   **缺乏理论分析**：论文主要从实验角度证明了有效性，但未提供一个理论框架来解释为何这种特定的混合与加权方式能如此稳定且高效地工作。

（完）
