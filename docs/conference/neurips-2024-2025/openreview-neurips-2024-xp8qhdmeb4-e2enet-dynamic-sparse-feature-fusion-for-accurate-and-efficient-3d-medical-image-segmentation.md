---
title: "E2ENet: Dynamic Sparse Feature Fusion for Accurate and Efficient 3D Medical Image Segmentation"
title_zh: E2ENet：动态稀疏特征融合实现精确高效的3D医学图像分割
authors: "Boqian Wu, Qiao Xiao, Shiwei Liu, Lu Yin, Mykola Pechenizkiy, Decebal Constantin Mocanu, Maurice van Keulen, Elena Mocanu"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=Xp8qhdmeb4"
tags: ["query:abdk-seg"]
score: 8.0
evidence: 提出E2ENet，一种具有动态稀疏特征融合的3D医学图像分割模型，兼具精度与效率。
tldr: 针对3D医学分割模型计算负担重的问题，本文提出E2ENet，通过动态稀疏特征融合自适应聚合多尺度信息并降低冗余，同时约束深度偏移卷积提升效率。实验表明E2ENet在多个3D医学分割任务上以极少参数和计算量取得顶尖性能。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-xp8qhdmeb4/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1453, \"height\": 294, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xp8qhdmeb4/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1284, \"height\": 634, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xp8qhdmeb4/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 589, \"height\": 637, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xp8qhdmeb4/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 644, \"height\": 589, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xp8qhdmeb4/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 593, \"height\": 557, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xp8qhdmeb4/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1318, \"height\": 351, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xp8qhdmeb4/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 655, \"height\": 123, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xp8qhdmeb4/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 736, \"height\": 875, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xp8qhdmeb4/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1453, \"height\": 732, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xp8qhdmeb4/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 669, \"height\": 691, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xp8qhdmeb4/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 856, \"height\": 421, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xp8qhdmeb4/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1086, \"height\": 513, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xp8qhdmeb4/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1440, \"height\": 457, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xp8qhdmeb4/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1452, \"height\": 435, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-xp8qhdmeb4/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1163, \"height\": 375, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-xp8qhdmeb4/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 727, \"height\": 450, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xp8qhdmeb4/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 868, \"height\": 276, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xp8qhdmeb4/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 873, \"height\": 422, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xp8qhdmeb4/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 871, \"height\": 437, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xp8qhdmeb4/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 726, \"height\": 212, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xp8qhdmeb4/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 872, \"height\": 271, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xp8qhdmeb4/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 869, \"height\": 528, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xp8qhdmeb4/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 726, \"height\": 235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xp8qhdmeb4/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 726, \"height\": 140, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xp8qhdmeb4/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1446, \"height\": 335, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-xp8qhdmeb4/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1443, \"height\": 232, \"label\": \"Table\"}]"
motivation: 现有3D医学分割模型参数量和计算量巨大，难以在资源受限硬件上部署。
method: 提出动态稀疏特征融合机制和限制深度偏移的3D卷积，构建高效E2ENet。
result: 在多个3D医学影像分割数据集上，以更低FLOPs和参数量达到了先进精度。
conclusion: E2ENet为高效3D医学分割提供了新方案，有利于临床实时应用。
---

## Abstract
Deep neural networks have evolved as the leading approach in 3D medical image segmentation due to their outstanding performance. However, the ever-increasing model size and computational cost of deep neural networks have become the primary barriers to deploying them on real-world, resource-limited hardware. To achieve both segmentation accuracy and efficiency, we propose a 3D medical image segmentation model called Efficient to Efficient Network (E2ENet), which incorporates two parametrically and computationally efficient designs. i. Dynamic sparse feature fusion (DSFF) mechanism: it adaptively learns to fuse informative multi-scale features while reducing redundancy. ii. Restricted depth-shift in 3D convolution: it leverages the 3D spatial information while keeping the model and computational complexity as 2D-based methods. We conduct extensive experiments on AMOS, Brain Tumor Segmentation and BTCV Challenge, demonstrating that E2ENet consistently achieves a superior trade-off between accuracy and efficiency than prior arts across various resource constraints. %In particular, with a single model and single scale, E2ENet achieves comparable accuracy on the large-scale challenge AMOS-CT, while saving over 69% parameter count and 27% FLOPs in the inference phase, compared with the previous
best-performing method. Our code has been made available at: https://github.com/boqian333/E2ENet-Medical.

---

## 论文详细总结（自动生成）

### 1. 论文核心问题与研究动机
- **问题背景**：3D医学图像分割（CT/MRI）对于临床诊断至关重要，但现有深度神经网络（如nnUNet、Transformers）参数量和计算量（FLOPs）呈立方级增长，导致在资源受限的真实医疗硬件上难以部署。
- **核心矛盾**：分割精度与模型效率之间的权衡。冗余的多尺度特征融合和全3D卷积是计算开销的主要来源。
- **研究目标**：设计一种兼具高精度和高效率的3D分割模型，在不牺牲性能的前提下大幅压缩模型大小与计算量。

### 2. 方法论：E2ENet
E2ENet（Efficient to Efficient Network）包含两大效率化设计：

#### 2.1 动态稀疏特征融合（DSFF）
- **特征融合架构**：骨干网络提取多尺度特征图后，通过多个阶段逐步聚合来自“向下”（高分辨率细节）、“向上”（全局上下文）和“向前”（同级信息）三个方向的特征。每个融合节点采用 $1\times 1\times 1$ 卷积 + Instance Norm + LeakyReLU。
- **稀疏连接学习**：每个融合操作维护一个二值掩码 $M_{j,i}\in\{0,1\}^{C_{\text{in}}\times C_{\text{out}}}$，控制输入–输出通道间的连接存在与否。训练开始时随机初始化，使连接数量满足特征稀疏度 $S$（例如 $S=0.8$ 表示80%连接被置零）。
- **动态演化机制**：每隔 $\Delta T$ 个epoch，按连接权重 L1 范数评估重要性，剪去最不重要的一定比例连接，同时随机重新激活等量的休眠连接（重新初始化），保持稀疏度恒定。该“稀疏到稀疏”的训练方式实现了自适应多尺度特征选择，大幅降低计算和存储消耗。
- **公式核心**：融合输出为
  $$
  x_{j,i}^{c_{\text{out}}} = \sigma\!\left(\mathrm{IN}\!\left(\sum_{c=0}^{C_{\text{in}}}( \tilde{x}_{j,i}^{c} * (M_{j,i}^{c,c_{\text{out}}}\cdot \theta_{j,i}^{c,c_{\text{out}}}) )\right)\right)
  $$
  其中 $\tilde{x}_{j,i}^{c}$ 为拼接后的第 $c$ 通道特征图，$\theta$ 为卷积核。

#### 2.2 受限深度偏移3D卷积
- **思路来源**：受视频理解中的 temporal shift 和 3D-shift 启发，将特征图沿通道维度均分为三部分，分别沿深度维度偏移 $-1, 0, +1$ 单位，然后使用 $1\times 3\times 3$ 卷积。
- **效率优势**：保持了与2D卷积几乎相同的参数量和计算量（因 $1\times 3\times 3$ 核），但通过偏移操作交换了相邻切片的上下文，实现了类3D的信息聚合。实验表明，偏移量选择 $\{-1,0,1\}$ 能最佳平衡空间精细度与深度信息。

### 3. 实验设计
- **数据集与场景**：
  - **AMOS-CT**：500例腹部CT，15类器官，多中心、多设备采集（训练/验证/测试=200/100/200）。
  - **BraTS (MSD)**：484例多模态MRI脑肿瘤分割（水肿、增强肿瘤、非增强肿瘤），5折交叉验证。
  - **BTCV**：30例训练+20例测试，13类腹部器官。
- **对比方法**：
  - CNN类：nnUNet、VNet、3D UNet++、DiNTS（NAS方法）等。
  - Transformer类：CoTr、nnFormer、UNETR、Swin UNETR。
  - 多尺度方法：DeepLabv3、MedFormer。
- **评价指标**：平均Dice（mDice）、参数总量（Params）、推理FLOPs、PT分数（综合精度与资源），以及边界指标mNSD。

### 4. 资源与算力
- **实现框架**：PyTorch，基于nnUNet代码库进行数据预处理。
- **硬件**：所有实验在**NVIDIA A100 GPU** 上完成，但文中未给出具体GPU数量及单次训练时长。
- **训练设置**：SGD优化器，初始学习率0.01采用poly衰减，动量0.99，权重衰减$3\times 10^{-5}$，最大1000 epoch，每epoch 250次迭代。训练采用5折交叉验证，推理采用滑窗策略。推理速度对比额外使用了Intel Xeon Platinum 8360Y CPU（18核）并结合DeepSparse库。
- **缺失信息**：全文未报告训练单个模型的总耗时或GPU小时数。

### 5. 实验数量与充分性
- **主要实验组**：
  - 在三个国际医学分割挑战赛数据集上进行SOTA对比（多个稀疏度版本：$S=0.7, 0.8, 0.9$）。
  - 详尽消融实验：DSFF有/无、shift有/无、shift幅度（$\pm1,\pm2,\pm3,\pm7$）、卷积核尺寸（$1\times 3\times 3$ vs $3\times 3\times 3$）、DSFF更新频率 $\Delta T$ 等。
  - 泛化性测试：AMOS-CT预训练后微调到AMOS-MRI；在CT测试集上跨越扫描仪域漂移验证。
  - 模型容量公平对比：缩放nnUNet（减少通道/层数）与放大E2ENet，在相似FLOPs下比较。
  - 特征融合比例动态可视化、收敛曲线分析、PT分数权重敏感性分析。
  - 统计显著性检验：基于mDice的Nemenyi事后检验临界距离图。
- **评估充分性**：实验覆盖三个主流数据集、两类模态，对比超过10种SOTA方法，消融变量全面，且进行了公平性的容量控制，整体实验设计客观、公平、扎实。

### 6. 主要结论与发现
- E2ENet在**精度–效率权衡**上显著优于现有方法。例如在AMOS-CT验证集上，$S=0.8$ 的E2ENet以**9.44M参数、778.74G FLOPs**达到mDice **90.3%**，相比nnUNet参数减少69%、FLOPs降低27%，而mDice仅低0.2%；即使稀疏度提升至90%，mDice仍达89.6%，参数仅7.64M。
- DSFF机制在不损失精度的前提下能滤除大量冗余特征连接，动态更新策略优于静态剪枝。
- 受限深度偏移 $1\times 3\times 3$ 卷积在精度上等价甚至优于全 $3\times 3\times 3$ 卷积，但计算量大幅降低；偏移量过大反而损害边界精度。
- E2ENet的架构拓扑可直接迁移至新模态（CT→MRI），且表现出良好泛化性。

### 7. 优点
- **创新性强**：将动态稀疏训练引入多尺度特征融合，同期工作极少见；受限深度偏移以极小代价实现3D感受野。
- **高效设计**：从特征选择和卷积操作两个层面协同降本，可在CPU上通过稀疏推理库获得实际加速。
- **实验严谨**：多数据集、多指标、充分消融和统计检验；公平缩放对比避免容量偏差。
- **可解释性**：通过可视化融合比例揭示了“前向流为主导、向上/向下流互补”的学习模式。
- **开源**：代码已公开，有益于复现和社区应用。

### 8. 不足与局限
- **实际训练加速有限**：由于当前GPU对非结构稀疏支持不足，训练时仍需使用稠密掩码模拟，未实现真实的训练提速和内存节省。
- **推理加速依赖特定硬件**：CPU上的加速（1.26×–1.38×）远未达到理论稀疏比所对应的倍率，尤其在3D分割这种卷积密集型任务上，硬件生态限制明显。
- **模型规模探索有限**：仅在固定骨干（通道数48‑320）下验证，未对不同深度/宽度的E2ENet做更广泛探索；也未在更大规模数据集或更具挑战的细粒度任务（如血管分割）上测试。
- **偏移策略固化**：深度偏移量固定为 $\{-1,0,1\}$，未尝试可学习偏移，灵活度有提升空间。
- **对比缺失**：未与基于状态空间模型（如Mamba）的最新轻量分割方法比较，尽管文中提及了该方向。

（完）
