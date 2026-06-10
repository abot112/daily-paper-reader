---
title: "GauSAM: Contour‑Guided 2D Gaussian Fields for Multi‑Scale Medical Image Segmentation with Segment Anything"
title_zh: GauSAM：基于轮廓引导的2D高斯场多尺度医学图像分割与Segment Anything模型
authors: "Jinxuan Wu, Jiange Wang, Dongdong Zhang"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=7LulWI9QJy"
tags: ["query:abdk-seg"]
score: 7.0
evidence: 提出一种基于Segment Anything模型的深度学习多尺度医学图像分割方法
tldr: 现有医学图像分割方法在保持空间连续性和高频边界细节方面存在不足。GauSAM将轮廓引导的2D高斯概率场融入Segment Anything模型，通过可学习的二维高斯原语参数化分割掩码，并结合Contourlet变换提取多方向频率信息，实现多尺度平滑且精确的分割。实验表明该方法在医学数据集上平衡了不同分辨率下的分割性能。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-7lulwi9qjy/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1399, \"height\": 545, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7lulwi9qjy/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1311, \"height\": 1080, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7lulwi9qjy/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1367, \"height\": 389, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7lulwi9qjy/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1390, \"height\": 873, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-7lulwi9qjy/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 971, \"height\": 658, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-7lulwi9qjy/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1209, \"height\": 504, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7lulwi9qjy/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 491, \"height\": 520, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7lulwi9qjy/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1438, \"height\": 218, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7lulwi9qjy/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1374, \"height\": 285, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7lulwi9qjy/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 685, \"height\": 536, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7lulwi9qjy/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1298, \"height\": 256, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7lulwi9qjy/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1428, \"height\": 624, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7lulwi9qjy/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1297, \"height\": 247, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7lulwi9qjy/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1441, \"height\": 234, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7lulwi9qjy/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 584, \"height\": 265, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7lulwi9qjy/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1436, \"height\": 159, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-7lulwi9qjy/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1157, \"height\": 189, \"label\": \"Table\"}]"
motivation: 解决多尺度医学图像分割中空间连续性与高频边界细节难以同时保持的问题。
method: 将轮廓引导的二维高斯概率场与Segment Anything模型结合，利用Contourlet变换提取边缘和纹理信息。
result: 在多个医学数据集上展示了平衡多分辨率分割性能的能力。
conclusion: GauSAM有效提升了医学图像分割的空间连续性和边界精确性。
---

## Abstract
Effective multiscale medical image segmentation requires simultaneously preserving smooth spatial continuity and accurately delineating high-frequency boundaries, yet pixel-wise decoders often fail to maintain this balance consistently across varying resolutions. We introduce GauSAM, which seamlessly integrates contour‑guided 2D Gaussian probability fields into the Segment Anything Model to address these challenges. In our framework, segmentation masks are parameterized as continuous probability fields of learnable 2D Gaussian primitives, enforcing spatially smooth and structurally consistent. Contourlet transforms extract rich multidirectional frequency information, notably edges and fine textures, which dynamically guide the spatial distribution of Gaussian primitives to substantially improve boundary fidelity in complex structures. The incorporation of these high-frequency contour priors also enriches the expressive capacity of the SAM image encoder. Extensive experiments on diverse 2D medical segmentation tasks confirm that GauSAM consistently delivers robust generalization and state-of-the-art performance with only 1.2M trainable parameters. The official implementation of GauSAM is publicly available at https://github.com/Quinten-Wu504/GauSAM.

---

## 论文详细总结（自动生成）

## GauSAM 论文详细总结

### 1. 论文的核心问题与整体含义
- **研究背景**：医学图像分割要求同时保持平滑的空间连续性和精确的高频边界（如器官边缘、息肉轮廓），但传统像素级解码器在不同分辨率下容易出现离散化伪影与边界模糊，难以维持这种平衡。
- **核心挑战**：现有离散方法（如U-Net、SAM微调）依赖固定网格，跨分辨率泛化能力弱；连续隐式表征方法（INR）虽支持连续坐标，但随机采样策略忽略局部轮廓与方向纹理，难以捕捉精细结构。
- **解决思路**：论文提出 **GauSAM**，首次将**连续2D高斯概率场**与**Segment Anything Model (SAM)** 相结合，并引入**非下采样Contourlet变换（NSCT）** 提取多尺度、多方向轮廓先验，以引导高斯原语的空间分布，从而在任意分辨率下生成轮廓清晰、空间平滑的分割掩码。

### 2. 方法论
#### 2.1 总体流程
- **第一阶段**：对SAM图像编码器进行**轮廓增强**。利用NSCT提取输入图像的轮廓能量图 \(E\)，通过设计的**轮廓传播单元（CPU）** 将轮廓特征逐层注入ViT编码块，并在传播过程中自适应重加权和软融合，使编码器具备多尺度、多方向的轮廓敏感能力。
- **第二阶段**：**2D高斯连续场解码**。从一组可学习的各向异性2D高斯原语叠加成连续特征场，再经过轻量分割头输出类别概率场。通过在原语位置引入**轮廓引导的位置漂移（Contour‑Guided Position Drift）**，使高斯核向语义边界偏移，从而强化轮廓对齐。

#### 2.2 关键技术细节（文字说明，公式已省略）
- **轮廓特征提取**：使用NSCT将图像分解为多级、多方向子带，再通过对数压缩和伽马校正聚合为单一轮廓能量图，以突出弱轮廓并抑制强噪声（如体液反光）。
- **轮廓传播单元（CPU）**：每个Transformer块接收图像特征 \(F_\ell\) 和轮廓特征 \(E_\ell\)，通过轻量MLP对\(E_\ell\)进行通道加权，然后以残差方式融合到图像嵌入流中，并将更新后的 \(E'_\ell\) 传递到下一块，保证结构信息贯穿编码全过程。
- **2D高斯连续概率场**：由 \(N\) 个2D高斯原语（均值 \(\mu_i\)、协方差 \(\Sigma_i\)、不透明度 \(\xi_i\)）加权叠加构成连续特征场 \(X(p)\)。协方差和不透明度从一个**可学习模板库**中通过Gumbel‑Softmax机制软选择而得，以减少参数量、提升训练稳定性。
- **轮廓引导的位置漂移**：利用轮廓编码器提供的轮廓特征 \(u_i\) 通过MLP预测一个小偏移量 \(\Delta\mu_i\)（经tanh约束），更新高斯中心 \(\mu_i = p_i + \Delta\mu_i\)，使原语主动靠近边界。
- **训练策略**：SAM的ViT骨干冻结，仅在Q/V投影层插入**LoRA适配器**（rank=4）；新引入的模块（轮廓增强、高斯场解码）全量训练。使用混合Dice‑CE损失监督。

### 3. 实验设计
- **数据集**：
  - 二进制息肉分割：Kvasir‑Sessile（源域），跨域测试用CVC‑ClinicDB；
  - 多类器官分割：BCV（13类），跨域测试用AMOS（仅肝脏）；
  - 补充实验：REFUGE2（视盘/视杯）、BUSI（乳腺超声病灶）。
  - 所有3D数据转为2D切片，按6:2:2划分训练/验证/测试集。
- **对比方法**：
  - 离散方法：U‑Net、Res2UNet、nnUNet、MedSAM；
  - 连续/隐式方法：OSSNet、IOSNet、SwIPE、I‑MedSAM（此前SOTA）。
- **评估指标**：Dice系数、Hausdorff距离（HD）。额外评估跨分辨率（384→128、384→896）和跨域泛化能力。

### 4. 资源与算力
- **训练硬件**：4块 NVIDIA H20 GPU。
- **训练时长**：息肉分割约3小时，多器官分割约50小时。
- **推理测试**：在单块 NVIDIA RTX 4090 上测延迟，输入512×512，批量大小为1，平均188 ms/帧。去掉NSCT后延迟降至79 ms，说明NSCT是主要计算瓶颈（但文章未提供训练期间的GPU显存消耗细节）。

### 5. 实验数量与充分性
- **主实验**：分别在两个主要基准上对比了8种方法，报告了均值±标准差（6次不同种子），并统计可训练参数量。
- **跨域泛化**：训练于源域、测试于目标域，覆盖息肉和器官两种迁移情景。
- **跨分辨率泛化**：在Kvasir‑Sessile上评估训练分辨率（384）到低分辨率（128）和高分辨率（896）的稳定度。
- **边界质量**：单独比较了HD指标，辨识出在多器官源域测试中HD不占优的局限性。
- **消融实验**：
  - 核心模块消融（高斯场、CPU、位置漂移）在三类设置（域内、跨域、跨分辨率）下的消融；
  - 轮廓提取方法消融（NSCT vs. FFT、Canny、Wavelet、Sobel）；
  - 高斯模板库大小（50/100/300/500/800/1000）的影响；
  - 计算效率部件分解表。
- **额外验证**：在REFUGE2和BUSI上补齐模态，对抗模糊边界图像做了低质量鲁棒性分析，并定性展示了NSCT边缘图的效果。
- **公平性**：所有方法采用相同数据划分和评估协议；离散方法使用输入自适应（如nnUNet*）确保对比公正。
- 总体来看，实验设计系统、全面，能够支撑论文的核心主张。

### 6. 主要结论与发现
- GauSAM在二进制息肉分割（Dice 94.76%）和多类器官分割（Dice 89.75%）上达到**SOTA性能**，且仅需1.2~2.9M可训练参数。
- 在**跨域**和**跨分辨率**情景下均展现出显著优势，尤其跨域迁移时Dice大幅领先（如Kvasir→CVC为91.79%）。
- 高斯连续场与轮廓引导机制有效提升了边界连续性、平滑性和抗伪影能力，在低质量模糊图像上提升尤为明显（高模糊子集增益+7.3% Dice）。
- 当前的多器官HD表现说明单连续场对多类小物体仍有局限性。

### 7. 优点
- **新颖性**：首次将2D高斯溅射构建为SAM的连续概率场，并引入NSCT轮廓先验实现边界感知，是连续表征与基础模型融合的创新范例。
- **参数效率**：仅需极少可训练参数（1.2~2.9M），显著低于同等性能的对手，易于部署。
- **泛化能力强**：跨域、跨分辨率表现稳健，且额外扩充了眼科、超声等模态，验证了方法的通用性。
- **可解释性设计**：轮廓提取、高斯场叠加、位置漂移等模块都有清晰的物理/几何含义，非黑箱。
- **完备的消融与分析**：主模块、轮廓提取方式、高斯库大小、计算开销拆分等实验层次清晰，支撑每个设计选择。

### 8. 不足与局限
- **多类分割小物体精度**：BCV多器官任务中HD偏高，根源在于单连续场难以同时精细刻画所有类别，尤其是小器官。文中也承认这是“刻意取舍”（若采用多场会膨胀参数）。
- **计算效率瓶颈**：整个推理延迟的58%来自NSCT模块（109 ms），且现有NSCT实现老旧、未经CUDA优化，阻碍实时应用。
- **2D局限性**：当前仅处理2D切片，直接将3D容积转为切片会牺牲空间连续性，文中虽给出3D理论扩展，但未实际验证。
- **对比方法范围**：尽管包含主流离散和连续方法，但未对比同期其他高斯溅射分割方案（如有），但作为首创，此点可接受。
- **鲁棒性测试**：跨域实验仅单一目标域，未在更多样化的临床场景（如不同设备、噪声水平）下全面压力测试。

（完）
