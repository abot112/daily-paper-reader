---
title: "BLO-SAM: Bi-level Optimization Based Finetuning of the Segment Anything Model for Overfitting-Preventing Semantic Segmentation"
title_zh: BLO-SAM：基于双层优化的分割一切模型微调用于防止过拟合的语义分割
authors: "Li Zhang, Youwei Liang, Ruiyi Zhang, Amirhosein Javadi, Pengtao Xie"
date: 2024-05-02
pdf: "https://openreview.net/pdf?id=qRtM5EqE9l"
tags: ["query:abdk-seg"]
score: 6.0
evidence: 双层优化微调SAM用于全监督医学图像分割
tldr: 针对SAM在医学图像等下游分割任务中易过拟合且依赖提示的局限，提出BLO-SAM双层优化微调方法，通过分离模型训练与超参数学习来平衡拟合与泛化，在通用和医学图像分割数据集上均超越现有微调策略，为全监督腹部器官分割提供了稳定高效的解决方案。
source: ICML-2024-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2024-qrtm5eqe9l/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1755, \"height\": 370, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qrtm5eqe9l/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 860, \"height\": 348, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qrtm5eqe9l/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 756, \"height\": 538, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qrtm5eqe9l/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 862, \"height\": 296, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qrtm5eqe9l/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 848, \"height\": 441, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qrtm5eqe9l/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 759, \"height\": 443, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qrtm5eqe9l/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1780, \"height\": 584, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qrtm5eqe9l/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 787, \"height\": 461, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qrtm5eqe9l/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 736, \"height\": 442, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qrtm5eqe9l/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 786, \"height\": 439, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qrtm5eqe9l/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 737, \"height\": 451, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qrtm5eqe9l/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1598, \"height\": 536, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qrtm5eqe9l/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1596, \"height\": 537, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qrtm5eqe9l/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1594, \"height\": 536, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qrtm5eqe9l/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1598, \"height\": 540, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2024-qrtm5eqe9l/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1602, \"height\": 535, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 856, \"height\": 280, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1749, \"height\": 537, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1697, \"height\": 533, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1782, \"height\": 487, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 883, \"height\": 235, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 769, \"height\": 305, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 843, \"height\": 171, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 738, \"height\": 304, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 862, \"height\": 107, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1706, \"height\": 167, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 882, \"height\": 302, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1317, \"height\": 955, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 1740, \"height\": 531, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1558, \"height\": 491, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 999, \"height\": 167, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 864, \"height\": 172, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 1444, \"height\": 212, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2024-qrtm5eqe9l/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 900, \"height\": 169, \"label\": \"Table\"}]"
motivation: 医学图像分割等下游任务中，SAM微调易过拟合且依赖提示输入，限制其全自动应用。
method: 提出双层优化框架，将分割模型训练与超参数学习解耦，自动平衡拟合与泛化能力。
result: 在自然和医学图像分割数据集上，BLO-SAM优于传统微调和提示工程方法，有效防止过拟合。
conclusion: BLO-SAM为医学图像分割提供了鲁棒微调方案，可广泛应用于腹部等多器官全监督分割任务。
---

## Abstract
The Segment Anything Model (SAM), a foundation model pretrained on millions of images and segmentation masks, has significantly advanced semantic segmentation, a fundamental task in computer vision. Despite its strengths, SAM encounters two major challenges. Firstly, it struggles with segmenting specific objects autonomously, as it relies on users to manually input prompts like points or bounding boxes to identify targeted objects. Secondly, SAM faces challenges in excelling at specific downstream tasks, like medical imaging, due to a disparity between the distribution of its pretraining data, which predominantly consists of general-domain images, and the data used in downstream tasks. Current solutions to these problems, which involve finetuning SAM, often lead to overfitting, a notable issue in scenarios with very limited data, like in medical imaging. To overcome these limitations, we introduce BLO-SAM, which finetunes SAM based on bi-level optimization (BLO). Our approach allows for automatic image segmentation without the need for manual prompts, by optimizing a learnable prompt embedding. Furthermore, it significantly reduces the risk of overfitting by training the model's weight parameters and the prompt embedding on two separate subsets of the training dataset, each at a different level of optimization. We apply BLO-SAM to diverse semantic segmentation tasks in general and medical domains. The results demonstrate BLO-SAM's superior performance over various state-of-the-art image semantic segmentation methods. The code of BLO-SAM is available at https://github.com/importZL/BLO-SAM.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **研究背景**：Segment Anything Model（SAM）作为视觉基础模型，在语义分割上表现强大，但存在两大局限：
  - **依赖手动提示**：需要用户提供点、框等提示才能指定分割目标，无法实现全自动分割。
  - **下游任务适配困难**：通用预训练数据与医学影像等下游数据分布存在差异，直接应用效果不佳；在小样本微调时极易发生过拟合。
- **核心问题**：如何在极少训练样本下，对 SAM 进行高效微调，使其既能自动完成语义分割（无需提示），又能有效防止过拟合，提升在通用和医学领域的泛化能力。

### 2. 论文提出的方法论
- **整体思路**：提出 **BLO‑SAM**，一种基于双层优化（Bi‑Level Optimization, BLO）的 SAM 微调框架。
- **关键技术细节**：
  - **可学习提示嵌入**：将手动提示替换为一个可训练的向量，消除对人工输入的依赖，实现全自动分割。
  - **参数分组与双层优化**：
    - 将有限训练集随机等分为两个子集 `D1` 和 `D2`。
    - **下层优化**：在 `D1` 上，固定提示嵌入 `A`，用组合损失（交叉熵 + Dice，加权参数 λ=0.8）训练模型权重 `W`（包括 LoRA 层、转置卷积、MLP 头），得到 `W*(A)`。
    - **上层优化**：在 `D2` 上，用同样的组合损失验证 `W*(A)`，并反向更新提示嵌入 `A`，将提示嵌入作为“超参数”来学习。
  - **参数高效微调**：仅微调 SAM 掩码解码器中自注意力、图像-提示交叉注意力等模块的查询和值投影层的 LoRA 低秩矩阵，其余参数冻结。
  - **优化算法**：采用一阶近似（也可用二阶）求解 BLO，近似公式为：  
    `W^{(t+1)} = W^{(t)} - η1 × ∇_W L(W^{(t)}, A^{(t)}; D1)`  
    `A^{(t+1)} = A^{(t)} - η2 × ∇_A L(W^{(t+1)}, A^{(t)}; D2)`  
    迭代至收敛，从而避免在单一数据集上联合优化全部参数导致的过拟合。

### 3. 实验设计
- **数据集**：
  - **通用领域**：人脸部件分割（CelebAMask‑HQ）、汽车部件分割（Car Segmentation Dataset）、人体分割（TikTok Dances）。
  - **医学领域**：牙齿分割（儿童全景牙科影像）、胃肠道疾病分割（Kvasir‑SEG）、肺部分割（JSRT）。
  - 额外补充了皮肤病变（ISIC2018）和腹部多器官（Synapse）数据集。
- **实验设置**：
  - 主打**极低数据量场景**（训练样本 ≤ 10 张），将原始训练集二次抽样为小样本训练集，并重复 3 次随机采样取均值和标准差。
  - 每个多类分割任务被分解为多个二值分割子任务。
- **对比基线**：
  - 全监督方法：DeepLabV3、SwinUnet、U‑Net。
  - 小样本方法：HSNet、SSP。
  - SAM 相关方法：原始 SAM（需提示）、Med‑SA（需提示）、SAMed（可学习提示但单阶段微调）、LISA、Auto‑SAM。
- **评估指标**：Dice 分数。

### 4. 资源与算力
- **GPU 配置**：所有实验在单块 **NVIDIA A100 80GB** GPU 上完成。
- **训练耗时**：以牙齿分割任务（4 个训练样本）为例，BLO‑SAM 训练总时长约 **0.57 GPU 小时**，推理时间 10.4 秒，与 SAMed（0.46 小时）接近，远低于 Med‑SA 的 0.62 小时，且推理速度优于需要提示输入的 Med‑SA。

### 5. 实验数量与充分性
- **主实验数量**：
  - 6 组跨数据集/任务对比（各含 2–3 种少样本设置），共计约 15 项主性能评测。
  - 包括通用和医学场景，测试样本数量不一（如 CelebAMask‑HQ 2000 张，JSRT 147 张）。
- **消融与分析实验**：
  - 可训练组件消融（4 种配置）
  - 提示嵌入优化方式（同一数据集 vs. 分离数据集，一阶 vs. 二阶）
  - 端到端对比两阶段分离训练
  - 训练子集划分比例（1:1 vs. 3:1）
  - 仅更新 LoRA 层（不学习提示）
  - 损失权重 λ 敏感性、LoRA 秩的选择
  - 全参数微调（FT‑SAM）对比
  - 跨域泛化测试（训练集与测试集来自不同数据中心或任务）
  - 增加训练样本量（128、512）的趋势实验
  - 与 LISA、Auto‑SAM、U‑Net 等额外对比
- **公平性评价**：所有方法在严格相同的小样本划分和评估协议下进行，报告均值和标准差；BLO‑SAM 未利用任何测试集信息，对比有效且公平。实验覆盖全面，结果详实。

### 6. 论文的主要结论与发现
- BLO‑SAM 在极少样本（甚至 2～4 张）下能够显著提升 SAM 的分割质量，且全程无需人工提示。
- 通过双层优化将模型参数和提示嵌入在不同数据子集上解耦训练，有效克服了现有 SAM 微调方法（如 SAMed、Med‑SA）的严重过拟合问题。
- 在通用物体和医学影像分割上均以明显优势超越有监督、小样本以及其它 SAM 微调基线。
- 消融研究表明：掩码解码器是微调最关键模块；分离数据集学习提示嵌入是防止过拟合的核心机制；二阶梯度近似可进一步提升性能但计算代价更高。
- 该方法参数效率高，训练和推理成本与其它 SAM 微调方案相当。

### 7. 优点（亮点）
- **创新性强**：率先将双层优化引入 SAM 微调，将提示嵌入视为“超参数”进行分离学习，从机理上缓解小样本过拟合。
- **全自动分割**：无需任何手工提示，更贴合医学等实际应用场景。
- **性能稳健**：在超低数据量下效果突出，且对随机种子和数据划分不敏感，方法稳定。
- **实验设计扎实**：涵盖通用和医学两大类六个数据集，丰富的消融与跨域实验，全面验证了方法的有效性和泛化性。
- **开源可复现**：提供代码，便于后续研究。

### 8. 不足与局限
- **数据划分依赖**：当训练样本极少（如只有 2 张）时，进一步划分 D1/D2 可能导致每个子集仅含 1 个样本，模型训练可能不稳定。
- **计算开销**：双层优化需要先后在 D1 和 D2 上执行前向/反向传播，比单阶段微调稍慢（但仍可接受），二阶梯度方法耗时更多。
- **未探讨更大规模数据**：实验主要集中于 ≤10 样本的极端少样本场景，对于中等规模（几百张）的训练数据下是否仍优于其它微调方法，缺乏展示。
- **医学任务代表性**：医学实验仅覆盖牙齿、息肉、肺结节等，对腹部多器官分割虽有附录中的 Synapse 实验，但主文呈现不够突出，且未与专门设计的医学分割模型（如 nnU‑Net）对比。
- **提示嵌入的偏差风险**：学习到的“虚拟提示”完全基于训练子集，可能编码了训练数据特有的分布偏差，在真实临床异质分布中的鲁棒性需进一步验证。

（完）
