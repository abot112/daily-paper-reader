---
title: "FuseUNet: A Multi-Scale Feature Fusion Method for U-like Networks"
title_zh: FuseUNet：一种用于U型网络的多尺度特征融合方法
authors: "Quansong He, Xiangde Min, Kaishen Wang, Tao He"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=KYiynifZUk"
tags: ["query:abdk-seg"]
score: 6.0
evidence: 提出了一种用于U-Net的多尺度特征融合方法，U-Net是医学图像分割中广泛使用的架构。
tldr: 针对U-Net跳跃连接缺乏多尺度特征交互和简单融合操作的局限，提出FuseUNet，将解码过程建模为初值问题，通过离散化跳跃连接实现多尺度特征融合，实验表明其在医学图像分割上性能提升，为U型网络提供新思路。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-kyiynifzuk/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 529, \"height\": 375, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kyiynifzuk/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1683, \"height\": 1033, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kyiynifzuk/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1766, \"height\": 575, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kyiynifzuk/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 835, \"height\": 522, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kyiynifzuk/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 782, \"height\": 516, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kyiynifzuk/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1775, \"height\": 475, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kyiynifzuk/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1774, \"height\": 474, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kyiynifzuk/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1777, \"height\": 471, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-kyiynifzuk/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1739, \"height\": 1242, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-kyiynifzuk/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 841, \"height\": 454, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kyiynifzuk/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1751, \"height\": 347, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kyiynifzuk/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1627, \"height\": 816, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kyiynifzuk/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1709, \"height\": 397, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kyiynifzuk/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 787, \"height\": 250, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kyiynifzuk/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1142, \"height\": 609, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kyiynifzuk/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 968, \"height\": 190, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kyiynifzuk/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1722, \"height\": 186, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kyiynifzuk/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1120, \"height\": 154, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kyiynifzuk/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 882, \"height\": 783, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kyiynifzuk/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 934, \"height\": 284, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-kyiynifzuk/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1761, \"height\": 182, \"label\": \"Table\"}]"
motivation: U-Net跳跃连接缺乏多尺度特征交互，仅依赖简单拼接或相加，限制了信息整合。
method: 将U-Net解码过程重新构想为求解初值问题，把跳跃连接视为离散化，提出多尺度特征融合方法。
result: 在医学图像分割任务上，FuseUNet相比基线方法取得了有竞争力的结果。
conclusion: FuseUNet有效克服了U-Net跳跃连接的局限性，提升了多尺度特征融合能力。
---

## Abstract
Medical image segmentation is a critical task in computer vision, with UNet serving as a milestone architecture. The typical component of UNet family is the skip connection, however, their skip connections face two significant limitations: (1) they lack effective interaction between features at different scales, and (2) they rely on simple concatenation or addition operations, which constrain efficient information integration. While recent improvements to UNet have focused on enhancing encoder and decoder capabilities, these limitations remain overlooked. To overcome these challenges, we propose a novel multi-scale feature fusion method that reimagines the UNet decoding process as solving an initial value problem (IVP), treating skip connections as discrete nodes. By leveraging principles from the linear multistep method, we propose an adaptive ordinary differential equation method to enable effective multi-scale feature fusion. Our approach is independent of the encoder and decoder architectures, making it adaptable to various U-Net-like networks. Experiments on ACDC, KiTS2023, MSD brain tumor, and ISIC2017/2018 skin lesion segmentation datasets demonstrate improved feature utilization, reduced network parameters, and maintained high performance. The code is available at
https://github.com/nayutayuki/FuseUNet.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **研究动机**：医学图像分割中，UNet 及其变体（统称 U-Nets）虽已成为里程碑式架构，但其跳跃连接存在两大局限：① 无法实现不同尺度特征间的有效交互；② 仅依赖简单的特征拼接或相加，限制了信息的高效整合。近年来的改进多集中于增强编码器或解码器模块，而跳跃连接本身的多尺度融合问题被长期忽视。
- **整体含义**：论文将 UNet 的解码过程重新构想为一个**初值问题（IVP）**，把多个尺度的跳跃连接视为离散节点，并引入**线性多步法**（linear multistep method）的思想，设计出一种自适应的高阶离散方法。这一方法独立于具体的编码器、解码器架构，理论上可泛化至各类 U 型网络，从数值计算的角度为跨层信息传播提供可解释的数学基础。

### 2. 论文提出的方法论
- **核心思想**：将解码器逐阶段恢复特征的过程类比为常微分方程（ODE）的数值求解。传统的逐阶段上采样+同尺度跳跃连接类似于一阶显式欧拉法，精度有限。论文使用**线性多步法**（如 Adams-Bashforth 显式方法和 Adams-Moulton 隐式方法），利用过去多个阶段的跳跃连接特征和已求得的解码器状态来预测当前状态，从而实现跨尺度特征融合。
- **关键技术细节**：
    - **自适应离散方法**：根据当前所处的解码阶段数，动态选择多步法的阶数。在低阶段（i<4）时使用较低阶的隐式方法启动；当阶段数≥4时，采用 4 阶隐式方法；最后阶段则使用 4 阶显式方法计算最终输出。整个流程通过**预测-校正**（Predictor-Corrector）机制实现：先用显式方法给出预测值，再用隐式方法进行校正，以在未知当前导数值的前提下获得更高精度。
    - **神经记忆常微分方程（nmODEs）**：将 nmODEs 引入离散求解过程。其方程形式为 \(\dot{Y}_i = -Y_i + f(Y_i + g(X_i))\)，其中 \(X_i\) 为当前尺度的跳跃连接特征，\(Y_i\) 为记忆流（解码器状态），\(f(\cdot)\) 为非线性映射（根据骨干网络架构不同可选用卷积、Transformer 或 Mamba 操作），\(g(\cdot)\) 通过卷积和插值对齐通道数与空间尺寸。记忆流初始化为 0，并在各阶段逐步填充多尺度信息。
    - **整体框架**：在原有 U-Net 编码器输出多个尺度的特征 \(X_1, X_2, \dots, X_L\) 后，通过上述自适应离散 nmODEs 模块依次更新记忆流 \(Y_1, Y_2, \dots, Y_L\)，最后经由 1×1 卷积映射为分割图。模块分为预测-校正器（P-C）、计算器（C）和 nmODEs 块。

### 3. 实验设计
- **数据集**：选用两类任务共 5 个数据集。
    - **3D 分割任务**：心脏 MRI 数据集 ACDC（3 类，100 例）、肾脏 CT 数据集 KiTS2023（3 类，559 例）、脑肿瘤 MRI 数据集 MSD Brain Tumor（3 类，484 例）。
    - **2D 分割任务**：皮肤镜图像数据集 ISIC2017（1 类，2000 例）和 ISIC2018（1 类，2594 例）。
- **骨干网络与对比方法**：为验证泛化性，针对三种主流架构各选一个代表性骨干网络，并在其原论文使用的数据集上开展实验。
    - 卷积架构：nn-UNet；对比方法包括 CoTr、Swin-UNETR、U-Mamba、STU-Net-L 等。
    - Transformer 架构：UNETR；对比方法有 TransUNet、Swin-UNETR 等。
    - Mamba 架构：UltraLight VM-UNet；对比方法含 UNet、TransFuse、MALUNet、EGE-UNet、VM-UNet 等。
- **评价指标**：3D 任务报告 Dice 系数（五折交叉验证），2D 任务报告 Dice、敏感度、特异度、准确率。同时统计参数量和 GFLOPs。

### 4. 资源与算力
- 所有实验均在**单块 NVIDIA RTX 4090** GPU 上完成。
- 文中未给出总训练时长，但提供了部分模型的显存占用和每 epoch 耗时（例如 nn-UNet 骨干网络每 epoch 约 144 秒，FuseUNet 约 128 秒；UltraLight VM-UNet 骨干每 epoch 约 21 秒，FuseUNet 约 22 秒）。
- 除学习率（设为骨干网络的 2~3 倍）外，其余超参数均与对应的骨干网络保持一致。

### 5. 实验数量与充分性
- **性能对比实验**：在 3 个 3D 数据集和 2 个 2D 数据集上，分别将所提方法嵌入三种骨干网络，与多种 SOTA 方法进行了全面对比，涵盖了卷积、Transformer、Mamba 三种主流范式，实验横向覆盖较广。
- **消融实验**：
    - 探究特征融合步数（最大阶数）对性能的影响（在 5 个数据集首折上进行），表明阶数越高（多尺度交互越充分）性能呈正相关。
    - 研究记忆流通道数（记忆容量）对性能的敏感度（在 KiTS 首折上进行），确定了 2 倍目标类别数的通道设置可在性能与开销间取得较好平衡。
- **可视化分析**：提供了多个数据集的定性分割结果对比，展示了 FuseUNet 在边界识别、假阳性/假阴性改善方面的效果。
- **统计分析**：附录中对 ACDC 和 KiTS 数据集进行了差异显著性检验，显示 FuseUNet 与 nn-UNet 的性能无统计学显著差异（p>0.05），表明方法可在大幅瘦身的同时保持竞争力。
- 实验设计较为系统，对比公平（沿用骨干网络原始设置，仅调整学习率），消融实验针对关键组件，具备较好的充分性和客观性。

### 6. 论文的主要结论与发现
- FuseUNet 提出的多尺度特征融合方法能有效克服经典 U-Net 跳跃连接缺乏跨尺度交互、融合策略简单的缺陷。
- 该方法具有良好的架构无关性，可灵活嵌入基于卷积、Transformer 和 Mamba 的 U 型网络。
- 在多个 3D 和 2D 医学图像分割任务中，FuseUNet 在**大幅减少参数量**（如 nn-UNet 减少 54.9%）和**计算量**（GFLOPs 降低 34.3%~50%）的同时，**保持了与骨干网络相当甚至略优的分割性能**。
- 数值计算理论（线性多步法）可为网络结构设计提供可解释的数学基础，揭示了跳跃连接与数值积分的深层联系。

### 7. 优点
- **视角新颖**：首次从数值求解 ODE 的角度重新诠释并重构跳跃连接，为分割网络设计提供了数学理论支撑。
- **通用性强**：方法解耦于编码器/解码器具体实现，可直接适配多种主流 U 型网络，实用性高。
- **资源效率显著**：在保持分割精度的前提下，显著降低了模型参数量和 FLOPs，尤其适用于参数冗余较大的卷积类 U-Net。
- **实验扎实**：覆盖多种架构和数据集，并包含消融实验、可视化及统计检验，结论可信度较高。

### 8. 不足与局限
- **内存消耗较高**：线性多步法需要存储多个历史时刻的解（记忆流），当目标类别数很多或网络深度较大时，显存占用会明显增加。例如在 KiTS 消融实验中，4 倍于目标类别数的通道已使显存升至 8.7GB。
- **极轻量网络中 FLOPs 可能增加**：在 UltraLight VM-UNet 这类参数极少的骨干网络上，由于需要插值对齐空间尺寸，FuseUNet 的 GFLOPs 出现了微小上升（增加 0.075），其瘦身优势在极端轻量级模型上可能有限。
- **计算流程相对复杂**：引入预测-校正和自适应阶数选择，增加了实现与调试的复杂度。
- **泛化性验证范围**：虽然覆盖了三种架构，但所有实验均限于医学图像分割，在自然图像或其他视觉任务中的有效性尚未验证。
- **缺乏更细粒度的效率对比**：未详细报告推理延迟或吞吐量，而参数量/FLOPs 的减少能否完全转化为实际加速仍有待商榷。

（完）
