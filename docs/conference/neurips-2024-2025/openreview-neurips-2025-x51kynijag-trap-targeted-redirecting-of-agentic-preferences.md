---
title: "TRAP: Targeted Redirecting of Agentic Preferences"
title_zh: TRAP：定向重定向智能体偏好
authors: "Hangoo Kang, Jehyeok Yeon, Gagandeep Singh"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=X51kYnijag"
tags: ["query:sem-vis-atk"]
score: 10.0
evidence: 基于扩散的语义注入操控视觉语言模型智能体的决策
tldr: 现有视觉语言模型对抗攻击多依赖可见像素扰动或需白盒访问，难以实际部署。TRAP提出基于扩散的生成式对抗框架，通过负向提示退化与正向语义优化，在视觉-语言嵌入空间进行语义注入，隐蔽重定向智能体决策偏好。实验表明该方法可在不引入可见噪声的条件下有效操控VLM驱动的自主智能体，为多模态安全评估提供新攻击范式。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-x51kynijag/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1299, \"height\": 721, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-x51kynijag/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1158, \"height\": 563, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-x51kynijag/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1398, \"height\": 612, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-x51kynijag/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1123, \"height\": 725, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-x51kynijag/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1394, \"height\": 431, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-x51kynijag/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1275, \"height\": 224, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-x51kynijag/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1469, \"height\": 307, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-x51kynijag/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1379, \"height\": 326, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-x51kynijag/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1380, \"height\": 325, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-x51kynijag/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1134, \"height\": 379, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-x51kynijag/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1133, \"height\": 377, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-x51kynijag/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1134, \"height\": 268, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-x51kynijag/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1131, \"height\": 291, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-x51kynijag/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 1132, \"height\": 395, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-x51kynijag/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 1273, \"height\": 304, \"label\": \"Table\"}]"
motivation: 现有针对视觉语言模型的对抗攻击依赖可见像素扰动或需要特权访问，难以在实际场景中隐蔽实施。
method: 提出TRAP框架，结合负向提示退化与正向语义优化，在扩散模型的视觉-语言嵌入空间中注入语义扰动。
result: 该方法实现了对VLM智能体决策偏好的隐蔽操控，避免了可见像素修改。
conclusion: TRAP验证了通过语义级注入可有效操纵多模态模型的行为，为实际场景下的对抗攻击提供了新思路。
---

## Abstract
Autonomous agentic AI systems powered by vision-language models (VLMs) are rapidly advancing toward real-world deployment, yet their cross-modal reasoning capabilities introduce new attack surfaces for adversarial manipulation that exploit semantic reasoning across modalities. Existing adversarial attacks typically rely on visible pixel perturbations or require privileged model or environment access, making them impractical for stealthy, real-world exploitation. We introduce TRAP, a novel generative adversarial framework that manipulates
the agent’s decision-making using diffusion-based semantic injections into the vision-language embedding space. Our method combines negative prompt–based degradation with positive semantic optimization, guided by a Siamese semantic network and layout-aware spatial masking. Without requiring access to model internals, TRAP produces visually natural images yet induces consistent selection
biases in agentic AI systems. We evaluate TRAP on the Microsoft Common Objects in Context (COCO) dataset, building multi-candidate decision scenarios. Across these scenarios, TRAP consistently induces decision-level preference redirection on leading models, including LLaVA-34B, Gemma3, GPT-4o, and Mistral-3.2, significantly outperforming existing baselines such as SPSA, Bandit, and standard diffusion approaches. These findings expose a critical, generalized vulnerability: autonomous agents can be consistently misled through visually subtle, semantically-guided cross-modal manipulations. Overall, our results show the need for defense strategies beyond pixel-level robustness to address semantic vulnerabilities in cross-modal decision-making. The code for TRAP is accessible on GitHub at https://github.com/uiuc-focal-lab/TRAP.

---

## 论文详细总结（自动生成）

### 1.  论文的核心问题与整体含义
*   **研究背景**：基于视觉-语言模型 (VLMs) 的自主智能体系统正快速走向实际应用。然而，其处理多模态信息的能力引入了新的攻击面，即利用跨模态语义推理的对抗性操纵。
*   **核心问题**：现有的对抗性攻击通常依赖于可视的像素扰动，或需要模型、环境的特权访问权限（白盒攻击），这使得它们在需要隐蔽性的真实场景中不切实际。
*   **研究动机**：为揭示并验证一种更隐蔽、更具现实威胁的跨模态漏洞，即通过语义注入而非像素级噪声，来操纵智能体的决策偏好。
*   **整体含义**：本文提出了一种新型攻击框架 TRAP，它能在黑盒条件下，生成视觉上自然但语义被篡改的图像，从而持续且隐蔽地误导自主智能体的选择行为。这暴露了多模态系统在语义层面的关键脆弱性，强调安全防御需超越像素级鲁棒性。

### 2.  论文提出的方法论
TRAP 是一个生成式对抗框架，其核心思想是在 CLIP 模型的潜在嵌入空间中，通过语义注入来优化图像，而非直接修改像素。该方法结合了负向提示引导的退化和正向语义优化，整个框架包括四个阶段，具体的技术细节如下：
*   **核心思想**：
    *   **语义注入**：在 CLIP 的共享嵌入空间中，通过优化图像的表示，使其与一个攻击者设定的正向引导提示（\( p_{pos} \)）在语义上高度对齐，从而在视觉不变的情况下改变其高级语义。
    *   **身份保持**：引入孪生语义网络和独特的特征保留损失，确保对抗性编辑不会破坏图像原有的独特身份和视觉辨识度。
*   **关键技术细节与优化流程**：
    *   **问题形式化**：攻击目标是在给定一个文本提示 \( p \) 和一组候选图像 \( \{x_i\} \) 时，使智能体模型 \( M \) 选择攻击者指定的对抗性图像 \( x_{adv} \)，同时要求 \( x_{adv} \) 与原始图像在感知上相似。
    *   **总损失函数**：优化目标是最小化一个复合损失函数，该函数是可变的对抗性嵌入 \( e_{adv} \) 的函数。
        *   \( L_{total} = \lambda_1 L_{sem} + \lambda_2 L_{dist} + \lambda_3 L_{LPIPS} \)
    *   **语义对齐损失 (\( L_{sem} \))**：计算对抗性嵌入 \( e_{adv} \) 与正向提示嵌入 \( e_{pos} \) 之间的余弦距离，旨在注入高级语义，使图像对特定查询更具吸引力。
        *   \( L_{sem}(e_{adv}, e_{pos}) = 1 - \cos(e_{adv}, e_{pos}) \)
    *   **独特特征保留损失 (\( L_{dist} \))**：通过一个孪生语义网络 \( S_{dist} \)，将嵌入分解为“通用”和“独特”两部分。该损失惩罚 \( e_{adv} \) 的独特部分与原始图像嵌入的独特部分 \( e_{target}^{(dist)} \) 之间的 L2 距离，确保图像身份不丢失。
        *   \( L_{dist}(e_{adv}, e_{target}^{(dist)}) = \| S_{dist}(e_{adv})[1] - e_{target}^{(dist)} \|_2^2 \)
    *   **感知相似性损失 (\( L_{LPIPS} \))**：通过一个可微分的解码流水线，将优化后的嵌入解码成候选图像 \( x_{cand} \)，并计算其与原始图像的 LPIPS 分数，以保证视觉上的逼真度。
        *   此过程中，一个由布局生成器 \( L \) 和分割模型（如DeepLabv3）结合产出的空间掩码 \( A_{final} \) 会被用于调制嵌入的“通用”部分，精确定位可编辑的区域。
    *   **最终解码**：优化完成后，使用最终的对抗性嵌入 \( e^*_{adv} \)，通过稳定扩散模型（Stable Diffusion）解码并生成最终的对抗性图像 \( x_{adv} \)。

### 3.  实验设计
*   **数据集与场景**：
    *   **主数据集**：微软 COCO Captions 数据集，从中抽取 100 组图像-文本对，构建多候选决策场景。
    *   **额外数据集**：为测试泛化能力，还在 `Flickr8k_sketch` 和 `ArtCapt` 数据集上进行了评估。
    *   **任务场景**：构建了一个黑盒的 N 路选择任务，模拟智能体（如电商代理）在多个候选图像中进行选择的情景。每个测试案例都从一个“坏图像”（初始选择概率低）开始。
*   **评估基准（Benchmark）与方法对比**：
    *   **核心指标**：攻击成功率（ASR），即经优化的对抗性图像获得超过 1/n 多数票的实例百分比。
    *   **对比方法**：
        1.  **传统攻击基线**：SPSA（黑盒攻击）、Bandit（黑盒攻击）。
        2.  **生成式基线**：标准 Stable Diffusion 重生成（未经优化）。
        3.  **嵌入空间攻击基线**：SSA_CWA、SA_AET。
    *   **被评估的受害者模型**：覆盖了六种主流的开源与闭源视觉-语言模型：LLaVA-1.5-34B、Gemma3-8B、Mistral-small-3.1/3.2-24B、GPT-4o、CogVLM。
    *   **防御评估**：评估了TRAP在面对高斯噪声、标题级过滤器（CIDER、MirrorCheck）以及对抗性训练模型（Robust-LLaVA）时的鲁棒性。

### 4.  资源与算力
*   **硬件配置**：服务器搭载 4 块 NVIDIA A100-PCIE-40GB GPU 和一颗 48 核的 Intel Xeon Silver 4214R CPU。
*   **运行时成本**：TRAP 的平均每次迭代优化耗时约 520 秒。作为对比，SPSA 约 376 秒，Bandit 约 110 秒。TRAP 是计算成本最高的方法。

### 5.  实验数量与充分性
*   **实验数量**：论文覆盖了较为广泛的实验，包括：
    1.  **主实验**：在单个 COCO 数据集上对 6 种模型、5 种基线方法的成功率对比。
    2.  **鲁棒性实验**：对 5 种防御/扰动策略下的攻击效果进行评估。
    3.  **泛化实验**：在 2 个额外数据集（Flickr8k_sketch, ArtCapt）上进行评估。
    4.  **消融实验**：对优化目标中不同损失项的权重、迭代次数、不同的嵌入模型（ViT-B/32, SigLIP, Jina-CLIP）以及不同的扩散生成器（SD1.5, SD2.1, SDXL）进行了消融研究。
    5.  **场景模拟**：模拟了更真实的电子商务网页场景下的攻击效果。
    6.  **稳定性实验**：分析了不同的系统提示词和采样温度对攻击成功率的影响。
*   **充分性与客观性**：实验设计是充分的。它不仅在标准数据集上与多种基线方法进行了对比，还全面评估了攻击的鲁棒性、泛化性、稳定性以及在不同组件下的表现，覆盖了真实应用场景。对比公平，评估模型涵盖开源和闭源，且使用了统一的评估协议。

### 6.  论文的主要结论与发现
*   **攻击有效性**：TRAP 在所有评估的视觉-语言模型上均实现了100%或接近100%的攻击成功率，性能远超所有传统像素级攻击和标准扩散方法基线。
*   **漏洞普遍性**：该攻击成功暴露了一个关键的、普遍的漏洞：自主智能体可以被视觉上细微、语义引导的跨模态操作持续误导。即使是GPT-4o这样的闭源模型也未能幸免。
*   **攻击鲁棒性**：TRAP 生成的攻击对采样温度、系统提示词的变化、高斯噪声具有鲁棒性，并能部分抵抗现有的文本级防御措施（如CIDER）和对抗性训练。
*   **防御号召**：研究结果强调，迫切需要超出像素级鲁棒性的防御策略，以应对跨模态决策中的语义漏洞。

### 7.  优点
*   **新颖的攻击范式**：从像素级扰动转向语义嵌入空间操纵，实现了更隐蔽、视觉自然且可转移的攻击。
*   **全面的方法设计**：巧妙融合了孪生网络、空间掩码和感知损失等多种技术，在保证语义转移的同时维护了图像的真实感和身份特征。
*   **实验评估极其全面**：涵盖了多个主流开源与闭源模型、多种基线方法、不同数据集、多种防御/干扰测试以及全面的消融实验，结论非常扎实。
*   **高现实威胁性**：在黑盒设定下工作，不需要访问模型内部，且生成的图像视觉自然，能绕过基本的哈希检测，模拟了真实的攻击场景。

### 8.  不足与局限
*   **计算开销高昂**：TRAP 依赖迭代优化和扩散模型的解码过程，单次攻击耗时较长（约520秒/迭代），远高于传统攻击方法，限制了其在实时场景中的应用。
*   **对模型架构的假设**：该攻击的一个核心前提是智能体依赖于对比式的视觉-语言相似度度量。对于未来完全不采用此类推理范式的系统，攻击有效性可能会下降。
*   **组件依赖性**：攻击效果依赖于辅助组件（如布局掩码生成、扩散模型）的质量，在极端或资源受限的情况下性能可能退化。
*   **防御机制仍在发展**：虽然有评估，但并未证明TRAP能攻破所有可能的、更先进的语义级防御。

（完）
