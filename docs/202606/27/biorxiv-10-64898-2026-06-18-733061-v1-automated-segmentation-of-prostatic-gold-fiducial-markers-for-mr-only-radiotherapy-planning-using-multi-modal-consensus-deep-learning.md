---
title: Automated Segmentation of Prostatic Gold Fiducial Markers for MR-Only Radiotherapy Planning Using Multi-Modal Consensus Deep Learning
title_zh: 使用多模型共识深度学习进行前列腺金标标记物的自动分割用于仅MR放射治疗计划
authors: "Stewart, A. W., Goodwin, J., Richardson, M., Robinson, S. D., O'Brien, K., Jin, J., Barth, M."
date: 2026-06-23
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.18.733061v1.full.pdf"
tags: ["query:abdk-seg"]
score: 9.0
evidence: 全监督的3D U-Net集成深度学习模型用于医学图像分割
tldr: "前列腺癌MR-only放疗需精准定位植入金质基准标记（FM），但自动分割可靠性不足。本研究提出多模型共识深度学习方法，基于3D U-Net集成并平均概率图生成稳定预测。在25例测试中，四模型共识取得96%敏感度、95%精确度，85%患者标记完全检出，远优于单一模型84%敏感度。该方法仅依赖常规T1 MRI，已在扫描仪和浏览器端部署，有望简化放疗流程，提升自动化水平。"
source: biorxiv
selection_source: fresh_fetch
motivation: 在前列腺癌MR-only放疗中，金质基准标记（FM）的可靠自动分割对精准定位至关重要，但单一模型常不够稳定。
method: 采用3D U-Net集成四个随机种子模型，通过对标记类概率图取平均并选取前三连通成分，实现FM自动分割。
result: "四模型共识在25例测试中实现96%敏感度、95%精确度，85%患者获完美标记检测，优于单一模型84%敏感度。"
conclusion: 多模型共识深度学习显著提升FM分割可靠性，仅需常规T1 MRI，有望推动MR-only放疗规划落地。
---

## 摘要
目的：开发并评估一种多模型共识深度学习方法，用于在T1加权前列腺MRI中自动分割金标标记物（FM）。

材料与方法：在这项回顾性研究中，收集了127名前列腺癌患者（均为男性；平均年龄70岁±7[标准差]；年龄范围50–88岁；收集时间为2020年10月至2026年1月）的T1加权MRI和CT衍生的参考标准分割，每名患者均植入了三个金标FM。使用四个随机种子在93名受试者上训练了一个3D U-Net，以产生一个集成模型。在推理时，跨模型平均标记物类别概率图，并选择前三个连通分量。在34名时间上保留的受试者（9名用于调优，25名用于测试）上，使用标记物级别的敏感性和精确度以及精确的（Clopper-Pearson）95%置信区间（CIs）评估性能。进行了模型数量消融研究。该流程通过OpenRecon框架部署在西门子MRI系统上进行扫描仪端处理，并作为基于浏览器的应用程序使用WebAssembly，完全在客户端执行。

结果：在25名测试受试者上，四模型共识达到了96%（73个中的70个）的敏感性和95%（74个中的70个）的精确度，34名中的29名（85%）受试者实现了完美的标记物检测。单一模型的平均敏感性为84%（标准差9%），使用四模型共识提高到了96%（标准差<1%）。

结论：与单一模型相比，多模型共识深度学习显著提高了FM分割的可靠性，仅使用常规采集的T1加权MRI就实现了高敏感性和高精确度。

## Abstract
PurposeTo develop and evaluate a multi-model consensus deep learning approach for automated gold fiducial marker (FM) segmentation in T1-weighted prostate MRI.

Materials and MethodsIn this retrospective study, T1-weighted MRI and CT-derived reference standard segmentations were collected from 127 prostate cancer patients (all male; mean age, 70 years {+/-} 7 [standard deviation]; age range, 50-88 years; collected between October 2020 and January 2026) who each had three implanted gold FMs. A 3D U-Net was trained on 93 subjects using four random seeds to produce an ensemble. At inference, marker-class probability maps were averaged across models and the top three connected components selected. Performance was evaluated on 34 temporally held-out subjects (9 tuning, 25 test) using marker-level sensitivity and precision with exact (Clopper-Pearson) 95% confidence intervals (CIs). A model count ablation study was performed. The pipeline was deployed for on-scanner processing on Siemens MRI systems via the OpenRecon framework and as a browser-based application using WebAssembly, executing entirely client-side.

ResultsThe four-model consensus achieved 96% (70 of 73) sensitivity and 95% (70 of 74) precision on 25 test subjects, with 29 of 34 (85%) subjects achieving perfect marker detection. Single models had a mean sensitivity of 84% (SD, 9%), improving to 96% with four-model consensus (SD, <1%).

ConclusionMulti-model consensus deep learning substantially improved FM segmentation reliability over individual models, achieving high sensitivity and precision using only routinely acquired T1-weighted MRI.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **研究背景**：在前列腺癌仅磁共振（MR-only）放射治疗规划中，为了精准定位肿瘤靶区与周围危及器官，需要在患者前列腺内植入金质基准标记物（Fiducial Marker, FM）。临床流程必须能够自动、可靠地在治疗前MRI图像上识别并分割出这些标记物，从而取代基于CT的配准环节，实现真正的一体化MR-only工作流。
- **核心问题**：单一深度学习分割模型在这些细小、类圆形、低对比度的金标标记物检测中表现不稳定，容易出现漏检或误检，难以满足临床对近乎零失误的严苛要求。
- **整体含义**：本文提出运用**多模型共识（Multi-Model Consensus）策略**，通过集成多个同构但初始化不同的3D U-Net模型，并以平均概率图结合连通分量筛选的方式，在不依赖额外成像序列或复杂后处理的情况下，将标记物分割的敏感性与精确度提升至临床可用的高水平，从而有望简化并加速MR-only放疗流程。

### 2. 论文提出的方法论
- **核心思想**：利用多样化的模型集成来增加预测的鲁棒性，通过“群体智慧”抑制单个模型的随机性误差，并借助待测标记物总数已知（每例患者植入三颗）的先验知识，强制选择置信度最高的三个候选区域。
- **关键技术细节与流程**：
  - **基础网络**：采用3D U-Net作为主干分割网络，输入为常规T1加权前列腺MRI体积。
  - **模型集成**：使用四个不同的随机种子，在相同训练集上独立训练四个结构一致但参数初始化不同的3D U-Net模型。
  - **推理阶段共识形成**：
    1. 对每一测试病例，四个模型各自输出标记物类别的概率图。
    2. 将四幅概率图进行逐体素**平均（Averaging）**，得到一张集成概率图。
    3. 对集成概率图进行阈值化，并提取所有连通成分。
    4. 根据连通成分的累积概率大小排序，**强制选取概率最大的前三个连通成分**（与患者实际植入数量匹配）作为最终预测的FM区域。
- **算法本质**：该流程融合了“模型集成平均”（减少方差）与“结构化后处理”（引入先验约束），并未引入复杂的学习策略。

### 3. 实验设计
- **数据集**：
  - **总样本**：127名前列腺癌患者（均为男性，年龄50–88岁），每名患者植入三颗金标FM，横跨2020年10月至2026年1月。
  - **划分方式**：严格按**时间顺序**保留后34例作为独立测试集（其中9例用于调优，25例用于最终测试），前93例作为训练集。这种划分模拟了临床真实的前瞻性验证环境。
- **基准与对比方法**：
  - **单一模型基准**：将四个独立训练的单模型各自的分割表现作为主要对比基准。
  - **模型数量消融研究**：评估不同数量的集成模型（如2个、3个、4个）对最终性能的影响。
- **评估指标**：
  - **标记物级别**：敏感性（Recall）、精确度（Precision），并计算精确的Clopper-Pearson 95%置信区间。
  - **患者级别**：实现“完美标记物检测”（三颗全部检测正确且无误检）的患者比例。
- **参考标准**：以同一患者在CT图像上手动勾画或识别的标记物作为金标准。

### 4. 资源与算力
- 论文的摘要及所提供的元数据中，**未明确提及**训练所使用GPU的具体型号、数量、批大小（batch size）或单次/整体训练时长等算力相关信息。部署部分仅说明推理流程已通过OpenRecon框架在西门子MRI系统上实现扫描仪端运行，以及使用WebAssembly构建了完全在浏览器客户端执行的应用程序。

### 5. 实验数量与充分性
- **实验组数**：主要包括四项关键验证。
  1. 四个单模型的独立性能评估。
  2. 最终四模型共识在25例时序测试集上的核心结果验证。
  3. 模型集成数量（从1至4）的消融实验。
  4. 兼顾灵敏度与精确度，并报告了患者完美检出率。
- **实验充分性与公平性**：
  - **充分性较好**：样本量适中，且采用严格的时间性留出验证，能较为真实地反映方法泛化能力；评估指标从体素、标记物、患者三个层面进行，全面且有说服力；消融实验锁定了关键的超参数（集成数量为4）。
  - **公平性有保障**：所有模型均基于相同的网络骨架和训练数据，只有随机种子的区别，单一模型与集成模型的对比建立于同一算法基准上。唯一未明确的部分是集成模型推理时间的额外开销比较。

### 6. 论文的主要结论与发现
- **性能巨幅提升**：四模型共识在25例时序测试集上实现了**96%的标记物级别敏感性和95%的精确度**，远优于单一模型的平均值（敏感性84%，标准差9%）。性能的稳定性也显著提高，标准差降低至不足1%。
- **临床可用性**：**85%的患者（29/34）获得了完美的三标记全部检测**，且几乎无误检，证明该方法能大幅减少后续人工核对与修正的工作量。
- **流程简化可行**：仅依赖常规T1加权成像，无需注射对比剂或额外采集特殊序列，可无缝嵌入现有临床扫描方案。

### 7. 优点
- **稳健的共识策略**：利用模型多样性结合硬性先验（已知标记数）的方法简单而有效，极大抑制了单个模型预测中的离群噪点，直接针对“可靠性”这一临床痛点。
- **临床友好的部署形态**：已实现扫描仪在线重建流程和客户端浏览器推理两种低依赖、零数据传输压力的部署方案，为向临床转化扫清了主要工程障碍。
- **严格的时间性验证**：以时间而非随机混洗作为数据划分依据，更能经得起“真实世界”数据漂移的考验，结论可信度更高。
- **零额外采集成本**：不改变常规T1扫描协议，不影响患者流通量，硬件友好。

### 8. 不足与局限
- **单中心回顾性数据**：所有数据来自同一时段、同一机构，模型对不同MRI机型和扫描参数下的泛化能力未经外部验证，可能存在设备偏差。
- **标记物数量先验依赖**：方法假设所有患者均植入且仅植入三颗标记物，若未来标记物使用方案发生变化（如数量增减、零植入），硬性选择三个连通分量的后处理会直接失效，需要重新设计。
- **罕见情况的鲁棒性未知**：对于标记物因植入过深、伪影遮挡、或合并术后出血等情况导致MRI上完全不显影的极端案例，多模型共识也无法“无中生有”，其召回上限受限于基础图像的可见度。
- **参考标准误差**：CT衍生的分割参考标准本身可能存在配准误差或部分容积效应带来的模糊性，可能轻微低估或高估模型的真实性能。
- **算力信息缺失**：训练资源需求未阐述，难以评估该方法的复现与扩展成本。
- **标记物外形泛化**：仅针对金质标记，对其它材质（如碳基、液态基准标记）的形状和信号特征未见覆盖。

（完）
