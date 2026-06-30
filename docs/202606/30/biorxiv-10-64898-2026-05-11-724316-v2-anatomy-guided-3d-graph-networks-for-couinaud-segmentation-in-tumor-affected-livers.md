---
title: Anatomy-Guided 3D Graph Networks for Couinaud Segmentation in Tumor Affected Livers
title_zh: 基于解剖引导的三维图网络用于肿瘤受累肝脏的Couinaud分段
authors: "You, L., Dang, H., Wang, H., Matta, E., zhou, X."
date: 2026-06-29
pdf: "https://www.biorxiv.org/content/10.64898/2026.05.11.724316v2.full.pdf"
tags: ["query:abdk-seg"]
score: 7.0
evidence: 使用3D UNet和GCN进行腹部CT/MR中肝脏的全监督深度学习分割
tldr: 传统Couinaud分割在肿瘤肝脏中因结构扭曲而失效。本文提出两阶段框架，整合3D UNet与3D解剖结构引导图卷积网络，并标准化预处理肝脏体积。在未见临床数据上平均Dice达0.828，实现稳健分割。首次公开代码与权重，为提供可复现资源。
source: biorxiv
selection_source: fresh_fetch
motivation: 肝癌病例中病理结构扭曲导致传统Couinaud分割泛化差，需适应肿瘤肝脏的稳健方法。
method: 采用两阶段框架，先3D UNet提取肝脏，再3D GCN建模八段解剖关系，预处理标准化至50帧。
result: 盲测Dice系数0.828，在未见临床数据集上展现优越泛化性能。
conclusion: 提出首个公开的肿瘤肝脏Couinaud分割深度学习方案，融合解剖引导图网络显著提升鲁棒性。
---

## 摘要
摘要：基于图像的肝脏Couinaud分段旨在自动提供肝脏CT/MR图像中可疑目标的位置。一旦实现，医生将被引导至可疑结节所在的目标切片和区域。然而，传统算法主要在健康肝脏图像上训练，由于病理结构扭曲，常常无法泛化至肝细胞癌（HCC）病例。在这项工作中，我们提出了一个鲁棒的两阶段框架，将三维Unet与三维解剖结构引导的图卷积网络（3D GCN）相结合。该两阶段策略有效地分离肝脏体积，消除了邻近器官（如脾脏）的结构噪声，使框架能够专注于八个肝段之间复杂的三维解剖关系。为了确保全局空间推理所需的拓扑一致性，我们实施了一个标准化的预处理流程，将纯肝脏体积沿z轴归一化至恰好50帧。通过将轻量级三维UNet骨干与三维GCN相结合进行精细边界推理，我们的模型在未见过的临床数据集上展现了卓越的泛化性能，在盲测中达到了0.828的平均Dice分数。通过发布我们的代码和预训练权重，我们旨在为鲁棒的Couinaud分段提供首个公开可用的深度学习资源。

## Abstract
Abstract: Image-based liver Couinaud segmentation is designed to automatically provide the locations of suspicious objects in liver CT/MR images. Once achieved, the physicians will be guided to the target slice and area where the suspicious node is located. However, conventional algorithms trained primarily on healthy liver images often fail to generalize to Hepatocellular Carcinoma (HCC) cases due to pathological structural distortions. In this work, we propose a robust two-stage framework that integrates a 3D Unet with a 3D Anatomical Structure-Guided Graph Convolutional Network (3D GCN). This two-stage strategy effectively isolates the liver volume to eliminate structural noise from neighboring organs, such as the spleen, allowing the framework to focus exclusively on the complex 3D anatomical relationships among the eight segments. To ensure the topological consistency required for global spatial reasoning, we implement a standardized preprocessing pipeline that normalizes liver-only volumes to exactly 50 frames along the z-axis. By combining a lightweight 3D UNet backbone with the 3D GCN for refined boundary reasoning, our model demonstrates superior generalization performance on unseen clinical datasets, achieving a mean Dice score of 0.828 in blind testing. By releasing our code and pretrained weights, we aim to provide the first publicly available deep learning resource for robust Couinaud segmentation.