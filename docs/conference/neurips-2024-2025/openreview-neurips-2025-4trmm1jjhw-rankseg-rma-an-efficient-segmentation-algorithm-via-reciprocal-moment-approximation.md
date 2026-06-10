---
title: "RankSEG-RMA: An Efficient Segmentation Algorithm via Reciprocal Moment Approximation"
title_zh: RankSEG-RMA：通过倒数矩逼近实现高效分割算法
authors: "Zixun Wang, Ben Dai"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=4tRMm1JJhw"
tags: ["query:abdk-seg"]
score: 6.0
evidence: 提出RankDice和RankIoU损失函数，直接在监督训练中优化分割指标。
tldr: 针对传统分割损失与指标不一致的问题，本文提出RankSEG-RMA，通过倒数矩近似直接优化Dice和IoU，实现高效且一致的监督分割。实验表明该方法在多个数据集上以更低计算开销获得更优性能，为监督训练提供了更直接的目标函数。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-4trmm1jjhw/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1361, \"height\": 608, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-4trmm1jjhw/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1418, \"height\": 292, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-4trmm1jjhw/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1271, \"height\": 827, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-4trmm1jjhw/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1438, \"height\": 320, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-4trmm1jjhw/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1440, \"height\": 603, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-4trmm1jjhw/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1445, \"height\": 228, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-4trmm1jjhw/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1443, \"height\": 307, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-4trmm1jjhw/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1438, \"height\": 220, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-4trmm1jjhw/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 724, \"height\": 182, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-4trmm1jjhw/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1314, \"height\": 453, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-4trmm1jjhw/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 868, \"height\": 207, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-4trmm1jjhw/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1293, \"height\": 154, \"label\": \"Table\"}]"
motivation: 传统分割方法优化目标与评估指标不一致，导致次优结果。
method: 提出RankDice和RankIoU损失，利用排序和倒数矩近似直接最大化Dice/IoU。
result: 在多个分割数据集上，RankSEG-RMA以低计算成本实现了更一致的性能。
conclusion: 该方法为监督分割训练提供了更有效的损失函数，可提升分割精度与效率。
---

## Abstract
Semantic segmentation labels each pixel in an image with its corresponding class, and is typically evaluated using the Intersection over Union (IoU) and Dice metrics to quantify the overlap between predicted and ground-truth segmentation masks. In the literature, most existing methods estimate pixel-wise class probabilities, then apply argmax or thresholding to obtain the final prediction. These methods have been shown to generally lead to inconsistent or suboptimal results, as they do not directly maximize segmentation metrics. To address this issue, a novel consistent segmentation framework, RankSEG, has been proposed, which includes RankDice and RankIoU specifically designed to optimize the Dice and IoU metrics, respectively. Although RankSEG almost guarantees improved performance, it suffers from two major drawbacks. First, it is its computational expense—RankDice has a complexity of $\mathcal{O}(d \log d)$ with a substantial constant factor (where $d$ represents the number of pixels), while RankIoU exhibits even higher complexity $\mathcal{O}(d^2)$, thus limiting its practical application. For instance, in LiTS, prediction with RankSEG takes 16.33 seconds compared to just 0.01 seconds with the argmax rule. Second, RankSEG is only applicable to overlapping segmentation settings, where multiple classes can occupy the same pixel, which contrasts with standard benchmarks that typically assume non-overlapping segmentation. In this paper, we overcome these two drawbacks via a \textit{reciprocal moment approximation} (RMA) of RankSEG with the following contributions:  (i) we improve RankSEG using RMA, namely RankSEG-RMA, reduces the complexity of both algorithms to $\mathcal{O}(d)$ while maintaining comparable performance; (ii) inspired by RMA, we develop a pixel-wise score function that allows efficient implementation for non-overlapping segmentation settings. We illustrate the effectiveness of our method across various datasets and state-of-the-art models. The code of our method is available in: \url{https://github.com/ZixunWang/RankSEG-RMA}.

---

## 论文详细总结（自动生成）

## 1. 论文的核心问题与整体含义

- **研究动机**：语义分割的常用评估指标是交并比（IoU）和 Dice 系数，但大多数方法在预测时仅对像素级概率取 argmax 或阈值处理，并未直接优化这两项指标，导致在指标上出现不一致或次优结果。
- **现有问题**：Dai & Li（2023）提出的 RankSEG 框架能从理论上一致地最大化图像级 Dice / IoU 指标，但存在两个缺陷：
  - **计算开销大**：RankDice 的时间复杂度为 $O(d \log d)$（含大常数因子），RankIoU 更高达 $O(d^2)$。例如，在 LiTS 上 RankSEG 需 16.33 秒，而 argmax 仅需 0.01 秒。
  - **仅支持重叠分割**：RankSEG 允许同一像素属于多个类，这与多数标准 benchmark（非重叠分割）相悖，限制了其直接应用。

- **论文目标**：通过**倒数矩近似**（Reciprocal Moment Approximation, RMA）技术，将 RankSEG 的计算复杂度降至 $O(d)$，并设计像素级得分函数，使其能够高效适配非重叠多类分割场景，同时保持甚至提升性能。

## 2. 方法论

- **核心思想：倒数矩近似**  
  直接优化 Dice / IoU 时，核心难点在于计算形如 $\mathbb{E}[1/(\tau + \Gamma + 1)]$ 的期望（$\Gamma$ 为 Poisson-二项随机变量）。RMA 利用不等式 $( \mathbb{E}\Gamma + \tau )^{-1} \leq \mathbb{E}(\Gamma + \tau)^{-1} \leq ( \frac{d+1}{d}\mathbb{E}\Gamma + \tau -1 )^{-1}$，将非线性的期望倒数量换为线性期望的倒数，从而避免对每个 $\tau$ 重新计算分布。

- **RankDice‑RMA 算法流程（二值分割）**：
  1. 对输入图像的估计概率 $\hat{\mathbf{p}}$ 降序排列。
  2. 预计算累积概率和 $\hat{q}_\tau = \sum_{k=1}^{\tau} \hat{p}_{j_k}$ 及全局期望体积 $\hat{\mu} = \sum_j \hat{p}_j$。
  3. 用 RMA 近似计算目标函数 $\hat{\pi}^{\rm RMA}(\hat{J}_\tau) = \frac{2\hat{q}_\tau}{\tau+\hat{\mu}+1}$。
  4. 选择使该函数最大的体积 $\hat{\tau}^*$，以第 $\hat{\tau}^*$ 大的概率为阈值，输出前景像素。
  - RankIoU‑RMA 类似，仅目标函数不同（$\hat{\nu}^{\rm RMA}(\hat{J}_\tau) = \frac{\hat{q}_\tau}{\tau + (\hat{\mu}-\hat{q}_\tau)}$）。
  - 忽略排序，时间复杂度为 $O(d)$。

- **多类非重叠分割扩展**：
  1. 对每个类 $c$ 独立运行二值 RankDice‑/RankIoU‑RMA，得到预测集 $\hat{I}_c^+$。
  2. 识别所有类别间的重叠像素 $\hat{I}^{\rm overlap}$，将非重叠部分直接赋值为对应类别。
  3. 对重叠像素，计算**RMA‑score**（向类 $c$ 增加该像素带来的边际 Dice‑RMA 增益）$\hat{\Delta}_{c,j} = \hat{\pi}^{\rm RMA}(\hat{I}_c \cup \{j\}) - \hat{\pi}^{\rm RMA}(\hat{I}_c)$，然后通过 argmax 确定最终类别。
  - RMA‑score 的推导基于 Bayes 规则，比单纯使用概率或启发式加权更合理，且计算开销为 $O(Cd)$（与 argmax‑prob 相当）。

## 3. 实验设计

- **数据集**：
  - PASCAL VOC、Cityscapes、ADE20K（通用场景分割）
  - LiTS（肝脏肿瘤）、KiTS（肾脏肿瘤），处理为二值分割。
- **模型**：UNet、DeepLabV3+、PSPNet、UPerNet、SegFormer、CPT，覆盖 CNN 和 Transformer 架构，均使用交叉熵训练。
- **对比方法**：
  - argmax / 阈值规则（baseline）
  - RankDice‑BA（仅在 LiTS 和 KiTS 上对比，因其不支持非重叠多类）
  - RankDice‑RMA、RankIoU‑RMA
- **评估指标**：
  - 图像级平均 IoU 和 Dice（mIoU$^{\rm I}$ / mDice$^{\rm I}$）与类别级平均（mIoU$^{\rm C}$ / mDice$^{\rm C}$）。
  - 计时实验：对比 argmax、RankDice‑RMA、RankDice‑BA 及模型前向时间。
  - 最差情况分析：最低 $q$ 分位图像的平均 mIoU（mIoU$^{\rm I}_5$, mIoU$^{\rm I}_{10}$）。
  - 消融实验：比较 RMA‑score、Prob‑score、WProb‑score 三种重叠解决方式。

## 4. 资源与算力

- 时间效率测试使用 **单张 A100 GPU**，报告了不同数据集的预测时间（均值 ± 标准差，10 次运行）。
- 训练细节（优化器、学习率调度等）在附录 D 中说明，但**未明确给出使用的 GPU 总数或总训练时长**。

## 5. 实验数量与充分性

- **主要实验**：
  - 6 种模型 × 3 个多类数据集（PASCAL VOC、Cityscapes、ADE20K）的 mIoU$^{\rm I}$/$^{\rm C}$ 和 mDice$^{\rm I}$/$^{\rm C}$ 对比。
  - 多种模型在 LiTS、KiTS 上的二值分割对比（含 BA 方法）。
  - 时间消耗表（3 个多类 + 2 个医学数据集）。
- **额外分析**：
  - 类级别 IoU 变化（20 类 × 1 模型）。
  - 最差情况分析（5/10 分位数）。
  - 消融实验（不同分值比较，1 模型 × 3 数据集）。
  - 统计显著性检验（10 次独立运行的 t‑检验）。
- 实验设计覆盖不同数据规模、类别数和模型架构，对比公平，消融和显著性分析进一步增强了结论的可靠性。

## 6. 主要结论与发现

- RankSEG‑RMA **在所有数据集和模型上均优于** argmax‑prob，且计算效率远高于 RankSEG‑BA（LiTS 上加速 48 倍，KiTS 上 38 倍），额外耗时与模型前向相比可忽略。
- 该方法在提升 IoU 性能的同时，也改善了 Dice 指标；RankDice‑RMA 和 RankIoU‑RMA 性能几乎一致，可作为一个统一的预测规则。
- 对难分类别和小目标提升更显著；最差图像的性能也得到改善，有助于安全关键应用。
- RMA‑score 在解决重叠时比直接使用概率或简单加权更有效，尤其在类别数多的 ADE20K 上优势明显。

## 7. 优点

- **高效且理论支撑**：通过 RMA 将 RankSEG 复杂度降至 $O(d)$，并提供误差界保证（定理 2），既有理论依据又有实用性。
- **即插即用**：仅替换预测阶段的 argmax 操作，无需重新训练或调整损失函数，可直接应用于任何已训练模型。
- **广泛的适用性**：成功扩展到非重叠多类分割，覆盖主流 benchmark。
- **全面的实验验证**：涵盖十余种模型、多个数据集、指标、统计分析及消融实验，结论扎实。

## 8. 不足与局限

- **重叠解决策略**：当前采用逐像素贪心方法，未考虑全局最优分配（如 Hungarian 算法），可能仍有提升空间。
- **理论假设**：Bayes 规则建立在条件独立假设（$Y_i \perp Y_j \mid X$）之上，该假设在实际图像中可能不完全成立。
- **近似误差**：当前景体积极小（$d$ 很小或目标极小）时，RMA 的近似误差可能增大，但文中指出对于 30×30 的小目标误差仍 <0.1%，影响有限。
- **计算资源披露不全**：未报告训练总时长及所需 GPU 规模。

（完）
