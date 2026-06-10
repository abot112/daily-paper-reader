---
title: Native Segmentation Vision Transformers
title_zh: 原生分割视觉Transformer
authors: "Guillem Braso, Aljosa Osep, Laura Leal-Taixé"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=V7RRnsAlbY"
tags: ["query:abdk-seg"]
score: 6.0
evidence: 无单独分割头的通用视觉Transformer；可潜在用于监督腹部器官分割
tldr: 提出原生分割视觉Transformer，通过内容感知的空间分组层在特征提取中直接产生分割掩码，无需额外分割头。该通用架构可应用于全监督的腹部器官分割任务，为医学图像分割提供新的设计思路。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-v7rrnsalby/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1409, \"height\": 379, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-v7rrnsalby/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1439, \"height\": 404, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-v7rrnsalby/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1453, \"height\": 2111, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-v7rrnsalby/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 618, \"height\": 290, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-v7rrnsalby/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1451, \"height\": 1717, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-v7rrnsalby/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1442, \"height\": 496, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-v7rrnsalby/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 818, \"height\": 881, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-v7rrnsalby/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 671, \"height\": 553, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-v7rrnsalby/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 673, \"height\": 289, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-v7rrnsalby/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 708, \"height\": 284, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-v7rrnsalby/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 770, \"height\": 300, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-v7rrnsalby/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 829, \"height\": 196, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-v7rrnsalby/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 890, \"height\": 985, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-v7rrnsalby/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 829, \"height\": 332, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-v7rrnsalby/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1020, \"height\": 143, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-v7rrnsalby/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 818, \"height\": 543, \"label\": \"Table\"}]"
motivation: 传统下采样无法保留语义结构，需要更高效的分割表示。
method: 设计内容感知的空间分组层，堆叠形成层次化原生分割。
result: 无需分割头即可产生强分割掩码。
conclusion: 为分割任务提供了新的原生骨干范式，可迁移至医学分割。
---

## Abstract
Uniform downsampling remains the de facto standard for reducing spatial resolution in vision backbones. In this work, we propose an alternative design built around a content-aware spatial grouping layer that dynamically assigns tokens to a reduced set based on image boundaries and their semantic content. Stacking our grouping layer across consecutive backbone stages results in hierarchical segmentation that arises *natively* in the feature extraction process, resulting in our coined Native Segmentation Vision Transformer.
We show that a careful design of our architecture enables the emergence of strong segmentation masks solely from grouping layers, that is, without additional segmentation-specific heads. This sets the foundation for a new paradigm of *native*, backbone-level segmentation, which enables strong zero-shot results without mask supervision, as well as a minimal and efficient standalone model design for downstream segmentation tasks.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义（研究动机和背景）
- 现代层次化视觉骨干网络普遍采用**均匀、固定模式的下采样**（如池化、步长卷积），对所有空间位置一视同仁，完全忽略图像内容。
- 这种均匀下采样导致特征图在后续上采样时出现**特征错位**，迫使分割模型必须依赖专门设计的**解码头**（如 UPerNet、Mask2Former）来弥补信息损失，增加了系统复杂度。
- 已有一些工作尝试在骨干中引入基于内容的像素分组，但或者计算复杂度与输入分辨率呈**平方关系**（如使用稠密交叉注意力的方法），或者依赖**不可微分**的聚类算法，限制了可扩展性，且仍需要外部解码头。
- 本文旨在提出一种**原生分割**（Native Segmentation）范式，让骨干网络在特征提取过程中**自然形成**层次化的分割能力，彻底替代均匀下采样，使分割掩码直接从骨干中产生，而无需单独的解码头。

## 2. 论文提出的方法论
### 2.1 核心思想
- 设计一种**内容感知的空间分组层**（Spatial Grouping Layer），学习将输入令牌动态分配到更少的一组输出令牌，分配过程尊重图像边界和语义内容。
- 将分组层堆叠在骨干的多个阶段之间，构成**层次化的原生分割**，最终输出令牌直接对应不同粒度的图像区域，上采样即可获得全图分割掩码。

### 2.2 关键技术与算法流程
- **分组算法（Algorithm 1）**  
  将任务建模为可微分的迭代聚类，受到 K-means 和 Slot Attention 的启发。
  1. 使用步长卷积初始化输出令牌 Xout（作为初始聚类中心）。
  2. 迭代 L 次（L=3）：
     - 通过交叉注意力计算输入令牌与输出令牌之间的**软分配矩阵** Aups（行归一化），其中引入**相对位置偏置**，并加入**稀疏掩码** Mloc 以限制分组范围（局部或全局）。
     - 对 Aups 进行**列归一化**得到 Adown，再使用其转置加权聚合输入令牌的值，更新输出令牌 Xout。
     - 应用残差连接和前馈网络（MLP）进一步变换。
  3. 最终输出新的 Xout 以及两者分配矩阵 Aups 和 Adown。
- **局部与密集分组**  
  - 高分辨率特征图（阶段 2、3）采用**局部窗口**（3×3）分组，严格限制每个输出令牌只关注其空间邻域内的输入令牌，计算复杂度从 \(O(LN^2d)\) 降为 \(O(LNd)\)，实现线性可扩展性。
  - 最后阶段（阶段 4）使用**密集分组**（全局窗口），使最终令牌能够聚合整图信息，形成完整的分割掩码。
- **分配矩阵的组合与上采样**  
  将多阶段分配矩阵视为马尔可夫状态转移矩阵，通过矩阵乘法（根据稀疏性进行高效实现）可以将任意阶段的令牌**上采样或下采样**至其他阶段的分辨率，实现骨干级别的原生分割，无需额外上采样操作。
- 在需要掩码监督时，最终组令牌通过简单的 MLP 分类，结合分配矩阵上采样，即可用于语义/全景分割，或用作文本嵌入的相似度计算实现零样本分割。

## 3. 实验设计
### 3.1 无掩码监督实验
- **ImageNet 分类**  
  在 ImageNet-1k 和 ImageNet-22k 上预训练，遵循 Swin Transformer 的设置。  
  验证分类性能的同时，定性展示分组层产生的超像素式结构和语义区域。
- **零样本文本监督语义分割**  
  使用 CC3M、CC12M（以及扩展的 RedCaps12M）图文对，以对比损失训练 SeNaTra。  
  在 **Pascal VOC、Pascal Context、COCO-Object、COCO-Stuff、Cityscapes、ADE20k** 六个基准上评估零样本 mIoU，对比方法包括：CLIP 基方法（ViL-Seg, SegCLIP）、从头训练的分组方法（GroupViT, CoCu, SimSeg 等）以及其他 SOTA（TCL, CoDe, PGSeg）。

### 3.2 有掩码监督实验
- **语义分割**  
  在 **ADE20k**（150 类）上微调，比较 SeNaTra 原生掩码模型（仅用 MLP）与 Swin/NAT 等人搭配 UperNet/Mask2Former 的性能。  
  同时展示 SeNaTra 作为 Mask2Former 的 backbone 替换带来的提升。
- **全景分割**  
  在 **COCO-Panoptic** 上进行类似评估，指标为 PQ。对比原生模型与 MaskFormer、Mask2Former 等加不同骨干的性能。

### 3.3 消融实验
- 分组在**不同骨干阶段**的影响（替换为均匀下采样）。
- 分组层**内部设计**（如 GRU → 残差连接、可学习嵌入初始化、相对位置编码等）。
- **分割范式**对比：纯原生、加像素解码器、加 Transformer 解码器，对语义/全景分割的增益。

### 3.4 效率分析
- 延迟、吞吐量、显存占用，比较 CUDA 优化稀疏实现与朴素实现、均匀下采样基线，在不同输入分辨率下的表现。

## 4. 资源与算力
- **硬件**：实验全部使用 **NVIDIA A100** GPU（40 GB）。
- **典型的算力消耗**：
  - ImageNet-1k 预训练：**8 卡 A100，约 36 小时**。
  - ImageNet-22k 预训练：**16 卡 A100，约一周**；微调至 1k：**8 卡 A100，约 6 小时**。
  - 图文预训练（CC3M+CC12M）：**16 卡 A100，约 2 天**；添加 RedCaps 后约 **4 天**。
  - 有监督语义分割（ADE20k）：**8 卡 A100，约 6 小时**。
  - 全景分割（COCO-panoptic）：**8 卡 A100，约 2.5 天**。

## 5. 实验数量与充分性
- 实验覆盖 **3 种监督范式**（纯分类、图文对比、掩码监督），**6 个零样本评估数据集**，**2 个全监督密集预测数据集**，以及多个模型规模（Tiny/Base/Large）。
- 对比方法多达 **15 种以上**，包括标准骨干+解码头、基于分组的骨干等，对比公平，多使用相同的训练食谱。
- 消融实验对 **分组阶段配置、层内部组件、分割范式组合** 都做了控制变量研究，充分验证了每个设计的必要性。
- 提供了效率分析，证明方法在可扩展性上的优势，实验整体**客观、充分、公平**。

## 6. 论文的主要结论与发现
- 通过将均匀下采样替换为可微分的空间分组层，**无需任何掩码监督**，视觉骨干即可自动学习具有边界意识的层次化区域分组，早期层涌现超像素，最终层出现语义区域。
- 在**零样本文本监督分割**中，SeNaTra 显著超越未使用 CLIP 的方法，且在多数数据集上优于部分使用 CLIP 的方法，表现出极高的数据效率。
- 在**有监督分割**中，仅靠原生掩码即可达到或超过传统骨干+解码头组合的表现，且**参数更少、FLOPs 更低**；若再结合 Mask2Former，能进一步提升 SOTA 性能。
- 分组层的设计（残差连接、步长卷积初始化、局部/密集分组、相对位置编码）相较于原生 Slot Attention 对稳定性和性能均有大幅改善。
- 该方法在计算上可通过稀疏 CUDA 操作实现近似线性扩展，使高分辨率输入下的实用成为可能。

## 7. 优点
- **创新性强**：首次提出将内容感知的下采样作为骨干的核心组件，实现原生分割，打破“骨干提取特征+解码头”的传统范式。
- **全可微、端到端**：整个框架可从图像级标签或图文对直接训练，无需不可微中间步骤。
- **高效可扩展**：通过局部窗口分组实现线性复杂度，稀疏实现使高分辨率输入可部署。
- **表现优异**：在零样本和为多个有监督基准上均达到或超越同期先进方法，消融实验有力支撑了每个设计选择。
- **通用性**：可作为独立模型直接输出分割结果，也可作为即插即用的 backbone 增强现有分割框架。

## 8. 不足与局限
- **计算开销**：相较于均匀下采样，分组层仍引入约 **20‑40% 的骨干延迟**，在仅作特征提取而未利用其原生分割能力时，效率不占优。
- **实例分割能力偏弱**：在全景分割中，原生模型的提升幅度小于语义分割，可能因为 ImageNet 预训练不区分同类的不同实例，缺乏实例级分组归纳偏置。
- **仅探索 Transformer 架构**：方法在全 Transformer 骨干（NAT 基础）上验证，尚未在 CNN 等其他架构上测试泛化性。
- **未利用更大规模图文预训练**：零样本实验未像 CLIP 那样使用 4 亿数据，但通过添加少量 RedCaps 数据已展现良好的 scaling 趋势，更大规模预训练效果待验证。
- **代码暂未公开**：尽管实验细节详尽，且承诺开源，但目前还无法直接复现。
- **可能偏好语义而非实例**：预训练任务设计可能影响模型对不同粒度分组的能力，需要更有针对性的预训练方案。

（完）
