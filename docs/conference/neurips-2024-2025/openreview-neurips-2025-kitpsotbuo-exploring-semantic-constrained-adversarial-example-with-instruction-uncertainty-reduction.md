---
title: Exploring Semantic-constrained Adversarial  Example with Instruction Uncertainty Reduction
title_zh: 探索基于指令不确定性降低的语义约束对抗样本
authors: "Jin Hu, Jiakai Wang, linna Jing, Haolin Li, Haodong Liu, Haotong Qin, Aishan Liu, Ke Xu, Xianglong Liu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=kITPSoTBUo"
tags: ["query:sem-vis-atk"]
score: 9.0
evidence: "从自然语言指令生成语义约束对抗样本, 通过多维度不确定性降低提升攻击性"
tldr: "本文针对从自然语言指令生成语义约束对抗样本(SemanticAE)任务, 提出多维指令不确定性降低框架InSUR, 解决指令中的指代多样性、描述不完整性和边界模糊性等关键因素, 显著提升攻击能力, 为语义级对抗攻击提供了新方法论。"
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 462, \"height\": 413, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1419, \"height\": 596, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 288, \"height\": 285, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 1098, \"height\": 290, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1287, \"height\": 327, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1418, \"height\": 234, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 708, \"height\": 345, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 710, \"height\": 346, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 540, \"height\": 396, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 702, \"height\": 153, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 916, \"height\": 642, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-012.webp\", \"caption\": \"\", \"page\": 0, \"index\": 12, \"width\": 509, \"height\": 627, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-013.webp\", \"caption\": \"\", \"page\": 0, \"index\": 13, \"width\": 574, \"height\": 324, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-014.webp\", \"caption\": \"\", \"page\": 0, \"index\": 14, \"width\": 1092, \"height\": 760, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-015.webp\", \"caption\": \"\", \"page\": 0, \"index\": 15, \"width\": 1171, \"height\": 662, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-016.webp\", \"caption\": \"\", \"page\": 0, \"index\": 16, \"width\": 693, \"height\": 350, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-017.webp\", \"caption\": \"\", \"page\": 0, \"index\": 17, \"width\": 691, \"height\": 351, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-018.webp\", \"caption\": \"\", \"page\": 0, \"index\": 18, \"width\": 1143, \"height\": 565, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-019.webp\", \"caption\": \"\", \"page\": 0, \"index\": 19, \"width\": 1449, \"height\": 1821, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-020.webp\", \"caption\": \"\", \"page\": 0, \"index\": 20, \"width\": 1448, \"height\": 1825, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-021.webp\", \"caption\": \"\", \"page\": 0, \"index\": 21, \"width\": 1447, \"height\": 1819, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-022.webp\", \"caption\": \"\", \"page\": 0, \"index\": 22, \"width\": 1446, \"height\": 1819, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-023.webp\", \"caption\": \"\", \"page\": 0, \"index\": 23, \"width\": 1449, \"height\": 1817, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-024.webp\", \"caption\": \"\", \"page\": 0, \"index\": 24, \"width\": 1451, \"height\": 1813, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-025.webp\", \"caption\": \"\", \"page\": 0, \"index\": 25, \"width\": 1086, \"height\": 2255, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-026.webp\", \"caption\": \"\", \"page\": 0, \"index\": 26, \"width\": 1095, \"height\": 2247, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-027.webp\", \"caption\": \"\", \"page\": 0, \"index\": 27, \"width\": 672, \"height\": 143, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-028.webp\", \"caption\": \"\", \"page\": 0, \"index\": 28, \"width\": 691, \"height\": 144, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-029.webp\", \"caption\": \"\", \"page\": 0, \"index\": 29, \"width\": 705, \"height\": 161, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-030.webp\", \"caption\": \"\", \"page\": 0, \"index\": 30, \"width\": 703, \"height\": 159, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-031.webp\", \"caption\": \"\", \"page\": 0, \"index\": 31, \"width\": 717, \"height\": 141, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-032.webp\", \"caption\": \"\", \"page\": 0, \"index\": 32, \"width\": 701, \"height\": 142, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-kitpsotbuo/fig-033.webp\", \"caption\": \"\", \"page\": 0, \"index\": 33, \"width\": 702, \"height\": 139, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-kitpsotbuo/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1443, \"height\": 645, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kitpsotbuo/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 656, \"height\": 161, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kitpsotbuo/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 867, \"height\": 551, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kitpsotbuo/table-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 724, \"height\": 223, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kitpsotbuo/table-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1434, \"height\": 176, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kitpsotbuo/table-006.webp\", \"caption\": \"\", \"page\": 0, \"index\": 6, \"width\": 1437, \"height\": 201, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kitpsotbuo/table-007.webp\", \"caption\": \"\", \"page\": 0, \"index\": 7, \"width\": 1172, \"height\": 334, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kitpsotbuo/table-008.webp\", \"caption\": \"\", \"page\": 0, \"index\": 8, \"width\": 1383, \"height\": 175, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kitpsotbuo/table-009.webp\", \"caption\": \"\", \"page\": 0, \"index\": 9, \"width\": 1387, \"height\": 2220, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kitpsotbuo/table-010.webp\", \"caption\": \"\", \"page\": 0, \"index\": 10, \"width\": 855, \"height\": 2381, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-kitpsotbuo/table-011.webp\", \"caption\": \"\", \"page\": 0, \"index\": 11, \"width\": 885, \"height\": 2376, \"label\": \"Table\"}]"
motivation: "现有语义对抗样本生成方法对指令语义不确定性利用不足, 攻击能力有限。"
method: "提出InSUR框架, 通过降低指代多样性、描述不完整性、边界模糊性等多维不确定性来生成更强攻击性样本。"
result: "生成的语义对抗样本在攻击成功率上显著超越现有方法, 验证了指令不确定性降低的有效性。"
conclusion: "为灵活且可控的语义对抗攻击拓展了研究空间, 并揭示了指令语义不确定性在攻击中的关键作用。"
---

## Abstract
Recently, semantically constrained adversarial examples (SemanticAE), which are directly generated from natural language instructions, have become a promising avenue for future research due to their flexible attacking forms, but have not been thoroughly explored yet.
To generate SemanticAEs, current methods fall short of satisfactory attacking ability as the key underlying factors of semantic uncertainty in human instructions, such as $\textit{referring diversity}$, $\textit{descriptive incompleteness}$, and $\textit{boundary ambiguity}$, have not been fully investigated.
To tackle the issues, this paper develops a multi-dimensional $\textbf{ins}$truction $\textbf{u}$ncertainty $\textbf{r}$eduction ($\textbf{InSUR}$) framework to generate more satisfactory SemanticAE, $\textit{i.e.}$, transferable, adaptive, and effective.
Specifically, in the dimension of the sampling method, we propose the residual-driven attacking direction stabilization to alleviate the unstable adversarial optimization caused by the diversity of language references.
By coarsely predicting the language-guided sampling process, the optimization process will be stabilized by the designed ResAdv-DDIM sampler‌, therefore releasing the transferable and robust adversarial capability of multi-step diffusion models.
In task modeling, we propose the context-encoded attacking scenario constraint to supplement the missing knowledge from incomplete human instructions.
Guidance masking and renderer integration are proposed to regulate the constraints of 2D/3D SemanticAE, activating stronger scenario-adapted attacks.
Moreover, in the dimension of generator evaluation, we propose the semantic-abstracted attacking evaluation enhancement by clarifying the evaluation boundary based on the label taxonomy, facilitating the development of more effective SemanticAE generators.
Extensive experiments demonstrate the superiority of the transfer attack performance of InSUR.
Besides, it is worth highlighting that we realize the reference-free generation of semantically constrained 3D adversarial examples by utilizing language-guided 3D generation models for the first time.

---

## 论文详细总结（自动生成）

# 论文总结：基于指令不确定性降低的语义约束对抗样本生成

## 1. 论文的核心问题与整体含义
- **研究背景**：对抗样本（Adversarial Example）研究大多围绕已有数据进行扰动，而直接从自然语言指令生成语义约束的对抗样本（Semantic‑constrained Adversarial Example，**SemanticAE**）尚处于早期探索阶段。这类对抗样本由文本描述直接定义其合法语义范围，具有灵活的攻击形式，但攻击能力仍不令人满意。
- **核心问题**：当前生成SemanticAE的关键瓶颈在于**人类指令中内在的语义不确定性**未被充分建模和消除。论文将这种不确定性归纳为三种形式：
  - **指代多样性（Referring Diversity）**：同一语义下语言表述的多样性导致对抗优化过程中与扩散模型的协作不稳定。
  - **描述不完整性（Descriptive Incompleteness）**：用户指令往往不能精确刻画攻击场景，限制了场景自适应攻击的生成。
  - **边界模糊性（Boundary Ambiguity）**：语义约束的边界难以在任务定义中精确刻画，影响生成器的公平评估。
- **整体含义**：本文旨在从**多维度降低指令不确定性**，生成更具**可迁移性、自适应性和有效性**的语义对抗样本，推动语言驱动的对抗攻击及红队测试框架的发展。

## 2. 论文提出的方法论：InSUR 框架
论文提出**多维度指令不确定性降低（Instruction Uncertainty Reduction，InSUR）**框架，包含三个关键技术模块。

### 2.1 残差驱动的攻击方向稳定化（ResAdv‑DDIM 采样器）
- **动机**：多步扩散模型与对抗优化协作时，因语言引导的非线性导致不同步的对抗梯度方向不一致，限制了可迁移性。
- **核心思想**：利用扩散模型固有的多步去噪能力，从当前时刻 \(x_t\) 粗糙预测最终去噪结果 \(x_0\)（即 \(g_\theta(x_t)\)），以此估计更准确的攻击损失梯度 \(\nabla_{x_t} L_{\text{ATK}}\)，从而稳定优化方向。
- **实现方式**：设计 **ResAdv‑DDIM** 后验采样器。在去噪过程中，当时间步 \(t\) 小于一定阈值 \(t_s\) 时，执行如下步骤：
  1. 使用少量大步长的 DDIM 步骤跳跃式预估 \(x_0\)（残差捷径）。
  2. 在该预估结果上计算对抗损失，并用动量更新 \(x_t\)。
  3. 通过约束与纯 DDIM 采样轨迹的 \(l_2\) 距离（\(\epsilon\)）保证语义不偏离。
  4. 引入**自适应迭代机制**，根据当前攻击成功率估计提前终止优化，提升效率。
- **效果**：使早期去噪步即可获得有效对抗优化，加强多步正则，生成更可迁移且鲁棒的对抗模式。

### 2.2 上下文编码的攻击场景约束
针对**描述不完整性**，分别对 2D 和 3D 场景设计知识嵌入策略。
- **2D 场景**：提出**引导掩码（Guidance Masking）** 技术。将原始单一的条件引导重新分布为空间上的多重引导（如边缘区域降低条件引导权重），丰富背景生成多样性，同时保持前景语义。在 ResAdv‑DDIM 的采样和对抗优化中均使用掩码控制的噪声估计。
- **3D 场景**：首次实现纯文本驱动的 3D 语义对抗样本生成。通过在 **Trellis** 框架中集成**可微分高斯渲染（Gaussian Splatting）**，将 3D 生成与 2D 目标模型桥接。对抗优化时，对渲染过程应用期望‑变换（EoT）策略，随机采样相机视角以累积梯度，同时利用 ResAdv‑DDIM 将前步梯度重用于当前步，减少 EoT 步数。

### 2.3 语义抽象的攻击评估增强
为解决**边界模糊性**，设计更合理的评价体系。
- **攻击目标抽象化**：基于 WordNet 的词义层级（Hyponym）构建抽象标签，将攻击任务从「将 `tiger‑shark` 错分为 `great‑white‑shark`」提升为「将 `great‑white‑shark` 错分为非 `shark` 的抽象类别」，更贴近真实攻击场景。
- **非对抗样本辅助评估**：要求生成器同时输出一个对抗样本 \(x_{\text{adv}}\) 和一个语义一致的邻近样本 \(x_{\text{exemplar}}\)。使用**相对攻击成功率（ASR$_{\text{Relative}}$）**：仅当 \(x_{\text{exemplar}}\) 被正确分类时才计入 \(x_{\text{adv}}\) 的攻击成败，并配合成对相似度指标评价语义一致性，避免攻击语义评估模型本身带来的偏差。

## 3. 实验设计
### 3.1 数据集与任务
- **2D 任务**：ImageNet‑1K 的原始标签逃避任务，以及基于 WordNet 构建的**抽象标签逃避任务**（将 ImageNet 细粒度标签归入高层语义类别，如狗、鸟等）。文本提示为 `“Realistic image of [AbstractedLabel] , specifically , [label]”`。
- **3D 任务**：同样基于抽象标签，通过 TRELLIS 生成 3D 物体，再渲染为视频帧评估。攻击目标为 ResNet50。

### 3.2 对比基准与目标模型
- **生成方法**：MI‑FGSM、DeCoWA ；基于扩散模型的 AdvDiff、SD‑NAE、VENOM。均接入相同的预训练扩散模型。
- **目标模型**（用于评估可迁移性）：ResNet50、ViT‑B/16、ConvNeXt‑T、ResNet152、InceptionV3、Swin‑B。前三者亦轮流作为代理模型。
- **额外代理设置**：ResNet50 + DeCoWA（输入变换增强）考察与现有迁移技术的兼容性。

### 3.3 评价指标
- **攻击性能**：准确率（ACC）、攻击成功率（ASR）、相对攻击成功率（ASR$_{\text{Relative}}$）。
- **语义相似度**：LPIPS、MS‑SSIM（成对比较）；无参考质量分 CLIP‑IQA。
- **生成时间**：单样本平均生成时长（4090 / A800 GPU）。

## 4. 资源与算力
- 2D 生成实验在 **单块 NVIDIA RTX 4090** 上进行，3D 生成使用 **单块 A800 GPU**。文中未报告训练过程（方法无需额外训练），仅给出了不同方法生成 100 个样本的平均时间与标准差，其中 InSUR 的 2D 生成时间约为 4.5 ~ 11.5 秒/样本，3D 约为 30 ~ 40 秒/样本（因自适应步数而异）。

## 5. 实验数量与充分性
- **主要对比实验**：4 种代理模型 × 2 种任务（原始标签、抽象标签）下的多方法对比，每种设置生成 100 个样本，计算各模型上的平均 ASR、ACC 和视觉质量指标。通过调整约束强度 \(\epsilon\) 展示 Pareto 前沿。
- **消融实验**：
  - 残差近似步数 \(K\) 的影响（0~4）；
  - 引导掩码不同参数的作用；
  - 3D 中 EoT 步数与残差近似的协同。
- **鲁棒性分析**：测试对抗防御（JPEG 压缩、DiffPure）下的表现。
- **扩展实验**：攻击大型视觉语言模型（CLIP 系列及 LLaVa、Qwen），验证方法泛化性。
- **整体评估**：实验覆盖全面，从多维度验证了各模块的增益，对比公平（统一扩散模型基座和评估协议），且提供了详细的方差分析，**充分性与客观性较好**。

## 6. 主要结论与发现
1. **InSUR 框架在几乎全部 2D/3D 设置中实现了更优的攻击可迁移性**：在同等的语义失真（LPIPS）下，ASR 至少提升 1.19 倍，且在各种代理‑目标组合中均保持优势。
2. **ResAdv‑DDIM 有效解决优化方向不一致**：通过粗糙预测 \(x_0\)，使早期采样步的对抗方向更准确，既提升攻击性能又改善生成图像的自然度。
3. **场景知识编码成功弥补指令描述不足**：引导掩码丰富了背景对抗模式，3D 渲染集成打通了文本驱动 3D 攻击的链路。
4. **抽象标签评估更贴合真实攻击场景**，非对抗样本评估（ASR$_{\text{Relative}}$）避免了语义评价器自身被攻击带来的评分失真。
5. **首次实现纯语言引导的 3D 语义对抗样本生成**，并展示了在光照、材质等变化下的鲁棒性潜力。

## 7. 优点
- **问题定义新颖且系统**：首次将指令不确定性细分为三种类型，并提出针对性解决方案。
- **方法论扎实**：ResAdv‑DDIM 巧妙利用扩散模型自身预测能力稳定对抗优化；上下文编码技术同时覆盖 2D 和 3D。
- **评估体系完善**：创新性地提出抽象标签任务和相对攻击成功率，缓解了评估困境。
- **实验全面且具有说服力**：包括多代理、多目标、多任务、多防御、消融和扩展至 VLM 的实验，且提供了生成时间等实际效率指标。
- **开源与可复现**：算法细节和伪代码公开，且未涉及额外训练，易于复现。

## 8. 不足与局限
- **生成质量仍有提升空间**：高约束强度下可能出现模糊等伪影，且 3D 任务的干净样本准确率本身不高，限制了攻击上限。
- **对大型模型的验证有限**：虽测试了部分 VLM，但未在更大规模的扩散模型或更复杂的现实任务上全面评估。
- **物理世界部署欠缺**：3D 攻击仅限于虚拟渲染，尚未在实际拍摄条件下验证；且未涉及动态遮挡、光照等极端现实变化。
- **自适应攻击的覆盖率**：上下文场景约束依赖预定义的掩码和渲染设置，对完全开放场景的适应性仍需进一步研究。

（完）
