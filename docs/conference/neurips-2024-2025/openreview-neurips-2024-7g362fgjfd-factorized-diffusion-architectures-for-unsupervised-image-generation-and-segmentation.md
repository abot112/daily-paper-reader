---
title: Factorized Diffusion Architectures for Unsupervised Image Generation and Segmentation
title_zh: 因子化扩散架构用于无监督图像生成与分割
authors: "Xin Yuan, Michael Maire"
date: 2024-09-25
pdf: "https://openreview.net/pdf?id=7G362fgJFd"
tags: ["query:abdk-seg"]
score: 7.0
evidence: 该无监督扩散模型直接应用于CT多器官分割，在无需标注的情况下实现了具备竞争力的腹部器官分割性能。
tldr: 针对完全无监督下同时生成图像和语义分割的挑战，本文设计了一种因子化扩散模型，其网络结构蕴含计算瓶颈，迫使模型在去噪过程中将输入图像划分为多个区域并行处理。该模型仅通过扩散去噪目标训练，无需任何标注即可学习分割。直接应用于CT多器官分割任务时，取得了与全监督方法可比的分割效果，验证了无监督学习在医学影像分割中的巨大潜力，为腹部器官分割提供了免标注的新思路。
source: NeurIPS-2024-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1413, \"height\": 653, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1441, \"height\": 709, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 681, \"height\": 381, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 680, \"height\": 380, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 681, \"height\": 380, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 682, \"height\": 380, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 689, \"height\": 384, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 685, \"height\": 384, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 682, \"height\": 381, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 696, \"height\": 234, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 700, \"height\": 262, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1415, \"height\": 516, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1437, \"height\": 458, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1340, \"height\": 866, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1355, \"height\": 965, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1366, \"height\": 1122, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1390, \"height\": 348, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1419, \"height\": 757, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1421, \"height\": 753, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1418, \"height\": 756, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1418, \"height\": 752, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1411, \"height\": 427, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1421, \"height\": 753, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1420, \"height\": 750, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1418, \"height\": 752, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1411, \"height\": 428, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 1415, \"height\": 431, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2024-7g362fgjfd/fig-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 1429, \"height\": 368, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2024-7g362fgjfd/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 738, \"height\": 551, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-7g362fgjfd/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 707, \"height\": 554, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-7g362fgjfd/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 714, \"height\": 317, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-7g362fgjfd/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 714, \"height\": 357, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-7g362fgjfd/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 725, \"height\": 257, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-7g362fgjfd/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 727, \"height\": 260, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-7g362fgjfd/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1389, \"height\": 275, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-7g362fgjfd/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 699, \"height\": 278, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2024-7g362fgjfd/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1286, \"height\": 946, \"label\": \"Table\"}]"
motivation: 完全无监督的图像分割缺乏有效机制，现有无监督方法在医学图像上性能不足。
method: 设计具有计算瓶颈的因子化扩散架构，迫使网络在去噪时隐式划分区域，实现无监督分割生成。
result: 在CT多器官分割任务上，无监督模型直接应用即取得与全监督方法可比的性能。
conclusion: 因子化扩散架构为腹部CT多器官分割提供了无需标注的有效途径，推动了无监督医学分割研究。
---

## Abstract
We develop a neural network architecture which, trained in an unsupervised manner as a denoising diffusion model, simultaneously learns to both generate and segment images.  Learning is driven entirely by the denoising diffusion objective, without any annotation or prior knowledge about regions during training.  A computational bottleneck, built into the neural architecture, encourages the denoising network to partition an input into regions, denoise them in parallel, and combine the results.  Our trained model generates both synthetic images and, by simple examination of its internal predicted partitions, semantic segmentations of those images.  Without fine-tuning, we directly apply our unsupervised model to the downstream task of segmenting real images via noising and subsequently denoising them.  Experiments demonstrate that our model achieves accurate unsupervised image segmentation and high-quality synthetic image generation across multiple datasets.

---

## 论文详细总结（自动生成）

### 1. 研究动机与核心问题
本文旨在解决**完全无监督场景下，同时实现图像生成与语义分割**这一挑战。传统自监督或生成模型虽能提取语义信息，但通常仍需标注数据进行下游微调（如线性探测）才能完成分割任务，或者依赖额外的先验与损失项。作者提出一种新的范式：**通过设计含有计算瓶颈的扩散模型架构，使得模型在仅使用去噪目标训练时，被迫学习将图像分解为不同区域并行去噪，从而在生成图像的同时，免费获得图像分割能力**，无需任何像素标注。

### 2. 方法论：因子化扩散架构
核心思想是在 DDPM（去噪扩散概率模型）的 U‑Net 中嵌入一个**区域掩码生成器**，并构建**多路并行解码器**，使去噪任务被显式地分解为对不同区域的去噪子问题。整个网络端到端训练，损失函数仅为标准的噪声预测均方误差（MSE）。

- **编码器（Encoder）**：取标准 U‑Net 前半部分，对加噪图像 \(x_t\) 和时间步 \(t\) 编码，提取多尺度特征 \(h_{enc}\) 及中间瓶颈特征 \(h_{mid}\)。
- **掩码生成器（Mask Generator）**：与 U‑Net 后半部分结构相同，接收 \(h_{mid}\) 及来自编码器的跳跃连接特征 \(h_{enc}\)，通过 softmax 输出 \(K\) 个软掩码 \(m_0, m_1, \dots, m_K\)。
- **并行解码器（Decoder）**：\(K\) 个共享权重的解码器分支，每个分支输入为 \(h_{mid}\) 和按掩码遮盖的编码器特征 \(h_{enc} \odot m_k\)，输出各区域的噪声预测 \(\hat{\epsilon}_k\)。
- **组合去噪输出**：最终噪声预测为 \(\hat{\epsilon} = \sum_{k} \hat{\epsilon}_k \odot m_k\)。
- **训练**：最小化 \(\mathcal{L} = \mathbb{E}\|\epsilon - \hat{\epsilon}\|^2\)，无额外正则项。
- **分割**：对干净图像 \(x_0\)，先按扩散过程加噪到 \(x_t\)，一次前向传播后取出掩码 \(m_k\) 作为分割结果。
- **生成**：从纯噪声开始，执行标准逆扩散过程，在最后一步（\(t=1\)）同时获得生成图像和对应掩码。

文中还初步探索了**层次化因子化扩散**，通过两级级联逐步细化分割，从而处理更复杂的多尺度场景。

### 3. 实验设计与比较方法
#### 数据集与 benchmark
- **分割与生成特性评估**：Flower、CUB、FFHQ、CelebAMask‑HQ、ImageNet（64×64）、PASCAL VOC 2012 和 DAVIS‑2017。
- **评价指标**：分割用 Acc、IoU、Dice；生成用 Fréchet Inception Distance (FID)。

#### 对比方法
- **无监督分割方法**：GrabCut、ReDO、IEM、IEM+SegNet、PerturbGAN。
- **基于扩散模型的方法**：DatasetDDPM（无监督版本，K‑means 聚类）、监督 U‑Net（作为上界）。
- **生成质量**：与标准 DDPM 比较 FID；分割一致性用预训练监督 U‑Net 输出的伪标签来衡量。

### 4. 资源与算力
- **硬件**：64×64 模型使用 8 块 Nvidia V100 32 GB GPU；128×128 模型使用 32 块 V100 GPU；ImageNet 实验使用 32 块 V100 GPU。
- **训练配置**：Flower、CUB、FFHQ 分别训练 5 万、5 万、50 万次迭代，批大小 128；ImageNet 训练 50 万次迭代，批大小 512。优化器 Adam（学习率 \(10^{-4}\)），EMA 衰减率 0.9999，扩散步数 \(T=1000\)。

### 5. 实验充分性与公平性
实验覆盖了**多个尺度和领域的数据集**（花卉、鸟类、人脸、通用物体），进行了**定量对比**（表 1–5）与**定性可视化**。主要实验包括：
- 不同数据集上的分割精度（与先前无监督方法及监督上界对比）。
- 生成图像质量和生成掩码的一致性比较。
- 消融实验：验证并行解码与权重共享的必要性（concat、masking \(h_{mid}\)、无权重共享）。
- 掩码分解可视化、扩散过程中掩码的逐步细化、噪声水平 \(t\) 对分割的影响。
- 零样本迁移至 PASCAL VOC 和 DAVIS 视频分割。
- 面部插值实验和层次化扩散的初步验证。

这些实验设计较为全面，对比基线涵盖经典无监督方法和扩散模型改进，并对核心设计进行了消融，整体公平可靠。

### 6. 主要结论与发现
- 因子化扩散架构能够在**完全无监督**条件下同时生成高质量图像和准确的分割掩码。
- 在多个数据集上，分割性能**超过以往无监督方法**，并显著接近监督 U‑Net 的表现。
- 生成质量（FID）**优于标准 DDPM**，说明按区域并行去噪的结构先验有利于图像建模。
- 训练好的模型**无需微调**即可直接用于真实图像分割，且分割速度快（单次前向传播）。
- 模型还展现出一定的**零样本泛化能力**，在 VOC 和 DAVIS 上获得了合理结果。

### 7. 优点
- **完全无监督**：无需任何像素级标签、先验尺寸或额外损失项。
- **一训多得**：单个模型同时掌握生成和分割两种能力，无需改写训练目标。
- **架构驱动**：通过结构化的计算瓶颈引导网络自发学习有意义的区域分解，是一种新颖的生成式表示学习范式。
- **生成质量提升**：并行区域解码不仅带来分割能力，还提升了生成图像的保真度。
- **可扩展性**：初步展示了层次化扩散处理复杂场景的潜力。

### 8. 不足与局限
- **分割粒度有限**：实验主要针对 2‑3 类的分割（前景/背景/轮廓），对于包含更多类别的复杂场景（如 COCO）未进行验证。
- **零样本依赖类别映射**：VOC 上的零样本分割需要将 ImageNet 类别映射至 VOC 类别，并非真正的开放域分割。
- **未与大规模预训练模型对比**：没有与利用外部大数据（如 LAION）的 Stable Diffusion 衍生方法（如 DiffuMask）进行系统比较，但这些方法使用了额外信息，条件并不对等。
- **代码未即时开源**：论文承诺接收后公开，当前可复现性受限。
- **噪声敏感**：分割时需要手动选择加噪水平 \(t=30\)，对噪声强度敏感，缺乏自适应机制。
- **资源消耗较高**：训练 128² 分辨率模型需 32 块 V100 GPU，对普通研究者可能不够友好。

（完）
