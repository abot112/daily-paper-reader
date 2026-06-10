---
title: "Upping the Game: How 2D U-Net Skip Connections Flip 3D Segmentation"
title_zh: 升级游戏：2D U-Net跳跃连接如何改变3D分割
authors: "Xingru Huang, Yihao Guo, Jian Huang, Tianyun Zhang, HE HONG, Shaowei Jiang, Yaoqi Sun"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=QI1ScdeQjp"
tags: ["query:abdk-seg"]
score: 8.0
evidence: 使用2D U-Net跳跃连接的3D医学图像分割；直接适用于腹部CT多器官分割
tldr: 提出一种集成2D U-Net跳跃连接的3D分割网络，有效利用轴向切片平面特征，提升3D医学图像分割性能。该方法直接适用于全监督腹部CT多器官分割任务，为解决各向异性问题提供了新架构。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-qi1scdeqjp/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1446, \"height\": 386, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qi1scdeqjp/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1415, \"height\": 576, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qi1scdeqjp/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1437, \"height\": 338, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qi1scdeqjp/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1435, \"height\": 533, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qi1scdeqjp/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 705, \"height\": 459, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qi1scdeqjp/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 632, \"height\": 435, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qi1scdeqjp/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1431, \"height\": 422, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qi1scdeqjp/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1433, \"height\": 419, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qi1scdeqjp/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1295, \"height\": 1054, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qi1scdeqjp/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1438, \"height\": 675, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-qi1scdeqjp/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1442, \"height\": 649, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 710, \"height\": 203, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1444, \"height\": 265, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 705, \"height\": 212, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 620, \"height\": 121, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 933, \"height\": 284, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 936, \"height\": 282, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 931, \"height\": 282, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1443, \"height\": 227, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 928, \"height\": 248, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 933, \"height\": 151, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1073, \"height\": 489, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1436, \"height\": 832, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1004, \"height\": 538, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1149, \"height\": 219, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1436, \"height\": 466, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1439, \"height\": 331, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1443, \"height\": 300, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1443, \"height\": 437, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1445, \"height\": 541, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1441, \"height\": 519, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1441, \"height\": 529, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1443, \"height\": 414, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1442, \"height\": 427, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1444, \"height\": 440, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-qi1scdeqjp/table-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1441, \"height\": 308, \"label\": \"Table\"}]"
motivation: 3D医学图像中三轴信息密度不均，切片特征利用不足。
method: 将2D U-Net跳跃连接融入3D CNN，增强切片特征融合。
result: 在CT和MRI上提升了分割效率。
conclusion: 为3D分割提供了高效的特征利用方案，适用于腹部器官分割。
---

## Abstract
In the present study, we introduce an innovative structure for 3D medical image segmentation that effectively integrates 2D U-Net-derived skip connections into the architecture of 3D convolutional neural networks (3D CNNs). Conventional 3D segmentation techniques predominantly depend on isotropic 3D convolutions for the extraction of volumetric features, which frequently engenders inefficiencies due to the varying information density across the three orthogonal axes in medical imaging modalities such as computed tomography (CT) and magnetic resonance imaging (MRI). This disparity leads to a decline in axial-slice plane feature extraction efficiency, with slice plane features being comparatively underutilized relative to features in the time-axial. To address this issue, we introduce the U-shaped Connection (uC), utilizing simplified 2D U-Net in place of standard skip connections to augment the extraction of the axial-slice plane features while concurrently preserving the volumetric context afforded by 3D convolutions. Based on uC, we further present uC 3DU-Net, an enhanced 3D U-Net backbone that integrates the uC approach to facilitate optimal axial-slice plane feature utilization. Through rigorous experimental validation on five publicly accessible datasets—FLARE2021, OIMHS, FeTA2021, AbdomenCT-1K, and BTCV, the proposed method surpasses contemporary state-of-the-art models. Notably, this performance is achieved while reducing the number of parameters and computational complexity. This investigation underscores the efficacy of incorporating 2D convolutions within the framework of 3D CNNs to overcome the intrinsic limitations of volumetric segmentation, thereby potentially expanding the frontiers of medical image analysis. Our implementation is available at https://github.com/IMOP-lab/U-Shaped-Connection.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义（研究动机和背景）

- **核心问题**：三维医学图像（如CT、MRI）在轴向（切片平面）和时间轴（层间）方向的信息密度不均一，切片平面特征信息更丰富。现有三维卷积神经网络（3D CNN）使用各向同性的三维卷积，同等对待所有轴，导致切片平面特征提取效率低下，参数和计算量高而效果提升有限。
- **整体含义**：文章提出一种新的架构，通过将2D U-Net形式的跳跃连接（称为U-shaped Connection, uC）集成到3D CNN的主干中，高效提取轴向切片平面的局部细节特征，同时保留三维空间上下文，从而以更少的参数和计算量实现更高的分割性能。

### 2. 论文提出的方法论：核心思想、关键技术细节

- **核心思想**：利用2D卷积对切片平面特征提取的高效性，将标准跳跃连接替换为一个轻量化的2D U-Net（uC），并将其输出与3D编码器-解码器特征融合，弥补3D CNN对切片平面信息利用不足的缺陷。
- **技术细节**：
  - **U-shaped Connection (uC)**：一个简化的2D U-Net，去掉首尾卷积层，仅保留下采样和上采样层，每个块含平均池化和两层卷积（2D卷积 + 群归一化 + ReLU）。输入来自3D编码器各阶段的特征（先通过reshape将5D张量转成4D以适配2D卷积），输出同样reshape回5D。
  - **uC 3DU-Net**：以3D U-Net为骨干，在编码器前三个阶段用uC替换原跳跃连接。解码器上采样后，使用双特征集成模块（DFi）融合3D空间特征和uC提供的切片平面特征。
  - **DFi模块**：将uC提取的2D切片特征（F1）和上采样得到的3D特征（F2）通过拼接（cat）和注意力机制（加法后Sigmoid生成注意力图）进行融合，并通过1×1卷积控制通道数，比简单拼接更轻量高效。
- **流程**：输入 → 3D编码器（5阶段） → 对应阶段特征经reshape输入uC → uC输出reshape后与解码器上采样特征通过DFi逐阶段融合 → 最终卷积输出分割图。

### 3. 实验设计：数据集、Benchmark 和对比方法

- **数据集**：
  1. FLARE2021（腹部CT，4类器官，361例，各向异性）
  2. OIMHS（视网膜OCT，4类，125个序列，各向异性）
  3. FeTA2021（胎儿脑MRI，7类，80例，各向同性）
  4. AbdomenCT-1K（腹部CT，4类，361例，各向异性）
  5. BTCV（腹部CT，13类，30例，各向异性）
- **基准对比方法**：包括3D U-Net、SegResNet、RAP-Net、nnU-Net、TransBTS、UNETR、nnFormer、SwinUNETR、3D UX-Net等经典和最新模型。
- **评估指标**：IoU/mIoU、Dice、ASSD、HD/HD95、VOE、AdjRand等。

### 4. 资源与算力

- **硬件**：每台工作站配备两块NVIDIA GeForce RTX 4090 GPU，128 GB内存。
- **训练设置**：所有实验均采用相同数据预处理和超参，80,000次迭代，批量大小为2，使用AdamW优化器，学习率0.0001，五折交叉验证。使用分布式数据并行（DDP）训练。
- **未明确说明总训练时长**，但给出了完整的硬件和软件环境（Python 3.9, PyTorch 2.0.0, MONAI 0.9.0）。

### 5. 实验数量与充分性、客观性

- **实验数量**：大量实验，包括：
  - 在5个公开数据集上与9种以上SOTA方法对比（主结果表）。
  - 不同骨干模型（SegResNet, TransBTS, SwinUNETR, 3D UX-Net）集成uC的泛化性实验。
  - 不同通道深度配置下的性能与参数对比。
  - 2D uC与3D uC的性能和参数量对比（消融）。
  - uC应用于不同编码阶段的消融。
  - DFi模块效果验证。
  - 切片维度的对比实验。
  - 图像重建质量（PSNR）辅助评估。
- **客观性**：使用公开数据集，固定预处理和训练配置，五折交叉验证，Wilcoxon检验保证统计显著性，与多个SOTA在统一设定下比较参数和FLOPs，实验设计较为严谨公正。

### 6. 主要结论与发现

- uC 3DU-Net在多个数据集（尤其各向异性数据）上以更少的参数量和更低的FLOPs达到或超越SOTA性能。
- 2D卷积在切片平面特征提取上效率远高于3D卷积，uC能有效弥补3D CNN在此方面的不足。
- 引入uC后，即使降低骨干的通道数，仍能维持甚至提升性能，进一步降低计算开销。
- DFi模块以轻量方式实现了2D和3D特征的有效融合。

### 7. 优点：方法或实验设计亮点

- **方法新颖性**：首次系统性地将2D U-Net形式的跳跃连接植入3D分割网络，针对各向异性医学图像的特性进行专项增强。
- **高效性**：通过简单的reshape和2D卷积，大幅提升切片平面特征利用效率，参数/性能比优异。
- **模块化设计**：uC和DFi均为即插即用组件，可便捷地集成到不同3D骨干中，实验已证明其泛化性。
- **实验全面**：覆盖多个领域（腹部、脑、视网膜）、多种模态（CT、MRI、OCT）和各向异性/同性数据，验证充分。

### 8. 不足与局限

- **各向同性数据集提升有限**：在FeTA2021（各向同性）上的性能提升幅度相对较小，表明方法主要针对切片平面与轴间分辨率差异大的情形。
- **未讨论计算/推理延迟**：尽管参数和FLOPs较低，但uC引入reshape和数据维度变换，实际推理速度未做分析。
- **仅限于全监督分割**：未探索在弱监督或自监督场景下的效果。
- **未与其他2D/3D混合方法深入对比**：例如2.5D网络或多视图融合方法，仅与纯3D架构比较。
- **单模态输入**：没有展示多模态融合场景下的表现。
- **未提供训练总时长**，无法直接评估训练效率。

（完）
