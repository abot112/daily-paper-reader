---
title: "MAE-UNETR++: Masked Autoencoder Pretraining for 3-D Lung Nodule Segmentation"
title_zh: MAE-UNETR++：面向三维肺结节分割的掩码自编码器预训练
authors: "Savant, V., Wang, Y., Xuan, J."
date: 2026-06-19
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.17.733000v1.full.pdf"
tags: ["query:abdk-seg"]
score: 7.0
evidence: 采用MAE预训练提升全监督3D肺结节分割的数据效率
tldr: 针对肺结节三维分割中标注数据稀缺、传统迁移学习因域差异受限的问题，提出基于掩码自编码器（MAE）的域内自监督预训练方法。在目标域CT数据上预训练后微调，UNETR++的DSC从随机初始化的0.136和Decathlon迁移的0.257提升至0.307。同时，该方法将V-Net在低数据场景的DSC从0.010提升至0.071，展现了鲁棒的初始化优势。
source: biorxiv
selection_source: fresh_fetch
motivation: 标注三维医学体素数据成本高，公开预训练权重的域差异常导致肺结节分割性能不佳，亟需域内自监督预训练破局。
method: 采用掩码自编码器（MAE）在目标域CT上进行自监督预训练，后微调UNETR++和V-Net进行结节分割。
result: MAE预训练后UNETR++ DSC达0.307，优于随机初始化（0.136）和Decathlon迁移权重（0.257）；V-Net在低数据时DSC从0.010升至0.071。
conclusion: MAE域内预训练能有效打破域差异造成的低效数据壁垒，为标注稀缺的三维分割任务提供实用稳健的初始化策略。
---

## 摘要
体积医学成像的体素级标注成本高昂且难以扩展，这使得在实践中训练高容量三维分割模型面临挑战。从大型公共数据集进行迁移学习是一种常见的补救方法，但当源域与目标解剖结构和采集特性不同时（如肺结节中常见的情况），其性能可能不佳。在本工作中，我们提出了一种基于掩码自编码器（MAE）预训练的方法，以打破领域差异造成的数据效率壁垒，并针对三维肺结节分割的领域特定自监督学习进行了深入的实证研究。我们评估了两种实验设置：第一，在代表性基线上比较掩码自编码器（MAE）预训练与随机初始化；第二，针对 UNETR++ 比较 MAE 与十项全能迁移学习，同时测试基于 MAE 的预训练是否也有益于 CNN 基线模型（V-Net）。在目标域 CT 体积上进行 MAE 预训练获得了 0.307 的 Dice 相似系数，优于随机初始化（0.136）和十项全能权重（0.257）。此外，MAE 提升了 V-Net 在“低数据”场景（即标注数据不足）下的稳定性，将 DSC 从 0.010 提升至 0.071。总体而言，这些结果表明，在标注数据有限的情况下，基于 MAE 的预训练可以为体积分割提供一种实用且稳健的初始化策略。

## Abstract
Voxel-level annotation for volumetric medical imaging is expensive and difficult to scale, which makes training highcapacity 3-D segmentation models challenging in practice. Transfer learning (TL) from large public datasets is a common remedy, but it can under-perform when the source domain differs from the target anatomy and acquisition characteristics, as is often the case for pulmonary nodules. In this work, we propose a masked autoencoder (MAE) pretraining-based approach to break the data efficiency wall of domain difference and present a focused empirical study of domain-specific self-supervised learning (SSL) for 3-D lung nodule segmentation. We evaluate two experimental settings: first, Masked Autoencoder (MAE) pretraining versus random initialization across representative baselines; second, MAE versus Decathlon TL for UNETR++ while testing whether MAE-based pretraining also benefits a CNN baseline (V-Net). MAE pretraining on target-domain CT volumes achieves a Dice Similarity Coefficient (DSC) of 0.307, outperforming random initialization (0.136) and Decathlon weights (0.257). In addition, MAE improves the stability of V-Net in a "low-data" regime (i.e., with "insufficiently labeled" data), increasing DSC from 0.010 to0.071. Overall, these results suggest that MAE-based pretraining can provide a practical and robust initialization strategy for volumetric segmentation when labeled data are limited.