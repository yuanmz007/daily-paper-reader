---
title: "A Frustratingly Simple Yet Highly Effective Attack Baseline: Over 90% Success Rate Against the Strong Black-box Models of GPT-4.5/4o/o1"
title_zh: "一种简单却高效的攻击基线：对GPT-4.5/4o/o1等强黑盒模型超过90%成功率"
authors: "Zhaoyi Li, Xiaohan Zhao, Dong-Dong Wu, Jiacheng Cui, Zhiqiang Shen"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=9xXjWwAoUF"
tags: ["query:sem-vis-atk"]
score: 9.0
evidence: 在对抗扰动局部区域编码明确语义细节以攻击LVLM
tldr: "针对面向黑盒大视觉语言模型的迁移攻击成功率低的问题，本文提出通过精炼语义清晰度、在局部区域编码显式语义细节的简单攻击基线方法，实现对GPT-4.5等模型超90%的成功率，表明语义信息对黑盒攻击的关键作用。"
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1415, \"height\": 507, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1443, \"height\": 397, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 703, \"height\": 460, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 723, \"height\": 451, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1396, \"height\": 553, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1397, \"height\": 556, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1447, \"height\": 830, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1422, \"height\": 279, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 930, \"height\": 379, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1398, \"height\": 815, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1425, \"height\": 388, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 157, \"height\": 155, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 163, \"height\": 150, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 153, \"height\": 152, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 159, \"height\": 155, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 156, \"height\": 156, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 161, \"height\": 154, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 162, \"height\": 160, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 158, \"height\": 145, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 829, \"height\": 493, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1455, \"height\": 1471, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1454, \"height\": 1383, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-9xxjwwaouf/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1449, \"height\": 1395, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 858, \"height\": 198, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1449, \"height\": 360, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1450, \"height\": 530, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 718, \"height\": 179, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 712, \"height\": 178, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1235, \"height\": 254, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1434, \"height\": 161, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1381, \"height\": 265, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1436, \"height\": 463, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1346, \"height\": 216, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 968, \"height\": 270, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 1087, \"height\": 387, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 863, \"height\": 218, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 864, \"height\": 219, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1299, \"height\": 348, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 1301, \"height\": 343, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 866, \"height\": 483, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1150, \"height\": 211, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-9xxjwwaouf/table-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1150, \"height\": 468, \"label\": \"Table\"}]"
motivation: 现有迁移攻击因缺乏语义信息导致黑盒商用LVLM攻击失败，需要增强对抗扰动的语义清晰度。
method: 提出在对抗扰动的局部区域编码显式语义细节，精炼语义清晰度的攻击方法。
result: "在GPT-4.5等强黑盒模型上达到超过90%的攻击成功率。"
conclusion: 语义清晰度对黑盒LVLM攻击至关重要，简单方法即可显著提升攻击效果。
---

## Abstract
Despite promising performance on open-source large vision-language models (LVLMs), transfer-based targeted attacks often fail against closed-source commercial LVLMs. Analyzing failed adversarial perturbations reveals that the learned perturbations typically originate from a uniform distribution and lack clear semantic details, resulting in unintended responses. This critical absence of semantic information leads commercial black-box LVLMs to either ignore the perturbation entirely or misinterpret its embedded semantics, thereby causing the attack to fail. To overcome these issues, we propose to refine semantic clarity by encoding explicit semantic details within local regions, thus ensuring the capture of finer-grained features and inter-model transferability, and by concentrating modifications on semantically rich areas rather than applying them uniformly. To achieve this, we propose  *a simple yet highly effective baseline*: at each optimization step, the adversarial image is cropped randomly by a controlled aspect ratio and scale, resized, and then aligned with the target image in the embedding space. While the naive source-target matching method has been utilized before in the literature, we are the first to provide a tight analysis, which establishes a close connection between perturbation optimization and semantics. Experimental results confirm our hypothesis. Our adversarial examples crafted with local-aggregated perturbations focused on crucial regions exhibit surprisingly good transferability to commercial LVLMs, including GPT-4.5, GPT-4o, Gemini-2.0-flash, Claude-3.5/3.7-sonnet, and even reasoning models like o1, Claude-3.7-thinking and Gemini-2.0-flash-thinking. Our approach achieves success rates exceeding 90\% on GPT-4.5, 4o, and o1, significantly outperforming all prior state-of-the-art attack methods with lower $\ell_1/\ell_2$ perturbations. Our optimized adversarial examples under different configurations are available at https://huggingface.co/datasets/MBZUAI-LLM/M-Attack_AdvSamples and our training code at https://github.com/VILA-Lab/M-Attack.

---

## 论文详细总结（自动生成）

好的，以下是根据您提供的论文内容生成的结构化中文总结。

---

### 1. 论文的核心问题与整体含义

*   **研究背景与动机**：当前的大型视觉语言模型，特别是GPT-4o、Claude-3.5、Gemini-2.0等闭源商业模型，已被广泛部署并对抗恶意攻击。现有基于迁移的攻击方法虽然对开源模型有效，但在攻击这些强鲁棒性的黑盒商业模型时往往失败。
*   **核心问题**：作者通过分析失败案例发现，传统攻击方法生成的对抗性扰动通常近似于**均匀分布**，**缺乏清晰的语义细节**。这些无意义的噪声要么被黑盒模型完全忽略，要么被错误解读，导致攻击无法产生预期的、有具体语义内容的错误输出。
*   **整体含义**：本文旨在揭示，提升对抗扰动**内部局部区域的语义清晰度**是成功攻击黑盒大视觉语言模型的关键。通过一个非常简单的攻击基线方法，作者证明了即使面对最强大的商业模型，也能实现极高的攻击成功率，从而对当前AI系统的鲁棒性和安全性提出了严峻挑战。

### 2. 论文提出的方法论

*   **核心思想**：通过**精炼对抗性扰动的局部语义清晰度**来提升攻击的可迁移性。具体而言，不是在整个图像上施加均匀噪声，而是在图像中语义丰富的局部区域编码清晰的目标图像语义，确保黑盒模型能够感知并误读这些被精心设计的特征。
*   **关键技术细节（M-Attack框架）**：
    *   **局部到全局/局部的匹配（Local-to-Global/Local Matching）**：
        *   **操作**：在每次优化迭代中，对当前的对抗图像进行**随机裁剪**（控制裁剪比例），然后将其调整回原始尺寸。
        *   **目的**：在嵌入空间中，将这个`随机裁剪-调整尺寸`后的局部区域特征与目标图像的特征进行余弦相似度对齐。这种机制使得对抗扰动能在中心区域逐步聚合并精炼出清晰的语义，形成许多对多的局部特征映射，避免了过拟合，增强了细节表达能力。
    *   **模型集成（Model Ensemble）**：
        *   **操作**：同时使用多个白盒替代模型（如不同补丁大小`patch size`的CLIP模型）来计算损失和梯度。
        *   **目的**：小补丁模型能提取更精细的扰动细节，而大补丁模型能更好地保持整体结构和模式。集成模型能够融合这些互补优势，生成更高质量的语义扰动，并提取出对未知黑盒模型更具迁移性的共享语义。
*   **公式与算法流程概述**：
    *   算法流程（`Algorithm 1`）可以概括为：初始化对抗图像为干净图像，然后在每一步迭代中，对源图像和目标图像分别应用随机裁剪变换`Ts`和`Tt`，得到局部特征。接着，计算集成模型中所有代理模型对该对局部特征余弦相似度的平均损失，并利用该损失的梯度（通过`I-FGSM`等方法）更新扰动，最后将更新后的扰动裁剪回允许的$\epsilon$范围内。

### 3. 实验设计

*   **数据集与场景**：
    *   **数据集**：主要使用**NIPS 2017对抗攻击与防御竞赛**的数据集，从中采样了100张图像（主要实验）和1000张图像（扩展实验）用于统计可靠性分析。图像尺寸统一调整为224x224像素。
    *   **任务场景**：主要评估**目标性、基于迁移的黑盒攻击**，即让黑盒模型将对抗图像（源图像）错误描述为目标图像的内容。在附录中，还评估了图像描述和视觉问答任务。
*   **Benchmark与对比方法**：
    *   **目标受害黑盒模型**：GPT-4.5, GPT-4o, o1, Claude-3.5/3.7-sonnet, Gemini-2.0-flash及其推理版本。
    *   **对比方法（Baselines）**：与四种先进的迁移攻击方法进行了比较：**AttackVLM**、**SSA-CWA**、**AnyAttack**、**AdvDiffVLM**。
*   **评估指标**：
    *   **KMRScore（关键词匹配率）**：作者提出的新指标，以减少人为主观性。通过人工为每张目标图像标注多个语义关键词，并使用GPT-4o自动判断黑盒模型的输出描述匹配了哪些关键词，最终计算匹配率（如KMRa、KMRb、KMRc分别代表至少、超过一半、完全匹配关键词的成功率）。
    *   **ASR（攻击成功率）**：基于GPTScore的方法，使用LLM-as-a-judge的思想，计算黑盒模型对源图像（经攻击后）的描述与对目标图像的描述之间的语义相似度，超过0.3阈值视为攻击成功。
    *   **不可感知性（Imperceptibility）**：使用归一化的$\ell_1$和$\ell_2$范数来衡量扰动大小。

### 4. 资源与算力

*   **硬件配置**：实验在**4块 NVIDIA RTX 4090 GPU**上进行。
*   **计算开销**：
    *   **生成单张对抗图像的时间**：**20.04秒**（使用单张RTX 4090）。
    *   **生成单张对抗图像的显存占用**：**549.78 MB**。

### 5. 实验数量与充分性

*   **实验组数量**：论文包含了非常丰富的实验，覆盖充足且客观公平。
    *   **主实验**：在三个主流黑盒模型（GPT-4o, Gemini, Claude）上，与4种最先进方法进行了全面的比较，同时使用多个`KMRScore`和ASR指标进行评估。
    *   **消融研究**：
        *   **组件消融**：逐一移除“源图像局部裁剪”、“目标图像局部裁剪”和“模型集成”等核心组件，验证其重要性。
        *   **参数消融**：研究了不同扰动预算`$\epsilon$`（4， 8， 16）、优化步数（100-500）、随机裁剪比例`[a， b]`、步长参数`$\alpha$`等对性能的影响。
        *   **匹配策略消融**：对比了局部-局部、局部-全局、全局-局部、全局-全局四种匹配方式，以及与传统数据增强（如旋转、色彩抖动）的对比，突出了所提方法中局部操作的不可替代性。
        *   **集成模型消融**：研究了集成模型中不同子模型（如移除某一个CLIP模型，或加入BLIP2）对各个受害模型的不同影响。
    *   **扩展与鲁棒性实验**：
        *   在更大规模的**1K图像数据集**上进行了验证。
        *   证明了方法对**推理模型**（o1等）和**最新的商业模型**（GPT-4.5等）同样有效。
        *   在开源大视觉语言模型（LLaVA， Qwen-VL）和生活场景任务（图像描述、视觉问答）上验证了有效性。
        *   对比了不同优化器实现（I-FGSM, MI-FGSM, PGD-ADAM），证明了算法的框架独立性。
        *   对攻击失败案例和扰动分布（KL散度）进行了定量和定性分析，支撑了论文的核心论点。
*   **公平性**：所有对比方法均使用了与原论文一致的设置和推荐的替代模型。评估时，作者对LLM温度参数置零，并手动校验了20%的KMRScore输出，确保了评估的客观性和可复现性。

### 6. 论文的主要结论与发现

*   **语义是关键**：对抗扰动缺乏清晰的局部语义是导致迁移攻击失效的根本原因。将扰动聚焦于图像中的关键语义区域，并使其具备可被感知和误读的语义细节，是有效攻击黑盒大视觉语言模型的关键。
*   **攻击方法极其有效**：提出的M-Attack是一个极其简单（随机裁剪+对齐）却非常强大的攻击基线。它在**GPT-4.5/4o/o1等强黑盒模型上实现了超过90%的攻击成功率**，远超所有现有方法，并且扰动的$\ell_1/\ell_2$范数更低，即**攻击更隐蔽、更强**。
*   **局部操作与模型的协同作用**：局部匹配（尤其是源图像的局部操作）和模型集成是两大核心设计，它们协同工作，使得整体攻击性能的提升大于二者各自贡献之和。
*   **推理模型同样脆弱**：具备强大推理能力的商业模型（如o1）在面对此类视觉对抗攻击时，鲁棒性并不比其非推理版本更强。

### 7. 优点

*   **方法论洞察深刻**：对失败攻击中扰动缺乏语义的分析非常透彻（如ECDF曲线、KL散度、模糊描述统计），为攻击设计提供了可靠的理论依据。
*   **方法简单高效**：提出的M-Attack方法容易复现，效果好，成功率高且扰动更小，树立了新的最先进基线。
*   **评估体系新颖客观**：引入`KMRScore`，结合自动化和人工校验，提供了一种比单纯依赖GPTScore或主观判断更精细、更客观的评估方式，解决了评价标准模糊的问题。
*   **实验设计严谨全面**：实验覆盖了多个主流商业模型和推理模型，进行了大量的、多角度的消融研究，结论信服度高。代码和数据均已开源，具有良好的可复现性。

### 8. 不足与局限

*   **攻击目标的局限性**：主要验证了**目标性攻击**，即让模型输出预设的错误描述。对于非目标性攻击或更复杂的多模态任务，其有效性有待进一步探究。
*   **对防御技术的鲁棒性未知**：论文未探讨当前常见的防御技术（如对抗训练、输入净化等）对该攻击方法的抵御能力，实际应用环境下的鲁棒性存疑。
*   **模型演进风险**：论文承认随着更强大的新模型发布，该方法的有效性不能永久保证，需要持续进行适应性评估。
*   **数据集多样性**：主实验仅基于NIPS 2017数据集，场景相对单一。虽然补充了1K图像的实验，但数据集多样性仍有提升空间。
*   **潜在的社会风险**：该方法可被滥用于生成误导信息或绕过内容安全审核，论文仅在“更广泛影响”中提及，未提出具体的防御或缓解措施。

（完）
