---
title: Neighborhood Self-Dissimilarity Attention for Medical Image Segmentation
title_zh: 用于医学图像分割的邻域自差异性注意力
authors: "Chen Junren, Rui Chen, Wang-wei, Junlong Cheng, Gang Liang, zhanglei-scu, Liangyin Chen"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=tBhEHymG1m"
tags: ["query:abdk-seg"]
score: 8.0
evidence: 提出无参数注意力机制用于医学图像分割，不增加复杂度而提升精度。
tldr: 为解决医学分割注意力模块精度与复杂度的矛盾，本文提出无参数的邻域自差异性注意力，通过计算邻域特征差异聚焦关键区域。实验表明该方法以更低计算量达到领先精度，有利于资源受限场景的部署。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-tbhehymg1m/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1444, \"height\": 271, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tbhehymg1m/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1425, \"height\": 878, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-tbhehymg1m/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1436, \"height\": 216, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-tbhehymg1m/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1448, \"height\": 889, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-tbhehymg1m/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1447, \"height\": 247, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-tbhehymg1m/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1445, \"height\": 196, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-tbhehymg1m/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1445, \"height\": 453, \"label\": \"Table\"}]"
motivation: 现有注意力机制难以兼顾精度与计算复杂度，限制其在医疗设备上的应用。
method: 提出邻域自差异性注意力，通过邻域特征差异生成注意力权重，无需额外参数。
result: 在多个医学分割数据集上，以更低参数量和计算量达到了领先性能。
conclusion: 该模块为轻量级医学分割网络设计提供了新方向，促进医疗AI公平可及。
---

## Abstract
Medical image segmentation based on neural networks is pivotal in promoting digital health equity. The attention mechanism increasingly serves as a key component in modern neural networks, as it enables the network to focus on regions of interest, thus improving the segmentation accuracy in medical images.  However, current attention mechanisms confront an accuracy-complexity trade-off paradox: accuracy gains demand higher computational costs, while reducing complexity sacrifices model accuracy. Such a contradiction inherently restricts the real-world deployment of attention mechanisms in resource-limited settings, thus exacerbating healthcare disparities. To overcome this dilemma, we propose a parameter-free Neighborhood Self-Dissimilarity Attention (NSDA), inspired by radiologists' diagnostic patterns of prioritizing regions exhibiting substantial differences during clinical image interpretation.  Unlike pairwise-similarity-based self-attention mechanisms, NSDA constructs a size-adaptive local dissimilarity measure that quantifies element-neighborhood differences. By assigning higher attention weights to regions with larger feature differences, NSDA directs the neural network to focus on high-discrepancy regions, thus improving segmentation accuracy without adding trainable parameters directly related to computational complexity.  The experimental results demonstrate the effectiveness and generalization of our method. This study presents a parameter-free attention paradigm, designed with clinical prior knowledge, to improve neural network performance for medical image analysis and contribute to digital health equity in low-resource settings. The code is available at [https://github.com/ChenJunren-Lab/Neighborhood-Self-Dissimilarity-Attention](https://github.com/ChenJunren-Lab/Neighborhood-Self-Dissimilarity-Attention).

---

## 论文详细总结（自动生成）

# 论文总结：Neighborhood Self-Dissimilarity Attention for Medical Image Segmentation

## 1. 研究动机与核心问题
- **核心矛盾**：当前用于医学图像分割的注意力机制面临**精度-复杂度权衡困境**——追求更高分割精度往往导致计算开销剧增，而轻量化设计又常常牺牲特征表达能力和准确性。
- **现实影响**：这种矛盾限制了注意力机制在计算资源有限的医疗环境（如偏远地区、低算力设备）中的部署，加剧医疗资源不均，不利于数字健康公平。
- **整体目标**：受放射科医生阅片时**优先关注差异性显著区域**这一临床观察的启发，提出一种**无参数、不增加可训练参数计算复杂度**的注意力机制，在提升分割精度的同时保持模型轻量。

## 2. 方法论
### 2.1 核心思想
- **邻域自差异性注意力 (NSDA)**：摒弃传统基于成对相似度的自注意力，转而**量化每个元素与其邻域之间的差异性**，对差异大的区域赋予更高注意力权重，引导网络聚焦于高辨识度的结构边界和病变区域。

### 2.2 关键设计
- **动态邻域缩放 (DyNS)**：
  - 根据特征图分辨率自适应调整邻域窗口大小，防止深层网络因固定窗口过大导致局部特征被过度平滑。
  - 窗口尺寸 \( b_L \) 与特征图尺寸 \( B_L \) 和缩放因子 \( S \)（经验取8）相关：\( b_L = \left\lfloor \frac{B_L}{S} \right\rfloor + c \)，其中 \( c \) 确保窗口尺寸为奇数以保持左右对称。
- **邻域检查**：
  - 模仿医生从焦点到上下文的观察模式，对每个位置 \( x_{i,j} \) 计算其局部窗口内的均值 \( y_{i,j} \) 和方差 \( \sigma_{i,j}^2 \)，用以表征邻域特征分布。
- **差异性量化**：
  - 利用**高斯核的补集**构造差异性度量：\( a_{i,j} = 1 - \exp\left(-\frac{\|x_{i,j} - y_{i,j}\|^2}{2\sigma_{i,j}^2}\right) \)。
  - 该度量天然满足注意力权重的非线性响应和 \( [0,1] \) 有界性要求，且强制保证相似度与差异度之和为1。
- **注意力融合**：
  - 采用残差连接融合：\( z_{i,j} = x_{i,j} \cdot a_{i,j} + x_{i,j} \)，避免传统直接相乘导致特征弱化。
  - 整个过程**无任何可训练参数**（无卷积、无MLP），完全基于统计量和高斯核运算。

### 2.3 公式/算法流程摘要
1. 给定特征图 \( X \)，根据当前层特征图尺寸由 DyNS 确定邻域窗口大小。
2. 对每个空间位置，通过局部平均池化和方差计算，获得邻域均值 \( y_{i,j} \) 和方差 \( \sigma_{i,j}^2 \)。
3. 利用高斯核补集计算差异性权重 \( a_{i,j} \)，生成注意力图 \( A \)。
4. 通过残差连接将注意力权重作用到原始特征图：\( Z = (X \odot A) \oplus X \)。

## 3. 实验设计
### 3.1 数据集与场景
- **医学图像分割**：
  - **Synapse**：多器官腹部CT分割（9个器官），162例，192个切片，分辨率256×256。
  - **ACDC**：心脏MRI分割（左右心室、心肌），100例，每个序列12帧，分辨率256×256。
  - **BUSI**：乳腺超声分割（良性/恶性/正常），780张图像。
- **检测**：COVID-19肺炎病灶检测 (CPLDet)。
- **分类**：内镜膀胱组织分类 (EBTCls)。
- **自然图像分割**：PASCAL VOC07+12 语义分割 (VOCSeg)。

### 3.2 对比方法
- **注意力机制**：SE、CBAM、ECA、BAM、SimAM、CA、GC、MHSA、MWSA、MLKA、CGA、CAA、CMO、MSCAM等经典及轻量级注意力。
- **主干网络**：U-Net、TransUNet、UNeXt、TinyU-Net（涵盖重型和轻型网络）。
- **额外对比**：在AttU-Net中替换原始注意力模块，以及在其他任务（检测、分类、自然图像分割）中集成NSDA。

## 4. 资源与算力
- 实验使用 **NVIDIA GeForce RTX 4090 GPU**（单卡）。
- 模型训练300 epoch，优化器Adam，初始学习率 \( 1\times10^{-4} \)，余弦退火衰减最低至 \( 1\times10^{-6} \)。
- FLOPs通过THOP工具测量，符合常规基准报告方式。论文未详细说明单个实验的训练时间，但主要从参数量、FLOPs和吞吐量评估算力效率。

## 5. 实验数量与充分性
- **大型主实验**：在3个医学分割数据集上，4个经典分割网络（U-Net、TransUNet、UNeXT、TinyU-Net）搭载14种注意力模块，共产生168组基线对比（表1），非常充分。
- **跨任务泛化**：进一步在检测、分类、自然图像分割任务上，将NSDA与若干注意力竞争（表2）。
- **消融实验**：
  - DyNS有效性（4个网络 × 7种静态窗口大小 vs 动态窗口，图3）。
  - 缩放因子S敏感性（表3）。
  - 高斯核方差系数影响（表3）。
  - 相似度 vs 差异度比较（表4），包括高斯核相似度、欧氏距离+sigmoid的差异度。
- 所有对比均在相同训练策略下进行（数据增强、相同损失函数、训练轮次），客观公平。Sensitivity实验报告了三次随机种子的均值和标准差。

## 6. 主要结论与发现
- **NSDA实现显著的精度提升**：在多个基准上，NSDA增强的U-Net、TransUNet、UNeXt、TinyU-Net均获得最高平均Dice系数（例如U-Net+NSDA在Synapse上达81.62% vs 原始78.18%；TransUNet+NSDA达83.81% vs 79.89%）。
- **突破精度-复杂度权衡**：NSDA不引入额外可训练参数，在TinyU-Net上保持0.48M参数、3.39G FLOPs，仍将Synapse上的DSC从78.33%提升至81.57%，速度仅轻微下降；在TransUNet上参数0增加，DSC提升3.92个百分点。
- **传统注意力在医学分割中效果有限**：168组基线中有79%的注意力集成结果反而低于原始网络，表明全局上下文聚合带来的特征同质化损害了局部解剖结构的精细分割。
- **差异性优于相似性**：实验证明基于差异的注意力（DiSim、EDiSim）优于基于相似度的设计，且NSDA的基于高斯核补集的方法效果最优，同时优于MHSA/MWSA等成对相似度自注意力。
- **DyNS有效性**：固定窗口大小的所有配置均不如动态邻域缩放，且窗口过大或过小均导致性能下降，证明自适应调节的重要性。
- **良好的可解释性**：Grad-CAM可视化显示NSDA引导网络聚焦于真实病变和器官边界，有助于增强临床信任。

## 7. 亮点
- **参数自由**：完全基于局部统计和高斯核，无需任何可学习参数，极易集成到任何架构中。
- **临床先验驱动**：明确模仿放射科医生的邻域检查与差异优先策略，设计具有内在可解释性。
- **动态窗口设计**：DyNS策略简单而有效，跨层级适配特征图分辨率，保持细粒度特征。
- **多任务多架构验证**：大量实验覆盖分割、检测、分类，验证了出色的泛化能力。
- **公平全面的对比**：不仅与单类注意力对比，还提供了轻量化和重型网络的横向对比，结论可靠。

## 8. 不足与局限
- **依赖邻域方差估计**：差异性度量的可靠性受邻域方差影响，极端均匀区域或噪声可能影响权重准确性。
- **窗口尺度因子经验性**：缩放因子S固定为8，虽然进行了敏感性分析，但可能不是所有网络和数据的最优值。
- **未在超大型3D医学图像上验证**：实验均为2D切片分割（256×256），对3D体积数据（如CT全容积）的扩展性和效果未评估。
- **吞吐量略有下降**：相比原始网络，NSDA引入局部聚合计算导致轻微FPS下降（例如U-Net从298降至130），在极高实时性要求场景下可能仍存优化空间。
- **未与最新Transformer专用注意力对比**：主要对比通用和经典注意力，缺少与医学图像领域最前沿的特定注意力机制的直接比较（不过覆盖了多数常用方案）。
- **部署限制因素未完全解决**：作者指出，轻量神经网络结构本身的大小仍是低资源场景的限制，NSDA只解决了注意力模块的复杂度，未改变基础网络规模。

（完）
