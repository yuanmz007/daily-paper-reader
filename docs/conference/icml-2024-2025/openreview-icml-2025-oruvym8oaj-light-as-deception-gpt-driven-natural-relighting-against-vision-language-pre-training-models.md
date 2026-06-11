---
title: "Light as Deception: GPT-driven Natural Relighting Against Vision-Language Pre-training Models"
title_zh: 以光为欺：GPT驱动的自然重光照攻击视觉语言预训练模型
authors: "Ying Yang, Jie Zhang, Xiao Lv, Di Lin, Tao Xiang, Qing Guo"
date: 2025-01-23
pdf: "https://openreview.net/pdf?id=ORUVYM8OaJ"
tags: ["query:sem-vis-atk"]
score: 10.0
evidence: 提出LightD，通过语义引导的重新打光为视觉语言预训练模型生成自然对抗样本
tldr: 针对现有方法难以生成自然且语义有意义的对抗样本的挑战，LightD利用ChatGPT提出上下文相关的初始光照参数，结合预训练重光照模型生成自然的对抗图像，成功攻击视觉语言预训练模型，证明了语义层视觉攻击的有效性。
source: ICML-2025-Rejected-Public
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-icml-2025-oruvym8oaj/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 848, \"height\": 392, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oruvym8oaj/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 857, \"height\": 488, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oruvym8oaj/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1751, \"height\": 651, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oruvym8oaj/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1775, \"height\": 349, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oruvym8oaj/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1754, \"height\": 536, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oruvym8oaj/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1770, \"height\": 498, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oruvym8oaj/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 782, \"height\": 617, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oruvym8oaj/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1773, \"height\": 458, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oruvym8oaj/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1774, \"height\": 495, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oruvym8oaj/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1781, \"height\": 802, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-icml-2025-oruvym8oaj/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1770, \"height\": 1085, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-icml-2025-oruvym8oaj/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 861, \"height\": 1037, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oruvym8oaj/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 864, \"height\": 453, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oruvym8oaj/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 865, \"height\": 118, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oruvym8oaj/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 861, \"height\": 136, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oruvym8oaj/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1399, \"height\": 341, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-icml-2025-oruvym8oaj/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1504, \"height\": 1121, \"label\": \"Table\"}]"
motivation: 现有VLP对抗攻击方法因优化空间受限，难以生成自然且语义显著的扰动。
method: LightD利用ChatGPT建议上下文感知的初始光照参数，结合IC-light重光照模型，通过语义引导的重新打光生成对抗样本。
result: 实验表明，LightD生成的对抗样本能有效欺骗VLP模型，且保持高度自然。
conclusion: 该工作首次通过语义引导的重新打光实现了针对VLP模型的高效自然对抗攻击，揭示了语义层视觉扰动的重要性。
---

## Abstract
While adversarial attacks on vision-and-language pretraining (VLP) models have been explored, generating natural adversarial samples crafted through realistic and semantically meaningful perturbations remains an open challenge. Existing methods, primarily designed for classification tasks, struggle when adapted to VLP models due to their restricted optimization spaces, leading to ineffective attacks or unnatural artifacts. 
To address this, we propose **LightD**, a novel framework that generates natural adversarial samples for VLP models via semantically guided relighting. Specifically, LightD leverages ChatGPT to propose context-aware initial lighting parameters and integrates a pretrained relighting model (IC-light) to enable diverse lighting adjustments. LightD expands the optimization space while ensuring perturbations align with scene semantics. Additionally, gradient-based optimization is applied to the reference lighting image to further enhance attack effectiveness while maintaining visual naturalness.
The effectiveness and superiority of the proposed LightD have been demonstrated across various VLP models in tasks such as image captioning and visual question answering.

---

## 论文详细总结（自动生成）

好的，作为一名资深的学术论文分析助手，我将以Markdown形式，对您提供的论文《Light as Deception: GPT-driven Natural Relighting Against Vision-Language Pre-training Models》进行结构化、深入、客观的总结。

### **1. 论文的核心问题与整体含义 (研究动机和背景)**

*   **核心问题**：当前针对视觉-语言预训练模型的对抗攻击方法，主要通过在像素空间添加人眼不可见的微小扰动（Lp范数约束）实现。这类攻击容易被去噪防御机制抵御，且缺乏现实意义。为生成更“不易引起怀疑”的对抗样本，一些方法尝试调整语义级属性（如颜色、光照），但它们在针对VLP模型的复杂多模态任务时，普遍面临一个开放挑战：**难以在保证高攻击成功率的同时，维持图像的视觉自然度和语义一致性**。
*   **整体含义**：本研究旨在探索一种**更实际、更隐蔽**的对抗攻击范式。论文提出，通过模拟自然环境下的光照变化来生成对抗样本，不仅能有效欺骗VLP模型，还能让生成的图像在人类看来是完全自然、无篡改痕迹的，从而揭示了VLP模型面对语义级物理世界扰动的脆弱性。

### **2. 论文提出的方法论 (核心思想、关键技术细节)**

论文提出了名为 **LightD** 的框架，其核心思想是**利用GPT驱动的语义引导重光照技术，生成自然且具有攻击性的图像**。该方法包含三个关键组件：

*   **GPT驱动的光照参数选择**：
    *   为生成符合图像场景的初始光照，LightD使用ChatGPT分析图像内容。
    *   ChatGPT根据精心设计的提示模板，推荐初始的光照参数，包括起始颜色、结束颜色和光照方向。这确保了初始的重光照在视觉上是合理的。

*   **重光照驱动的对抗图像生成**：
    *   **参考光照图像生成器**：利用一个光照图像生成函数，将ChatGPT推荐的参数（颜色、方向、权重）转化为一张纯色的参考光照图。
    *   **预训练重光照模型**：使用一个预训练的扩散模型IC-Light，在“光照条件”模式下工作。该模型能够将参考光照图中的光照效果一致性地施加到原始干净图像上，生成一张只有光照变化、没有内容改变的重光照图像。

*   **基于光照的协作优化**：
    *   这是提升攻击成功率的核心策略，采用了受SGA思想启发的两步迭代优化过程。
    *   **第一步：光照参数优化**。将光照参数（颜色）作为优化变量，通过梯度上升法（计算损失函数对参数的梯度）来微调这些参数，目标是最大化攻击损失。
    *   **第二步：参考光照图像优化**。在最优参数的基础上，将整张参考光照图作为优化变量。通过多次缩放参考图来增强多样性，然后计算损失函数对图像像素的梯度，并以此扰动图像，进一步扩大优化空间。
    *   **损失函数设计**：损失函数平衡了两个目标：① **攻击性**：最大化对抗图像编码与正确文本编码之间的差异（如交叉熵损失）；② **视觉自然性**：最小化对抗图像编码与原始图像编码之间的差异（如余弦相似度损失），确保图像内容不变。

### **3. 实验设计 (数据集、基准、对比方法)**

*   **数据集与场景**：
    *   **图像描述**：MSCOCO, Flickr8K, Flickr30K。从每个数据集的测试集中随机选取1000张图片。
    *   **视觉问答**：MSCOCO, DAQUAR数据集。
*   **Baselines (对比方法)**：
    *   三类先进的非可疑对抗攻击方法被作为基准，并通过论文提出的通用优化框架适配到VLP任务上。
        *   **对抗重光照攻击**：ALA, EdgeFool, Jadena。
        *   **对抗色彩攻击**：SemanticAdv, ColorFool, AdvCF。
*   **受害者VLP模型**：
    *   **图像描述任务**：CLIPCap, BLIP, BLIP2。
    *   **视觉问答任务**：BLIP, BLIP2。

### **4. 资源与算力 (GPU型号、数量、训练时长等)**

*   **论文并未明确提及**所使用的具体GPU型号、数量以及训练或优化的具体时长。这是一个报告中缺失的信息点。

### **5. 实验数量与充分性 (实验组数、充分性、客观性、公平性)**

*   **实验数量**：实验设计较为全面，涵盖了：
    *   **主要性能对比**：在两个下游任务（Image Captioning, VQA）、三个数据集（MSCOCO, Flickr30K， 以及附录中的Flickr8K和DAQUAR）、针对多个VLP模型，与6个基线方法进行了横向对比。据此推算，主实验约有 **(3模型 × 2数据集 + 2模型 × 2任务) × N个指标** 组对比。
    *   **消融实验**：在MSCOCO数据集上，针对BLIP2模型，进行了两个关键组件的消融研究：① 验证ChatGPT推荐光照参数的有效性（对比随机选择）；②验证两步协作优化策略的有效性（对比单独优化参数、单独优化光照图）。
    *   **参数敏感性分析**：探讨了参考光照图像优化中的缩放次数（M）对攻击性能和自然度的影响。
*   **充分性与公平性**：实验整体是**充分且客观公平的**。为了公平对比，论文专门提出了一个通用框架，将原本用于图像分类的基线攻击方法迁移到VLP任务上，保证了所有方法在可比条件下进行评估。评估指标综合了攻击成功性指标和视觉自然度指标，使结论更具说服力。

### **6. 论文的主要结论与发现**

*   **现有方法的局限性**：实验证实，现有的色彩/光照攻击方法在迁移到VLP模型时，无法同时实现有效的攻击和高视觉自然度。
*   **LightD的优越性**：LightD在所有测试的VLP模型和任务上都显著优于基线方法，不仅攻击成功率更高（在图像描述任务中，各项指标分数更低；在VQA中准确率更低），而且保持了更低的NIQE值（表示图像质量更好），实现了攻击性与自然度的最优平衡。
*   **关键组件的有效性**：消融实验表明，GPT提供的光照参数初始值和两步协作优化策略都对最终性能有积极贡献，尤其是优化策略的引入至关重要。

### **7. 优点 (方法或实验设计上的亮点)**

*   **新颖的攻击范式**：创新性地将**扩散模型驱动的图像重光照**作为一种非可疑对抗攻击手段，扰动在语义层面（光照），对人类观察者来说非常自然。
*   **GPT的巧妙应用**：利用大语言模型的常识推理能力，为每张图像定制化地生成符合场景的初始光照参数，避免了盲目搜索，提升了生成图像的初始质量和攻击的自然性。
*   **有效的优化策略**：提出的“参数+图像”两步协作优化，有效扩大了优化空间，解决了单一类型优化可能遇到的瓶颈，极大地提升了攻击强度。
*   **完善的基准测试框架**：为适配现有方法而提出的通用优化框架，为该领域的后续研究提供了一个标准化和可复现的评估基准。

### **8. 不足与局限 (实验覆盖、偏差风险、应用限制等)**

*   **物理可实现性未验证**：攻击是在数字域生成的。论文未讨论或实验验证在物理世界中，通过实际改变光源能否复现并成功执行此类攻击。
*   **模型和场景覆盖有限**：
    *   受害者模型主要集中在大规模预训练的Transformer架构上，缺少对更早期或架构不同的VLP模型的评估。
    *   下游任务仅覆盖了图像描述和VQA，未涉及图像-文本检索等其他关键多模态任务。
*   **评估指标的局限性**：虽然NIQE用于评估自然度，但它是一个无参考评价指标，可能无法完全对齐人类的真实感知。缺乏用户主观评测来进一步证实其“非可疑”性。
*   **依赖外部工具**：方法的性能高度依赖于GPT的推荐能力和IC-Light模型的生成质量，这些外部工具的更新或变更可能会影响LightD的稳定性和效果。
*   **防御探讨缺失**：论文仅提出了攻击方法，并未探讨VLP模型针对此类语义级扰动的潜在防御策略。

（完）
