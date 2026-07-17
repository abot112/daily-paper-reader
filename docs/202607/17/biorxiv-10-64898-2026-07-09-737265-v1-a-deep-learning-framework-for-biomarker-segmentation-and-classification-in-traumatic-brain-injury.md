---
title: A Deep Learning Framework for Biomarker Segmentation and Classification in Traumatic Brain Injury
title_zh: 创伤性脑损伤中生物标志物分割与分类的深度学习框架
authors: "Dash, R., Mayilsamy, K., Green, R., Sun, Y., Mohapatra, S."
date: 2026-07-15
pdf: "https://www.biorxiv.org/content/10.64898/2026.07.09.737265v1.full.pdf"
tags: ["query:abdk-seg"]
score: 8.0
evidence: 提出脑外伤中双生物标志物分割的深度学习框架。
tldr: 创伤性脑损伤(TBI)后标志物GFAP和IBA1广泛激活，传统手动分析耗时费力。本研究提出自动化深度学习框架，利用U-Net变体分割双标志物，并结合ResNet50、Swin-T、MaxViT分类。多模态融合GFAP与IBA1显著提升分类性能，Swin-T准确率达0.9489。该框架为免疫荧光脑损伤图像分析提供可扩展自动化方案，加速研究。
source: biorxiv
selection_source: fresh_fetch
figures_json: "[{\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737265-v1/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1304, \"height\": 899, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737265-v1/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1615, \"height\": 497, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737265-v1/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1261, \"height\": 758, \"label\": \"Figure\"}, {\"url\": \"assets/figures/biorxiv/biorxiv-10-64898-2026-07-09-737265-v1/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1353, \"height\": 825, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-09-737265-v1/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1287, \"height\": 506, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-09-737265-v1/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1713, \"height\": 367, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-09-737265-v1/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1713, \"height\": 630, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-09-737265-v1/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1714, \"height\": 632, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-09-737265-v1/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1714, \"height\": 503, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-09-737265-v1/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1715, \"height\": 504, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-09-737265-v1/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1713, \"height\": 504, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-09-737265-v1/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1712, \"height\": 504, \"label\": \"Table\"}, {\"url\": \"assets/tables/biorxiv/biorxiv-10-64898-2026-07-09-737265-v1/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1713, \"height\": 538, \"label\": \"Table\"}]"
motivation: 传统手动分析TBI免疫荧光图像中的GFAP和IBA1标志物耗时费力，亟需自动化方法。
method: 提出基于U-Net变体的分割网络和视觉Transformer分类模型，融合GFAP与IBA1多模态特征。
result: U-Net分割GFAP Dice达0.9259，U-Net++分割IBA1 Dice达0.9676；多模态融合分类Swin-T准确率最高0.9489。
conclusion: 融合互补生物标志物增强TBI分类，深度学习为免疫荧光分析提供可扩展自动化方案。
---

## 摘要
创伤性脑损伤（TBI）触发广泛的生物标志物激活，包括星形细胞标志物如胶质纤维酸性蛋白（GFAP）和小胶质细胞标志物如离子钙结合衔接分子1（IBA1）。量化并分析这些生物标志物对于理解损伤影响至关重要；然而，当前方法劳动密集且耗时。在本研究中，我们提出了一种自动化的深度学习框架，用于使用GFAP和IBA1免疫荧光图像进行双生物标志物分割和TBI分类。训练了四种U-Net变体：基线U-Net、嵌套U-Net（U-Net++）、注意力U-Net（MANet）和残差U-Net（LinkNet）进行分割。在单生物标志物和双生物标志物条件下，训练了三种分类模型ResNet50、Swin-T和MaxViT来区分TBI和对照图像。基线U-Net在GFAP上实现了最高的分割Dice分数（0.9259），而U-Net++在IBA1上实现了最高的Dice分数（0.9676）。与QuPath方法相比，训练的分割模型表现出显著更优的性能。虽然单独使用GFAP即可支持高分类准确率，但单独使用IBA1效果较差。GFAP和IBA1的多模态融合显著提高了所有模型的分类性能，其中Swin_T实现了最高的总体准确率（0.9489），ResNet50实现了最高的F1分数（0.9499）。这些发现表明，整合互补生物标志物可增强自动化TBI分类，深度学习为免疫荧光脑损伤图像的手动分析提供了稳健的替代方案。该框架可扩展至其他生物标志物和损伤模型，提供了一种可重复的方法来加速生物标志物研究。

## Abstract
Traumatic brain injury (TBI) triggers widespread biomarker activation, including astrocytic markers such as glial fibrillary acidic protein (GFAP) and microglia markers such as ionized calcium-binding adapter molecule 1 (IBA1). Quantifying and analyzing these biomarkers are critical for understanding injury impact; however, current methods are labor-intensive and time-consuming. In this study, we propose an automated deep learning framework for dual-biomarker segmentation and TBI classification using GFAP and IBA1 immunofluorescent images. Four U-Net variants: Baseline U-Net, Nested U-Net (U-Net++), Attention U-Net (MANet), and Residual U-Net (LinkNet) were trained for segmentation. Three classification models, ResNet50, Swin-T, and MaxViT, were trained to distinguish TBI from control images under single- and dual-biomarker conditions. The baseline U-Net achieved the highest segmentation Dice score for GFAP (0.9259), while the U-Net++ achieved the highest Dice score for IBA1 (0.9676). Trained segmentation models demonstrated significantly better performance compared to QuPath alternatives. While GFAP alone supported high classification accuracy, IBA1 alone was less effective. Multimodal fusion of GFAP and IBA1 significantly improved classification performance across all models, with Swin_T achieving the highest overall accuracy (0.9489), and ResNet50 achieving the highest F1-score (0.9499). These findings demonstrate that integrating complementary biomarkers enhances automated TBI classification, and deep learning offers a robust alternative to manual analysis for immunofluorescent brain injury imaging. This framework is scalable to additional biomarkers and injury models, offering a reproducible approach to accelerate biomarker research.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义

- **研究动机：**
  - 创伤性脑损伤（TBI）是全球致残主因之一，每年影响超5000万人，造成巨大社会经济负担。
  - TBI后小胶质细胞（IBA1标志物）和星形胶质细胞（GFAP标志物）的激活是神经炎症的关键指标，但其免疫荧光图像分析目前主要依赖手动或半自动方法，劳动密集、效率低、可重复性差。
- **核心问题：**
  - 能否建立自动化、可复现的深度学习框架，同时完成GFAP与IBA1的双标志物分割（segmentation）和TBI状态分类？
  - 多模态融合（同时使用两种标志物）是否比单标志物分类更准确？
- **整体意义：**
  - 提供一种可扩展、自动化的组织学图像分析方案，减少人工操作，加速生物标志物研究，并验证多标志物整合的优势。

### 2. 论文提出的方法论

- **整体流程：**
  - 采集小鼠脑组织免疫荧光图像（GFAP、IBA1）→ 预处理（灰度化、自动阈值二值化、人工验证掩码）→ 图像分块（512×512，50%重叠）→ 分割模型训练 → 分类模型训练，最终评估。
- **分割阶段（U-Net变体）：**
  - 使用四种编码器均为ResNet18的U-Net架构：基线U-Net、U‑Net++（嵌套密集跳跃连接）、MANet（多尺度注意力机制）、LinkNet（轻量级残差连接）。
  - 损失函数：二元交叉熵与Dice损失的等权组合（公式1）。
  - 训练设置：5折交叉验证（同只动物图像仅存于同一折，防泄漏），每折训练50个epoch，Adam优化器（lr=1e-4），batch size 64，自动混合精度。
  - 数据增强：仅应用水平/垂直翻转和90°倍数的随机旋转。
- **分类阶段（三种骨干网络）：**
  - 模型：ResNet50（CNN）、Swin‑T（视觉Transformer）、MaxViT（CNN‑Transformer混合），均使用ImageNet预训练权重，输出层改为2类。
  - 单/双通道输入：GFAP单独、IBA1单独、GFAP+IBA1拼接（6通道输入）。
  - 训练设置：利用分割后重建的完整免疫荧光图像（非掩码），尺寸调整为224×224，5折交叉验证重复两次（不同随机种子），每折训练60个epoch，AdamW优化器（lr=1e-4, weight decay=1e-4），早停耐心15个epoch，batch size 32。
  - 损失函数：交叉熵损失（公式2）。数据增强同上。
- **对比基准：** 分割阶段与QuPath内置的ANN、随机森林、逻辑回归像素分类器比较。

### 3. 实验设计

- **数据集：**
  - 来源：雄性C57BL/6小鼠，重复闭合性TBI模型，死后7天取脑，冠状切片免疫荧光染色。
  - 图像：GFAP（对照99, TBI 75）、IBA1（对照276, TBI 383）、成对GFAP‑IBA1（对照49对, TBI 50对，每对来自同一视野）。每张原始图像1360×1024像素。
- **分割benchmark：**
  - 评价指标：Dice、IoU、精度、召回率，在测试折上计算。
  - 对比方法：QuPath中的ANN、RF、LR像素分类器。
- **分类benchmark：**
  - 评价指标：准确率、灵敏度（TPR）、特异度（TNR）、F1分数、AUC‑ROC。
  - 对比方案：单标志物（仅GFAP、仅IBA1） vs. 双标志物（GFAP+IBA1），三种模型在各自配置下比较。
- **实验场景覆盖：**
  - 两种标志物 × 四种U‑Net = 8组分割对比，另加3种QuPath方法作为分割对照。
  - 三种输入模式 × 三种分类模型 = 9组分类对比。

### 4. 资源与算力

- 论文中未明确提及所用GPU型号、数量和具体训练时长。
- 部分训练细节可推断：启用自动混合精度，batch size达64（分割）和32（分类），训练50～60个epoch并使用早停，重复10个fold（5折×2次），但算力消耗规模未知，无法评估实际硬件需求。

### 5. 实验数量与充分性

- **实验总量：**
  - 分割：4种U‑Net × 2标志物 × 5折交叉验证 × 1次测试 = 40个模型训练及测试。
  - QuPath分割：3种方法 × 2标志物 × 5折交叉验证 × 2次 = 60个模型训练及测试。
  - 分类：3种模型 × 3种输入条件 × 5折交叉验证 × 2次重复 = 90个模型训练及测试。
  - 总共约190个训练‑测试循环，覆盖了多种架构和对比条件。
- **充分性与公平性：**
  - 采用严格的K‑折交叉验证（按动物分组防泄漏），重复两次以评估稳定性，客观性强。
  - 对比了传统方法（QuPath）和不同深浅/架构的分割模型，以及CNN、ViT、混合模型在分类上的表现。
  - 数据量在分类任务上相对较小（GFAP仅174张，成对仅99张），但鉴于组织学图像的获取成本，已有一定代表性。
  - 消融实验涵盖单通道 vs. 双通道，清楚地验证了多模态优势，实验设计合理。

### 6. 论文的主要结论与发现

- **分割性能：**
  - GFAP分割中，基线U‑Net Dice最高（0.9259），U‑Net++精度稍高但整体略低，LinkNet最差。
  - IBA1分割中，U‑Net++最佳（Dice 0.9676），且所有U‑Net模型均显著优于QuPath的传统像素分类器，预测速度也更快。
- **单生物标志物分类：**
  - GFAP单独分类表现强劲：ResNet50准确率0.9456，Swin‑T F1分数0.9357。
  - IBA1单独分类困难：MaxViT准确率最高仅0.8118，暗示IBA1染色模式更微弱、变异性更大。
- **双生物标志物分类：**
  - GFAP+IBA1多模态融合显著提升性能：Swin‑T准确率0.9489（最高），ResNet50 F1‑score 0.9499（最高），所有模型均优于单独IBA1，且大部分指标优于单独GFAP。
  - 融合后灵敏度大幅提高（如ResNet50从IBA1单通道的0.7582升至0.9600），表明星形胶质细胞信息有效减少了小胶质细胞分类的假阳性。
- **总体结论：** 深度学习可自动化TBI组织学的标志物分割与分类，多生物标志物融合显著提升鲁棒性，该框架可扩展至其他标志物和神经疾病模型。

### 7. 优点

- **创新的双标志物融合框架：** 首次系统评估了GFAP和IBA1双通道融合对TBI组织学分类的提升作用。
- **全面的模型比较：** 分割阶段涵盖了不同复杂度的U‑Net变体，分类阶段对比了CNN、ViT及混合架构，多维度验证稳健性。
- **严格的实验设计：** 采用按动物分组的K‑折交叉验证，避免数据泄露；训练细节清晰（损失函数、增强策略、早停等），可复现性高。
- **对比传统方法：** 与QuPath内置工具直接比较，突出深度学习的性能与速度优势。
- **临床意义突出：** 针对免疫荧光组织学分析耗时费力的痛点，提供端到端自动化方案，有望加速TBI生物标志物研究。

### 8. 不足与局限

- **数据集规模与多样性有限：**
  - 实验仅使用单一性别（雄性）小鼠，且均为同一时间点（7天）的单一TBI模型，跨性别、跨时间、跨损伤模型的外推性未知。
  - 图像数量较少，尤其成对图像仅99对，可能限制模型泛化能力。
- **预处理依赖人工：** 二值掩码的阈值平均及人工验证仍引入主观性，未完全免除人工介入。
- **分类输入使用原始荧光图像而非分割掩码，但分割模型未直接用于分类环节，未能形成端到端全自动 pipeline。**
- **算力信息缺失：** 未报告GPU资源和训练耗时，难以评估其实际落地效率。
- **未与其他近期相关方法直接比较：** 虽然引用了先前分割GFAP或IBA1的研究，但未在相同数据集上复现并对比它们的性能。
- **仅覆盖两个标志物：** 未尝试融入其他神经炎性标志物或形态学特征，多模态的扩展潜力仅停留在概念层面。

（完）
