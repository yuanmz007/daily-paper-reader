---
title: "HQA-VLAttack: Towards High Quality Adversarial Attack on Vision-Language Pre-Trained Models"
title_zh: "HQA-VLAttack: 面向视觉语言预训练模型的高质量对抗攻击"
authors: "Han Liu, Jiaqi Li, Zhi Xu, Xiaotong Zhang, Xiaoming Xu, Fenglong Ma, Yuanman Li, Hong Yu"
date: 2025-09-18
pdf: "https://openreview.net/pdf?id=LZ4IKybwWl"
tags: ["query:sem-vis-atk"]
score: 5.0
evidence: 对视觉语言预训练模型的对抗攻击
tldr: HQA-VLAttack针对视觉语言预训练模型的黑盒攻击，提出一种简单有效的框架，通过同时考虑正负图像-文本对相似度，生成高质量对抗样本，在降低查询成本的同时保持攻击效果。
source: NeurIPS-2025-Accepted
selection_source: conference_retrieval
figures_json: "[{\"url\": \"assets/figures/openreview/openreview-neurips-2025-lz4ikybwwl/fig-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 626, \"height\": 461, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-lz4ikybwwl/fig-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1352, \"height\": 642, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-lz4ikybwwl/fig-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 627, \"height\": 478, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-lz4ikybwwl/fig-004.webp\", \"caption\": \"\", \"page\": 0, \"index\": 4, \"width\": 800, \"height\": 456, \"label\": \"Figure\"}, {\"url\": \"assets/figures/openreview/openreview-neurips-2025-lz4ikybwwl/fig-005.webp\", \"caption\": \"\", \"page\": 0, \"index\": 5, \"width\": 1279, \"height\": 1142, \"label\": \"Figure\"}]"
tables_json: "[{\"url\": \"assets/tables/openreview/openreview-neurips-2025-lz4ikybwwl/table-001.webp\", \"caption\": \"\", \"page\": 0, \"index\": 1, \"width\": 1446, \"height\": 957, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-lz4ikybwwl/table-002.webp\", \"caption\": \"\", \"page\": 0, \"index\": 2, \"width\": 1445, \"height\": 956, \"label\": \"Table\"}, {\"url\": \"assets/tables/openreview/openreview-neurips-2025-lz4ikybwwl/table-003.webp\", \"caption\": \"\", \"page\": 0, \"index\": 3, \"width\": 1450, \"height\": 236, \"label\": \"Table\"}]"
motivation: 现有黑盒攻击方法查询成本高或忽视负样本对，制约攻击性能。
method: 提出HQA-VLAttack框架，平衡正负对相似度以生成高质量对抗样本。
result: 实验表明该方法在攻击成功率和查询效率上优于现有方法。
conclusion: 为视觉语言预训练模型的安全评估提供了新的高效攻击手段。
---

## Abstract
Black-box adversarial attack on vision-language pre-trained models is a practical and challenging task, as text and image perturbations need to be considered simultaneously, and only the predicted results are accessible. Research on this problem is in its infancy, and only a handful of methods are available. Nevertheless, existing methods either rely on a complex iterative cross-search strategy, which inevitably consumes numerous queries, or only consider reducing the similarity of positive image-text pairs but ignore that of negative ones, which will also be implicitly diminished, thus inevitably affecting the attack performance. To alleviate the above issues, we propose a simple yet effective framework to generate high-quality adversarial examples on vision-language pre-trained models, named HQA-VLAttack, which consists of text and image attack stages. For text perturbation generation, it leverages the counter-fitting word vector to generate the substitute word set, thus guaranteeing the semantic consistency between the substitute word and the original word. For image perturbation generation, it first initializes the image adversarial example via the layer-importance guided strategy, and then utilizes contrastive learning to optimize the image adversarial perturbation, which ensures that the similarity of positive image-text pairs is decreased while that of negative image-text pairs is increased. In this way, the optimized adversarial images and texts are more likely to retrieve negative examples, thereby enhancing the attack success rate. Experimental results on three benchmark datasets demonstrate that HQA-VLAttack significantly outperforms strong baselines in terms of attack success rate.

---

## 论文详细总结（自动生成）

### 1. 论文的核心问题与整体含义
- **研究背景**：视觉语言预训练模型（VLP）广泛应用于跨模态任务，但易受对抗攻击。黑盒攻击更具实际威胁，但现有方法存在两大缺陷：
  - 查询式攻击依赖大量查询，成本高；
  - 迁移式攻击（如 SGA、DRA）主要关注降低正图像-文本对的相似度，忽略负图像-文本对的相似度也会间接下降，导致检索仍偏向正样本，限制攻击成功率。
- **核心目标**：提出一个简单、高效、高质量的迁移式黑盒对抗攻击框架 **HQA‑VLAttack**，在无查询的条件下，同时操控正负图像-文本对的相似度，显著提升攻击成功率。

### 2. 方法论
- **整体框架**：分为 **文本攻击** 和 **图像攻击** 两个阶段，在替代模型上生成对抗样本后直接迁移到目标模型。
- **文本攻击**
  - 使用 **counter‑fitting 词向量** 构造语义一致的替代词集，避免传统 MLM 方法可能产生语义矛盾。
  - 对每个单词，从替代词集中选择使文本与对应图像的余弦相似度最低的单个替换，生成对抗文本 \(t_i'\)。
- **图像攻击**
  - **层重要性引导的初始对抗图像生成**：基于各层对最终输出的影响不同，利用 [CLS] token 在顶层与第 \(l\) 层的余弦相似度作为层重要性权重 \(w_{i,l}\)，然后通过最小化各层特征的加权余弦相似度，用 PGD 生成初始对抗图像 \(v_i'\)。
  - **对比学习优化**：在初始对抗图像的基础上，设计损失函数：
    \[
    L_c = \sum_{v^*_i \in \text{Trans}(v_i')} \left( \lambda \sum_{t_i'\in T_p} \cos(\cdot) + \sum_{t_j'\in T_n} \cos(\cdot) \right)
    \]
    - 对 **正文本对** (\(T_p\)) 施加惩罚因子 \(\lambda\)，最小化相似度（即排斥）；
    - 对批次内的 **负文本对** (\(T_n\)) 最大化相似度（即吸引）。
    - 同时使用尺度变换增强迁移性。优化后，对抗图像更可能检索到负样本文本，提升攻击成功率。
- **整体流程**：交替进行文本攻击和图像攻击，在替代模型上生成优化后的对抗集 \(D'_v, D'_t\)。

### 3. 实验设计
- **数据集**：
  - Flickr30K (1k 图像，5k 文本)
  - MSCOCO (5k 图像，约 25k 文本)
  - RefCOCO+ (3k 图像，15k 文本)
- **任务与场景**：
  - **图像-文本检索（ITR）**：跨架构、跨模型的黑盒迁移攻击（如 ALBEF→TCL，ALBEF→CLIPViT 等）；
  - **跨任务攻击**：将 ITR 对抗样本迁移到视觉定位（VG）和图像描述（IC）。
- **对比方法**：PGD、BERT‑Attack、Sep‑Attack、Co‑Attack、SGA、DRA（涵盖白盒、查询式黑盒、迁移式黑盒）。
- **评估指标**：攻击成功率（ASR），以 R@1 为主要指标，还报告 R@5、R@10；跨任务使用 Val/TestA/TestB 降低值以及 BLEU、CIDEr 等。

### 4. 资源与算力
- 文中未明确给出 GPU 型号、数量、训练时长或具体计算资源消耗。仅提到“We list the detailed computer resources In Appendix F”，但附录未提供。无法从现有文本中获知算力信息。

### 5. 实验数量与充分性
- **主要实验**：
  - 在 **两个检索数据集** 上，对 **4 种替代模型 × 4 种目标模型** 组合进行黑盒攻击，共 16 组×2 数据集 ≈ 32 组大实验（表1、表2）；
  - **跨任务实验**：ALBEF 生成对抗样本攻击 VG 和 IC（表3）；
  - **消融实验**：模块有效性（去除 counter‑fitting、层重要性、初始生成、对比优化）和 batch size 的影响（图4a、4b）；
  - 参数敏感性实验（附录F，λ 影响）。
- **公平性**：采用与 SGA 相同的扰动约束（ϵv=2/255，ϵt=1）、迭代次数、输入变换等设置，对比基线涵盖主流方法，实验公平。
- **充分性**：覆盖多个架构、数据集和任务，包含模块消融和超参数分析，实验设计较全面。

### 6. 主要结论与发现
- HQA‑VLAttack 在 **白盒** 场景下达到近乎 100% 攻击成功率。
- 在 **黑盒迁移** 中，较现有最优方法大幅提升：如 ALBEF→TCL 在 Flickr30K 上 TR 提升 23.28%，IR 提升 18.77%；跨架构迁移同样显著领先。
- 跨任务（视觉定位、图像描述）也明显超越 SGA、DRA 等，验证了攻击方法的广泛有效性。
- 同时操控正负图像-文本对相似度、引入层重要性初始化和对比学习是攻击成功的关键。

### 7. 优点
- **创新性**：首次在 VLP 迁移攻击中显式优化负对相似度，解决了现有方法忽视负对的缺陷。
- **高质量攻击**：无查询、高成功率，显著优于 SOTA。
- **模块设计合理**：counter‑fitting 保证文本语义一致性；层重要性引导初始化提升攻击与迁移的平衡；对比学习驱动正负对分离。
- **实验丰富**：涵盖不同模型架构、多个数据集和下游任务，消融与分析充分。

### 8. 不足与局限
- **计算资源未披露**：未说明 GPU、时间等成本，影响复现与实用性评估。
- **扰动限制固定**：仅测试 ϵv=2/255，对其他扰动上限的鲁棒性未知。
- **模型覆盖有限**：主要针对 ALBEF、TCL、CLIP 等，未验证在其他 VLP 模型（如 BLIP‑2、Flamingo）上的迁移性。
- **语义一致性依赖外部词向量**：counter‑fitting 词向量可能无法覆盖所有词汇，且阈值 τ 影响显著。
- **仅考虑单次替换**：文本攻击每次只替换一个词，对于较长文本可能攻击强度不足。
- **负样本选择受批次限制**：负样本对来自同一批次，可能不够多样，影响对比学习效果。

（完）
