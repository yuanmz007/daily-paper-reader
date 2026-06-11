---
title: "MP-Nav: Enhancing Data Poisoning Attacks against Multimodal Learning"
title_zh: MP-Nav：增强针对多模态学习的数据投毒攻击
authors: "Jingfeng Zhang, Prashanth Krishnamurthy, Naman Patel, Anthony Tzes, Farshad Khorrami"
date: 2025-05-01
pdf: "https://openreview.net/pdf?id=zy7VeNtSLM"
tags: ["query:sem-vis-atk"]
score: 4.0
evidence: 增强针对多模态学习的数据投毒攻击，通过错误关联概念
tldr: 现有针对多模态学习的数据投毒攻击因随机选择概念和样本而效果欠佳。MP-Nav提出通过更优的导航策略来增强攻击，恶意注入少量样本以错误关联不同概念，从而在文本-图像检索和视觉问答任务中更好地操控模型行为。实验表明该方法提高了投毒攻击的成功率和隐蔽性，为多模态模型的安全性研究提供了新的攻击视角。
source: ICML-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-zy7ventslm/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1570, \"height\": 899, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zy7ventslm/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1762, \"height\": 372, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zy7ventslm/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 778, \"height\": 440, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zy7ventslm/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 838, \"height\": 475, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zy7ventslm/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1575, \"height\": 1050, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-zy7ventslm/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1101, \"height\": 477, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-zy7ventslm/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 884, \"height\": 121, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zy7ventslm/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1750, \"height\": 279, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zy7ventslm/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 895, \"height\": 252, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zy7ventslm/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1777, \"height\": 267, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zy7ventslm/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1766, \"height\": 1577, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-zy7ventslm/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1774, \"height\": 270, \"label\": \"Table\"}]"
motivation: 现有多模态数据投毒攻击因随机选择概念和样本导致攻击效果不理想，需要增强攻击策略。
method: 提出MP-Nav方法，通过优化概念错误关联和有毒样本选择来增强投毒攻击。
result: 在文本-图像检索和VQA任务上，攻击成功率和隐蔽性得到提升。
conclusion: MP-Nav展示了更有效的多模态投毒攻击，突显了多模态学习安全风险。
---

## Abstract
Despite the success of current multimodal learning at scale, its susceptibility to data poisoning attacks poses security concerns in critical applications. Attacker can manipulate model behavior by injecting maliciously crafted yet minute instances into the training set, stealthily mismatching distinct concepts. Recent studies have manifested the vulnerability by poisoning multimodal tasks such as Text-Image Retrieval (TIR) and Visual Question Answering (VQA). However, the current attacking method only rely on random choice of concepts for misassociation and random instance selections for injecting the poisoning noise, which often achieves the suboptimal effect and even risks failure due to the dilution of poisons by the large number of benign instances. This study introduces MP-Nav (Multimodal Poison Navigator), a plug-and-play module designed to evaluate and even enhance data poisoning attacks against multimodal models. MP-Nav operates at both the concept and instance levels, identifying semantically similar concept pairs and selecting robust instances to maximize the attack efficacy. The experiments corroborate MP-Nav can significantly improve the efficacy of state-of-the-art data poisoning attacks such as AtoB and ShadowCast in multimodal tasks, and maintain model utility across diverse datasets. Notably, this study underscores the vulnerabilities of multimodal models and calls for the counterpart defenses.

---

## 论文详细总结（自动生成）

好的，请查收以下基于提供的论文内容生成的结构化中文总结。

### 1. 论文的核心问题与整体含义（研究动机和背景）
- **核心问题**：尽管大规模多模态学习（如图文检索、视觉问答）取得了巨大成功，但其对 **数据投毒攻击** 的脆弱性构成了严重的安全隐患。攻击者可通过向训练集注入少量恶意样本，隐秘地让模型将两个不同的概念错误关联（误匹配），从而操控模型行为。
- **研究动机与背景**：
  - **现有攻击的不足**：目前的投毒攻击方法（如 AtoB、ShadowCast）在构建攻击时，**随机选择** 用于错误关联的“原始概念-目标概念”对，并且 **随机选择** 注入投毒噪声的具体实例。
  - **负面后果**：这种随机策略效果不佳，甚至可能因大量良性样本稀释毒药而失败。例如，强行错误关联语义不相似的“熊”和“公共汽车”比关联“熊”和“狮子”更难；随机毒化不具代表性的实例效果也远不如毒化概念中心的“稳健”实例。
- **整体含义**：本文旨在通过优化攻击策略，系统性地揭示并增强多模态模型在数据投毒攻击下的脆弱性，从而呼吁业界开发更强大的防御机制。

### 2. 论文提出的方法论
- **核心思想**：提出一个名为 **MP-Nav** 的即插即用模块，通过 **概念级** 和 **实例级** 的优化选择，来指导增强现有的数据投毒攻击，最大化攻击效果。
- **关键技术细节与算法流程**：
  1.  **概念级选择**：
      - **目标**：识别语义高度相似的原始概念和目标概念对，以降低错误关联的难度。
      - **流程**：利用开源多模态模型（如 CLIP），计算数据集中每个概念的图像和文本的平均嵌入向量，然后计算所有概念对之间的余弦相似度，构建相似度矩阵。攻击者根据此矩阵选择相似度最高的概念对进行攻击。
  2.  **实例级选择**：
      - **目标**：在每个选定的概念中，挑选出最具代表性的“稳健”实例进行毒化，使其在嵌入空间中更接近概念中心，增强毒药抵抗良性样本稀释的能力。
      - **流程**：
          - 计算每个概念的中心嵌入。
          - 计算每个实例嵌入与概念中心的余弦相似度（即邻近度）。
          - 根据邻近度对所有实例进行排序，选择排名靠前的、最接近概念中心的实例作为投毒目标。
  3.  **攻击执行**：将选定的概念与实例，应用于现有的投毒攻击框架（AtoB 或 ShadowCast），生成毒化数据集。

### 3. 实验设计
- **数据集与场景**：
  - **文本-图像检索 任务**：
    - **COCO 数据集**：用于评估 AtoB 攻击。训练集约 119k 图像，测试集 3.9k 图像。
    - **Flickr-PASCAL 数据集**：用于评估 AtoB 攻击。训练集约 29.5k 图像，测试集 500 图像。
  - **视觉问答 任务**：
    - **MiniGPT4 和自定义“拜登-特朗普”数据集**：用于评估 ShadowCast 攻击。277 个训练实例，200 个测试实例。
    - **Food101 数据集**：用于在可控条件下对比 ShadowCast 攻击。包含 101 个食物类别，共 101k 图像。
- **对比基准与方法**：
  - 对比了使用 MP-Nav 前后的攻击性能。
  - MP-Nav 的配置：仅概念选择、仅实例选择、概念+实例联合选择，与随机选择的基线方法进行对比。
- **评估指标**：
  - **模型效用**：R@1, R@5, R@10（文本和图像检索），GQA 基准性能（VQA 任务）。
  - **投毒效力**：
    - AtoB 攻击：Hit@K（目标图像在 Top-K 结果中的命中率），MinRank（目标图像的最低排名）。
    - ShadowCast 攻击：攻击成功率（模型错误提及目标概念而未提及原始概念的比例）。

### 4. 资源与算力
- **说明**：论文中**未明确提及**使用的 GPU 型号、数量及具体训练时长。只提到了训练过程使用了 AdamW 优化器等方法，但未给出硬件资源和具体算力开销的细节。

### 5. 实验数量与充分性
- **实验数量**：论文进行了多组实验，覆盖了。
  - **两个核心任务**：文本-图像检索（TIR）和视觉问答（VQA）。
  - **两个主流攻击方法**：AtoB 和 ShadowCast。
  - **三个数据集**：COCO、Flickr-PASCAL、Food101 及一个自定义的拜登-特朗普数据集。
  - **消融实验**：对 MP-Nav 的“概念选择”和“实例选择”组件进行了单独的消融研究。
  - **多维度评估**：不仅评估了攻击效力的提升（Hit@K, MinRank, 攻击成功率），还验证了攻击的隐蔽性，即对原模型效用的影响。
- **充分性、客观性与公平性**：
  - **充分性**：实验设计比较全面，涵盖了不同任务、不同攻击方法、不同数据集和多维度指标，且重复了多次实验以报告标准差，体现了统计稳定性。
  - **客观性与公平性**：对比基线与 MP-Nav 的配置一致，仅在选择策略上有差异，比较公平。消融实验清晰地展示了不同组件（概念和实例）的贡献。不过，所有实验均在强假设（攻击者可访问开源模型和数据集）下进行，这在真实黑盒场景中可能不成立。

### 6. 论文的主要结论与发现
- MP-Nav 能够通过概念级和实例级的智能选择，**显著增强** 现有数据投毒攻击（AtoB 和 ShadowCast）的效果。
- 在 TIR 任务中，MP-Nav 提高了 Hit@K 并降低了 MinRank。
- 在 VQA 任务中，MP-Nav 显著提升了攻击成功率，尤其是在攻击预算小、存在良性样本稀释时，实例级选择的优势更加明显。
- 通过 MP-Nav 增强的投毒攻击能够保持与干净模型相当的模型效用，确保了攻击的 **隐蔽性**。
- 研究结果进一步证实并**突出了多模态模型面对精心设计的投毒攻击时的脆弱性**。

### 7. 优点
- **方法创新性**：首次系统性地从“概念”和“实例”两个层面提出导航策略来增强多模态投毒攻击，为红队测试提供了新的视角。
- **即插即用性**：MP-Nav 模块被设计为可轻易嵌入现有攻击框架（如 AtoB、ShadowCast），实用性高。
- **实验设计全面**：实验覆盖了多个主流任务、数据集和攻击方法，并包含细致的消融实验，结论可靠。
- **关注攻击隐蔽性**：不仅追求攻击成功，还持续监控并验证了对模型原始性能的影响，更贴合现实攻击要求。

### 8. 不足与局限
- **攻击假设较强**：方法建立在攻击者能够访问开源模型和大型数据集的假设上，与现实中的黑盒攻击场景有差距。
- **缺乏防御对策探讨**：论文重点在于增强攻击，虽然结尾呼吁开发防御，但未对潜在的防御机制进行实验或讨论。
- **实验规模与验证范围有限**：
  - 仅在有限的数据集和特定的预训练模型（如 CLIP ViT-B/32, LLaVA-1.5）上进行了验证，迁移到更大型、更先进的模型（如更大规模的 ViT 或 GPT-4 系列）上的效果未可知。
  - 未测试针对可能存在的防御手段（如数据清洗、鲁棒训练）的有效性。
- **算力信息缺失**：未报告任何计算资源开销，使得复现成本和攻击的实用性难以评估。
- **潜在偏差风险**：概念间的相似性高度依赖于所使用的开源嵌入模型。如果攻击者无法获取与被攻击模型分布相似的嵌入模型，MP-Nav 的选择可能并非最优。

（完）
