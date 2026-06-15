---
title: "Automated Segmentation of Brainstem and Subcortical White Matter: Mapping the Deep Tegmental Core with BundleParc"
title_zh: 脑干与皮层下白质的自动分割：利用BundleParc绘制深部被盖核心
authors: "Schilling, K. G., Rudravaram, G., Theberge, A., Amandola, M., Kim, M. E., Humphreys, K. L., Cutting, L., Archer, D., Hohman, T. J., Jefferson, A. L., Beason Held, L. L., Bilgel, M., Alzheimers Disease Neuroimaging Initiative,, The BIOCARD Study Team,, Chamberland, M., Descoteaux, M., Petit, L., Rheault, F., Landman, B. A."
date: 2026-06-12
pdf: "https://www.biorxiv.org/content/10.64898/2026.06.09.731210v1.full.pdf"
tags: ["query:abdk-seg"]
score: 8.0
evidence: 描述从扩散MRI自动分割脑白质通路的深度学习流水线，属于医学图像分割任务
tldr: 扩散MRI可无创描绘白质通路，但现有自动分割方法主要面向大型投射与联络束，紧凑的脑干和皮层下通路在连接组学中常被忽视。为弥补此缺口，本研究基于BundleParc架构，开发了可对97条深层通路进行直接分割和沿束分区的自动化流程。模型训练自HCP数据，采用解剖引导束路追踪与严格质控，成功重建复杂解剖轨迹，并在发育、衰老及疾病等外部数据集上保持稳健泛化。所发布的容器、模型与参考数据为研究深层脑系统在神经调控、发育及疾病中的作用提供了关键资源。
source: biorxiv
selection_source: fresh_fetch
motivation: 现有扩散MRI自动分割方法集中于大纤维束，脑干及皮层下紧凑通路常被忽略，限制了连接组分析的完整性。
method: 采用BundleParc架构，基于HCP扩散MRI与解剖引导束路追踪，对97条通路进行直接分割与沿束分区，并辅以自动过滤与手工质控。
result: 算法成功解析复杂解剖轨迹与有序分区，并在多中心发育、衰老与疾病数据上表现出稳健泛化性，克服分辨率和角度采样差异。
conclusion: 发布的容器、模型与参考数据为深入探索深层通路在神经调控、发育与疾病中的作用提供了标准化资源。
---

## 摘要
扩散磁共振成像能够无创地绘制人类白质通路，但自动分割方法主要集中于大型联合、投射和连合纤维束。然而，在基底节、小脑、边缘/奖赏、感觉和稳态功能中起支撑作用的紧凑脑干和皮层下通路，在大规模连接组学分析中仍然代表性不足。为解决这一缺口，我们将最近提出的纤维束分割架构BundleParc改造为自动化流程，用于97条皮层下和脑干白质通路的直接分割与沿束分割。模型基于人类连接组计划扩散磁共振成像数据整理出的参考数据集进行训练，该数据集使用解剖引导的纤维束追踪、明确的纳入与排除标准、自动异常值过滤以及手动质量保证构建。该算法直接作用于原生空间的纤维取向分布，成功恢复了这些复杂的解剖轨迹及其有序分割。我们展示了该模型能够泛化到涵盖发育、衰老和神经退行性疾病队列的多种外部数据集，在空间分辨率和角度采样变化的情况下仍保持稳健性能。发布的容器、训练好的模型、群体图谱、参考流线以及质量保证输出，为研究发育、衰老、疾病和神经调控相关解剖中的深部脑干和皮层下通路提供了一种资源。

## Abstract
Diffusion MRI enables noninvasive mapping of human white matter pathways, but automated segmentation methods have largely focused on large association, projection, and commissural bundles. Yet compact brainstem and subcortical pathways supporting basal ganglia, cerebellar, limbic/reward, sensory, and homeostatic functions remain underrepresented in large-scale connectomic analyses. To address this gap, we adapted BundleParc, a recently introduced bundle-parcellation architecture, into an automated pipeline for direct segmentation and along-tract parcellation of 97 subcortical and brainstem white matter pathways. The model was trained on a curated reference dataset derived from Human Connectome Project diffusion MRI using anatomy-guided tractography, explicit inclusion and exclusion criteria, automated outlier filtering, and manual quality assurance. Operating directly on native-space fiber orientation distributions, the algorithm successfully recovers these intricate anatomical trajectories and ordered parcellations. We show the model generalizes to diverse external datasets spanning development, aging, and neurodegenerative disease cohorts, maintaining robust performance across variations in spatial resolution and angular sampling. The released container, trained model, population atlas, reference streamlines, and quality assurance outputs provide a resource for studying deep brainstem and subcortical pathways in development, aging, disease, and neuromodulation-relevant anatomy.

---

## 论文详细总结（自动生成）

好的，请查收基于提供的论文元数据生成的结构化中文总结。

### 1. 论文的核心问题与整体含义

*   **研究背景与动机**：扩散磁共振成像（diffusion MRI）技术能够实现活体无创的人脑白质通路描绘。然而，领域内现有的自动化分割方法主要集中于大型纤维束，如投射、联络和连合纤维。
*   **核心问题**：支撑基底节、小脑、边缘/奖赏、感觉和稳态功能的紧凑、深部的脑干和皮层下白质通路，在规模化连接组学分析中常被忽视，代表性严重不足。
*   **整体含义**：本研究旨在填补这一技术空白，通过开发一套专门针对深部脑系统的自动化分割流程，为研究这些关键通路在神经调控、发育、衰老和疾病中的作用提供标准化资源，推动连接组学分析向更深、更精细的脑结构拓展。

### 2. 论文提出的方法论

*   **核心思想**：将一种名为 `BundleParc` 的纤维束分割框架，改造为一个专门处理皮层下与脑干白质通路的、端到端的深度学习自动化分割流水线。
*   **关键技术流程**：
    1.  **参考数据集构建**：模型训练的“金标准”并非人工直接标注，而是通过一套严格的流程生成。
        *   **解剖引导束路追踪**：基于解剖学先验知识进行纤维追踪。
        *   **明确纳入/排除标准**：设定规则筛选有效流线。
        *   **自动异常值过滤与人工质控**：通过算法和专家双重检查确保数据质量。
    2.  **模型算法特点**：
        *   **直接分割与沿束分区**：该算法不仅能分割出97条特定通路，还能同时生成沿纤维束走形的有序分区，描绘其内部亚结构。
        *   **原生空间操作**：模型直接作用于纤维取向分布函数，而非预处理后的标量图或模板空间，更好地保留了原始信号的几何信息。
*   **公式与算法流程**：文本未提供具体公式，但从描述可概括其逻辑流程：
    1.  **输入**：扩散 MRI 数据计算的纤维取向分布。
    2.  **处理**：经由 `BundleParc` 架构训练的深度学习模型，同时执行两个任务：对体素进行分类以识别和分割特定通路，以及为识别出的通路预测其内部的沿束分区标签。
    3.  **输出**：97条皮层下和脑干通路的直接分割图与沿束分区图。

### 3. 实验设计

*   **训练数据集**：
    *   模型训练基于来自 **人类连接组计划** 的扩散 MRI 数据，并经过了前述严格的参考数据整理流程。
*   **测试与泛化性验证数据集**：
    *   测试覆盖了多个外部独立队列，以全面评估模型的稳健性，包括：
        *   发育队列
        *   衰老队列
        *   神经退行性疾病队列
*   **评估场景与基准**：
    *   **内部基准**：通过与基于金标准流程构建的参考数据集进行对比。
    *   **泛化性基准**：重点评估模型在**不同空间分辨率**和**不同角度采样方案**的外部数据上能否保持性能，这构成了一个严苛的跨平台、跨人群泛化性测试。
*   **对比方法**：文本未提及与其他现有分割方法的直接定量比较，其验证重点在于自身方法在复杂解剖区域的恢复能力及跨数据集的稳健性。

### 4. 资源与算力

*   论文元数据中**未明确提及**进行模型训练时所使用的具体算力资源，例如 GPU 型号、数量或训练总时长。
*   信息指出最终成果包括了“发布的容器”和“训练好的模型”，这从侧面说明模型对运行环境有一定要求，并已为可复现和部署做了封装，但未提供原始训练开销的细节。

### 5. 实验数量与充分性

*   **实验组数量**：从元数据可推断出至少进行了以下几组核心实验：
    1.  基于 HCP 数据的模型训练与内部验证。
    2.  在多个独立外部数据集（发育、衰老、疾病）上的泛化性验证。
    3.  针对空间分辨率和角度采样变化等特定挑战的鲁棒性测试。
*   **实验充分性评估**：
    *   **充分性**：实验设计具有较高的充分性。它不仅在一组高质量数据上验证了模型的有效性，更重要的是在多中心、多人群、多成像参数的外部数据上系统性地检验了泛化能力，这对于评估一个声称能稳健工作的神经影像工具的临床和科研实用性至关重要。
    *   **客观性与公平性**：元数据未提供与其他主流分割方法的定量比较，因此无法评估对比实验的充分性与公平性。验证集中于证明该方法能够解决一个公认的、现有方法覆盖不足的难题，其价值在于“填补空白”而非“在相同任务上超越同行”。

### 6. 论文的主要结论与发现

*   **解剖解析能力**：所提出的算法能够成功地、准确地恢复深部脑干和皮层下这些复杂通路的解剖走形及其内部有序的分区结构，证明了深度学习用于此类精细解剖结构的可行性。
*   **泛化性与稳健性**：该模型展现出强大的泛化能力，能够在涵盖发育、衰老和疾病的不同外部数据上保持稳健性能，可以有效克服数据在**空间分辨率**和**角度采样**上的差异，这是其从方法走向应用的关键一步。
*   **资源贡献**：本研究的主要贡献之一是公开发布了一整套标准化资源，包括容器、训练模型、群体图谱、参考流线和质控输出，为神经科学界研究深层脑系统提供了可直接使用的关键工具。

### 7. 优点

*   **问题导向明确**：精准识别了当前连接组学分析中的一个显著盲区——深部紧凑通路，问题价值高。
*   **架构创新应用**：将 `BundleParc` 架构成功应用于全新的、更具挑战性的解剖目标，并实现了“分割+分区”的多任务输出，超越了简单的纤维束识别。
*   **数据驱动且严谨**：训练数据构建流程非常严格，结合了先验解剖知识、自动化过滤与人工质控，从源头保证了模型学习的质量。
*   **强调实用性与可复现性**：通过提供模型、容器和全套参考数据的开源共享策略，大大降低了其他研究者应用和复现的门槛，促进了方法的标准化和推广。

### 8. 不足与局限

*   **对比缺失**：文中未提及与基线方法或现有类似工具的直接性能比较，其相对优势主要体现在处理对象的新颖性和泛化性上，缺少定量化的领先性佐证。
*   **算力信息不透明**：未报告训练所需算力和时间成本，对需要评估复现成本或本地部署可行性的用户来说是一个信息缺失。
*   **评估指标未知**：总结中未出现分割准确性的具体量化指标（如 Dice 系数、表面距离等），结果的“成功性”依赖于定性描述和泛化鲁棒性证据，缺少精确的误差分析。
*   **金标准的潜在偏差风险**：尽管数据整理流程严格，但训练标签本质上来源于基于规则的纤维束追踪和人工编辑，这可能引入解剖学假设上的系统性偏差，并在复杂交叉或病变区域仍存在不确定性的风险。

（完）
