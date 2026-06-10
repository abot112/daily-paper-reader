---
title: "LangDAug: Langevin Data Augmentation for Multi-Source Domain Generalization in Medical Image Segmentation"
title_zh: LangDAug：用于医学图像分割多源域泛化的朗之万数据增强
authors: "Piyush Tiwary, Kinjawl Bhattacharyya, Prathosh AP"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=LB5F02kwAv"
tags: ["query:abdk-seg"]
score: 6.0
evidence: 医学图像分割域泛化数据增强方法
tldr: 针对医学图像分割模型跨域泛化难题，提出LangDAug，一种基于朗之万动态的数据增强方法。该方法利用对比训练的能量模型生成合成样本以丰富训练数据，学习域不变特征，不依赖特定域技巧。在2D医学图像分割中性能与表示学习方法相当或更优，为医学影像数据扩充提供了新框架。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1736, \"height\": 934, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 831, \"height\": 324, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 852, \"height\": 523, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 847, \"height\": 751, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1809, \"height\": 2058, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1648, \"height\": 2095, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1647, \"height\": 2101, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1647, \"height\": 2109, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1645, \"height\": 2103, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1646, \"height\": 2094, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1649, \"height\": 1371, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1645, \"height\": 2100, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1649, \"height\": 1371, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1647, \"height\": 2095, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1648, \"height\": 1371, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1647, \"height\": 2091, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1646, \"height\": 1370, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1646, \"height\": 2093, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1649, \"height\": 1369, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1646, \"height\": 2096, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-lb5f02kwav/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1650, \"height\": 1371, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-lb5f02kwav/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1775, \"height\": 405, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-lb5f02kwav/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1429, \"height\": 501, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-lb5f02kwav/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1773, \"height\": 236, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-lb5f02kwav/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 862, \"height\": 224, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-lb5f02kwav/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1432, \"height\": 174, \"label\": \"Table\"}]"
motivation: 医学图像分割模型跨域泛化困难，现有域泛化方法缺乏形式化保证。
method: 提出LangDAug，利用基于能量的模型通过朗之万动态生成增强样本，用于多源域泛化。
result: 在2D医学图像分割任务上，与表示学习等域泛化方法相比性能相当或更优。
conclusion: 该方法为医学图像分割提供了可靠的增强策略，提升模型跨域鲁棒性。
---

## Abstract
Medical image segmentation models often struggle to generalize across different domains due to various reasons. Domain Generalization (DG) methods overcome this either through representation learning or data augmentation (DA). While representation learning methods seek domain-invariant features, they often rely on ad-hoc techniques and lack formal guarantees. DA methods, which enrich model representations through synthetic samples, have shown comparable or superior performance to representation learning approaches. We propose LangDAug, a novel **Lang**evin **D**ata **Aug**mentation for multi-source domain generalization in 2D medical image segmentation. LangDAug leverages Energy-Based Models (EBMs) trained via contrastive divergence to traverse between source domains, generating intermediate samples through Langevin dynamics. Theoretical analysis shows that LangDAug induces a regularization effect, and for GLMs, it upper-bounds the Rademacher complexity by the intrinsic dimensionality of the data manifold. Through extensive experiments on Fundus segmentation and 2D MRI prostate segmentation benchmarks, we show that LangDAug outperforms state-of-the-art domain generalization methods and effectively complements existing domain-randomization approaches. The codebase for our method is available at https://github.com/backpropagator/LangDAug.

---

## 论文详细总结（自动生成）

好的，作为一名资深学术论文分析助手，我将使用中文、以 Markdown 形式，对这篇论文《LangDAug: Langevin Data Augmentation for Multi-Source Domain Generalization in Medical Image Segmentation》做结构化、深入、客观的总结。

### 1. 论文的核心问题与整体含义

- **核心问题**：医学图像分割模型在训练集（源域）上表现良好，但面对来自不同设备、协议或人群的未见过的测试数据（目标域）时，性能会显著下降，这源于域偏移问题。现有的域泛化方法主要分为表征学习（学习域不变特征）和数据增强两大类，前者缺乏形式化保证，后者则通常更简单有效。
- **整体含义**：本文提出了一种新的数据增强方法 `LangDAug`，旨在通过生成连接不同源域的“桥梁”样本来丰富训练数据的多样性，从而提升2D医学图像分割模型对未见目标域的泛化能力。其核心思想是利用能量模型和朗之万动力学在域之间进行有意义地遍历和采样，并有理论证明其能带来正则化效果，使模型学习到更平坦的损失景观，提升泛化性能。

### 2. 论文提出的方法论

- **核心思想**：在多源域之间生成“中间域”的样本。这相当于在数据流形上对源域进行插值，从而覆盖更广的数据分布，让下游任务模型能够学习到更具泛化性的特征。
- **关键技术细节**：
    - **能量模型训练**：对于每一对源域 `(Di, Dj)`，训练一个能量模型 `E_θij`。训练目标是让模型给来自目标域 `Dj` 的样本低能量，同时给从源域 `Di` 出发、通过朗之万动力学生成的样本高能量。该目标通过对比散度损失函数实现。
    - **朗之万动力学遍历**：训练好的能量模型定义了从一个域到另一个域的路径。从源域 `Di` 的一个样本 `x` 出发，使用能量模型 `E_θij` 执行 `K` 步朗之万动力学（一种基于梯度的MCMC方法），其更新公式为：
        `x_{t+1} = x_t - (α^2/2) * ∇E_θij(x_t) + α * ε, ε ~ N(0, I)`
    - **数据增强**：朗之万动力学迭代过程中的所有中间样本 `{x_t}` 都被保存下来，并赋予与初始样本 `x` 相同的标签 `y`，形成增强数据集。这些样本被认为是连接源域 `Di` 和 `Dj` 的“桥梁”数据。最终，原始数据和所有域对的增强数据一起用于训练下游的分割模型。
- **理论分析**：论文证明了 `LangDAug` 增强的经验风险可以分解为标准经验风险加上三个正则化项，这些正则化项对模型预测函数的梯度、曲率等进行约束。对于广义线性模型，该方法能将拉德马赫复杂度的上界从数据的**环境维度**降低到与数据流形的**内在维度**相关，这在理论上保证了更好的泛化能力。

### 3. 实验设计

- **数据集与场景**：
    - **视网膜眼底分割**：包含来自4个不同临床中心的眼底图像，任务是分割视杯和视盘。
    - **2D MRI前列腺分割**：包含来自6个不同临床中心的T2加权MRI扫描。通过从3D体积中提取2D轴向切片进行处理，任务是分割前列腺。
    - **评估协议**：采用域泛化中标准的留一法进行交叉验证，每次将一个域作为未见过的目标域，其余域作为源域进行训练。
- **基准对比方法**：
    - **通用域泛化方法**：来自DomainBed基准的 Hutchinson, Fish, Fishr。
    - **医学图像分割专用方法**：RandConv, MixStyle, FedDG, RAM, TriD。
    - 所有方法均统一使用基于ResNet34的骨干网络进行公平比较。
- **评估指标**：
    - 视网膜眼底分割：交并比和戴斯相似性系数。
    - 前列腺分割：戴斯相似性系数（2D切片）和平均表面距离（3D重建体积）。

### 4. 资源与算力

- **硬件配置**：论文在“计算成本分析”章节中明确指出，所有关于训练时间和峰值内存的比较实验均在**单个NVIDIA A6000 GPU（48GB显存）**上完成。
- **训练时长**：论文提供了一个详细的比较表格。对于视网膜眼底分割任务，`LangDAug` 的总训练时间（包括能量模型训练和下游分割模型训练）约为 **3.14 GPU小时**。作为对比，基础的经验风险最小化模型训练时间为1.51小时，其他域泛化方法如 `TriD` 为5.53小时，`FedDG` 为4.60小时。

### 5. 实验数量与充分性

- **实验数量**：实验设计相当充分，主要包括：
    - **2个不同类型的数据集**上的全面评估。
    - 与**超过10种**当前最先进的域泛化方法进行比较。
    - **消融研究**：对能量模型的关键超参数进行了详细的消融实验，包括：
        - 朗之万步数 `K`。
        - 朗之万步长 `β`。
        - 能量模型的复杂度（卷积块数量）。
        - 每条朗之万链保存的增强样本数量。
    - **组合实验**：验证了 `LangDAug` 与现有的域随机化方法（`FedDG`, `RAM`, `TriD`）的互补性，表明它能有效提升这些方法的性能。
- **充分性与公平性**：
    - **充分性**：实验覆盖了多个医学图像分割场景，对比方法多样且具有代表性，消融实验系统地分析了关键组件和超参数的影响，组合实验进一步证明了方法的实用价值。
    - **客观性与公平性**：统一使用ResNet34骨干网络、标准数据集和统一的评估协议（留一法），确保了比较的公平性。结果报告为三次独立运行的平均值，增加了结果的可靠性。

### 6. 论文的主要结论与发现

- **性能优越性**：`LangDAug` 在两个数据集上均取得了最优或极具竞争力的结果。尤其在泛化难度大的目标域（如Domain B）上，`LangDAug` 的性能优势更为明显，并且跨域表现更稳定。
- **互补性**：`LangDAug` 能与现有的域随机化方法有效结合，显著提升其性能，显示了强大的通用性和实用潜力。
- **理论支持**：理论分析揭示了 `LangDAug` 的正则化本质，并将其泛化能力与数据的内在维度联系起来，为方法的有效性提供了理论支撑。

### 7. 优点

- **方法创新**：将能量模型和朗之万动力学应用于域泛化的数据增强，构思新颖。生成了连接域分布的“桥梁”样本，而非直接在输入空间或特征空间进行简单的插值或混合。
- **理论扎实**：提供了从损失函数正则化到拉德马赫复杂度上界的完整理论分析，为数据增强方法的效果提供了深刻的解释。
- **实验全面**：涵盖了多个数据集、多种基线方法、详尽的消融实验和组合方法验证，实验结果具有说服力。
- **可解释性强**：通过t-SNE可视化展示了增强样本确实填补了源域之间的空白，直观地解释了方法的工作原理。

### 8. 不足与局限

- **计算开销大**：
    - **训练时间长**：需要为每对源域训练一个能量模型，且增强样本的生成和存储增加了额外的计算负担。
    - **内存消耗高**：如论文所述，`LangDAug` 的峰值内存需求（19.41 GB）高于标准训练（10.36 GB）和一些其他方法。
- **扩展性问题**：随着源域数量 `n` 的增加，需要训练的能量模型数量以 `O(n^2)` 增长，这会成为实践中的一个瓶颈。论文在局限部分也指出了这一点，并提出共享架构等未来方向。
- **领域特定性**：论文指出其设计考虑了医学影像中常见的幅度谱差异等结构变化，可能在其他领域或自然图像上的效果和通用性有待进一步验证。
- **2D切片处理**：目前的方法处理3D体积时是通过将其切片为2D图像进行，未能直接利用完整的3D空间上下文信息。

（完）
