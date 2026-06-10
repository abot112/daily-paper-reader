<div class="dpr-home-notice-card">
  <h3 class="dpr-home-notice-title">🚀 Start Here</h3>
  <ul class="dpr-home-notice-list">
    <li><a href="#/tutorial/README">使用教程</a></li>
  </ul>
</div>

## 每次日报
- 最新运行日期：2026-05-12 ~ 2026-06-10
- 运行时间：2026-06-10 04:49:36 UTC
- 运行状态：成功
- 本次总论文数：16
- 精读区：6
- 速读区：10

### 今日简报（AI）
本期精选16篇医学影像论文，重点解读6篇，其中Multi-planar 2D-U-Net利用空间出现图高效分割腹部器官，Anatomy-Guided 3D Graph网络在肿瘤肝脏精准分割Couinaud分段上表现突出。  
最值得关注的是将解剖先验（空间出现图、Couinaud分段）融入网络设计，以及Mamba、频域自适应等新架构在3D分割上的高效探索。  
读者可优先从这两篇精读入手，在自身任务中尝试引入位置或解剖约束，并对比最新轻量级骨干（如BiSegMamba、SwInception）的实际加速与精度。
- 详情：[/20260512-20260610/README](/20260512-20260610/README)

### 精读区论文标签
1. [Multi-planar 2D-U-Net Segmentation of 3D-CT Abdominal Organs augmented by Spatial Occurrence Maps](/20260512-20260610/2606.07717v1-multi-planar-2d-u-net-segmentation-of-3d-ct-abdominal-organs-augmented-by-spatial-occurrence-maps)  
   标签：评分：10.0/10、query:abdk-seg
   evidence：全监督多器官分割，针对3D CT中五个腹部器官，采用多平面2D U-Net和空间出现图。
2. [Anatomy-Guided 3D Graph Networks for Couinaud Segmentation in Tumor Affected Livers](/20260512-20260610/biorxiv-10-64898-2026-05-11-724316-v1-anatomy-guided-3d-graph-networks-for-couinaud-segmentation-in-tumor-affected-livers)  
   标签：评分：9.0/10、query:abdk-seg
   evidence：使用全监督三维UNet和图卷积网络进行肝脏Couinaud分割，直接腹部器官分割
3. [Deep Image Segmentation via Discriminant Feature Learning](/20260512-20260610/2605.14609v1-deep-image-segmentation-via-discriminant-feature-learning)  
   标签：评分：8.0/10、query:abdk-seg
   evidence：提出一种可微的、架构无关的损失函数，用于监督分割训练，以提升边界清晰度。
4. [Vision Transformer-Conditioned UNet for Domain-Adaptive Semantic Segmentation](/20260512-20260610/2605.16393v1-vision-transformer-conditioned-unet-for-domain-adaptive-semantic-segmentation)  
   标签：评分：8.0/10、query:abdk-seg
   evidence：提出ViTC-UNet，一种ViT条件化的UNet用于领域自适应生物医学语义分割。
5. [Patch-MoE Mamba: A Patch-Ordered Mixture-of-Experts State Space Architecture for Medical Image Segmentation](/20260512-20260610/2605.17719v1-patch-moe-mamba-a-patch-ordered-mixture-of-experts-state-space-architecture-for-medical-image-segmentation)  
   标签：评分：8.0/10、query:abdk-seg
   evidence：提出补丁有序混合专家Mamba架构，用于医学图像分割，兼顾效率与精度。
6. [ConvNeXt-FD: A Fractal-Based Deep Model for Robust Biomedical Image Segmentation](/20260512-20260610/2605.22002v1-convnext-fd-a-fractal-based-deep-model-for-robust-biomedical-image-segmentation)  
   标签：评分：8.0/10、query:abdk-seg
   evidence：提出ConvNeXt-FD，一种用于生物医学图像分割的新颖深度架构，利用分形损失。

### 速读区论文标签
1. [SwInception -- Local Attention Meets Convolutions](/20260512-20260610/2605.29954v1-swinception----local-attention-meets-convolutions)  
   标签：评分：8.0/10、query:abdk-seg
   evidence：在Swin变换器中引入Inception块进行全监督医学体积分割
2. [BiSegMamba: Efficient Bidirectional Tri-Oriented Mamba for 3D Medical Image Segmentation](/20260512-20260610/2605.30972v1-bisegmamba-efficient-bidirectional-tri-oriented-mamba-for-3d-medical-image-segmentation)  
   标签：评分：8.0/10、query:abdk-seg
   evidence：基于Mamba的双向三方向扫描三维医学分割网络，全监督
3. [SpectraFlow: Unifying Structural Pretraining and Frequency Adaptation for Medical Image Segmentation](/20260512-20260610/2605.14566v1-spectraflow-unifying-structural-pretraining-and-frequency-adaptation-for-medical-image-segmentation)  
   标签：评分：7.0/10、query:abdk-seg
   evidence：提出结构感知预训练和边界导向解码，适用于低数据下的全监督医学分割。
4. [Benchmarking transferability of SSL pretraining to same and different modality segmentation tasks](/20260512-20260610/2605.18491v1-benchmarking-transferability-of-ssl-pretraining-to-same-and-different-modality-segmentation-tasks)  
   标签：评分：7.0/10、query:abdk-seg
   evidence：在腹部器官CT分割任务上进行全监督微调
5. [Disentangling Sampling from Training Budget in Class-Imbalanced CT Body Composition Segmentation](/20260512-20260610/2605.20405v1-disentangling-sampling-from-training-budget-in-class-imbalanced-ct-body-composition-segmentation)  
   标签：评分：7.0/10、query:abdk-seg
   evidence：用于CT身体成分分割的类别平衡的全监督情景采样
6. [Automated Prediction of Postoperative Pancreatic Fistula Using Preoperative Computed Tomography](/20260512-20260610/2605.31539v1-automated-prediction-of-postoperative-pancreatic-fistula-using-preoperative-computed-tomography)  
   标签：评分：7.0/10、query:abdk-seg
   evidence：腹部CT胰腺分割，全监督
7. [FEFormer: Frequency-enhanced Vision Transformer for Generic Knowledge Extraction and Adaptive Feature Fusion in Volumetric Medical Image Segmentation](/20260512-20260610/2605.11434v1-feformer-frequency-enhanced-vision-transformer-for-generic-knowledge-extraction-and-adaptive-feature-fusion-in-volumetric-medical-image-segmentation)  
   标签：评分：6.0/10、query:abdk-seg
   evidence：体积医学图像分割方法，全监督，适用于腹部CT
8. [Rad-VLSM: A Cross-Modal Framework with Semantics-Assisted Prompting for Medical Segmentation and Diagnosis](/20260512-20260610/2605.18130v1-rad-vlsm-a-cross-modal-framework-with-semantics-assisted-prompting-for-medical-segmentation-and-diagnosis)  
   标签：评分：6.0/10、query:abdk-seg
   evidence：跨模态框架，用于全监督医学病灶分割与诊断，结合视觉-语言对齐和SAM。
9. [GIBLy: Improving 3D Semantic Segmentation through an Architecture-Agnostic Lightweight Geometric Inductive Bias Layer](/20260512-20260610/2605.24243v1-gibly-improving-3d-semantic-segmentation-through-an-architecture-agnostic-lightweight-geometric-inductive-bias-layer)  
   标签：评分：6.0/10、query:abdk-seg
   evidence：提出轻量几何归纳偏置层，可集成到3D分割架构中，潜在提升腹部CT分割。
10. [Implicit Fuzzification via Bounded Noise Injection for Robust Medical Image Segmentation](/20260512-20260610/2606.04427v1-implicit-fuzzification-via-bounded-noise-injection-for-robust-medical-image-segmentation)  
   标签：评分：6.0/10、query:abdk-seg
   evidence：通过U-Net跳跃连接注入噪声实现鲁棒医学图像分割


<div class="dpr-home-promo-card">
  <h3 class="dpr-home-promo-title">💬 社区与支持</h3>
  <ul class="dpr-home-promo-list">
    <li>欢迎 Star / Fork / Issue / PR</li>
    <li>QQ群：583867967（欢迎交流，已有：1151人）</li>
  </ul>
</div>
