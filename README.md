# 科研入门学习指南

## 学习目标

本学习指南面向刚开始接触科研的本科生和研究生，希望帮助同学逐步掌握编程、信息检索、论文阅读和代码实践等基本能力，并对本研究小组的方向形成初步认识。

这一阶段的重点是学会如何学习、如何开展科研：主动查找资料、理解论文与代码、设计实验、分析结果和解决问题。不同方向的具体知识需要继续积累，但学习方法和科研思路有很多相通之处；掌握这些能力后，就能更从容地进入新的研究方向。

> 本指南中的资料主要用于提供学习入口，遇到不懂的问题时，应主动搜索、阅读文档并动手实践。

**学习建议**：

1. 查找论文和技术资料时，建议优先使用 [Google](https://www.google.com/)；
2. 建议同学们学会使用 [ChatGPT](https://chatgpt.com/)、[Codex](https://learn.chatgpt.com/docs/codex/cli) 或 [Claude Code](https://claude.com/product/claude-code) 等工具辅助学习与实践；
3. 建议持续维护一份自己的线上学习笔记，记录知识、问题和解决过程；
4. 遇到不懂的问题时，可以先用 [Google](https://www.google.com/) 检索资料、在 [Bilibili](https://www.bilibili.com/) 查找教程，再带着具体问题向同学或老师请教，主动学习并尝试解决。

---

## 科研思路与基本习惯

在学习具体知识之前，应先建立主动检索、独立判断和动手验证的习惯。工具可以提高效率，但真正重要的是发现问题、理解问题并验证结论的能力。

### 1. 善用 AI，但不要依赖 AI

[ChatGPT](https://chatgpt.com/)、[Codex](https://learn.chatgpt.com/docs/codex/cli)、[Claude Code](https://claude.com/product/claude-code) 可以辅助学习、编程和科研，但不能代替独立思考，也不能保证所有回答都正确。

* 可以使用 [ChatGPT](https://chatgpt.com/) 解释概念、比较方法、辅助阅读论文、整理思路和检查文字表达；
* 可以使用 [Codex](https://learn.chatgpt.com/docs/codex/cli) 阅读代码仓库、梳理程序流程、修改代码、定位报错，也可以辅助完成论文复现和论文撰写；
* AI 有时会为了“完成任务”而采取捷径，例如忽略失败样本、弱化检查条件、生成冗余代码，甚至让实验结果看起来虚高；
* 应仔细检查 AI 生成的代码、实验日志和原始结果，对重要事实和论文结论，应回到原始资料核对；
* 面对复杂任务时，应将任务拆分成若干小步骤，逐步完成、逐步检查。

#### 使用 Codex 辅助科研和编程

可以在 VS Code 中安装 Codex 扩展，也可以在桌面端或终端中使用。使用过程中，应逐渐形成适合自己的任务描述和检查习惯，并将长期有效的项目约定写入 `AGENTS.md`。

Codex 还支持使用 [Skill](https://learn.chatgpt.com/docs/build-skills) 保存和复用特定工作流程。Skill 并非越多越好：如果某个 Skill 不适合当前任务或经常带来冗余步骤，应及时停用或删除，避免增加不必要的上下文和 Token 消耗。

### 2. 主动检索，并学会判断资料质量

科研初期应广泛阅读文献，避免过早将视野局限于某个具体方法。遇到陌生概念、代码报错或新的研究问题时，应主动检索资料，可以从 [Google](https://www.google.com/)、[Bilibili](https://www.bilibili.com/)、[知乎](https://www.zhihu.com/)、[小红书](https://www.xiaohongshu.com/)等渠道寻找线索。

* 使用 [Google](https://www.google.com/) 搜索论文、官方文档、代码仓库，以及相关学者和实验室的主页；
* 使用 [Google Scholar](https://scholar.google.com/) 检索学术论文，结合论文的参考文献和“被引用”列表，梳理前期工作与后续进展；
* 使用 [Bilibili](https://www.bilibili.com/) 上的中文课程、论文讲解和技术分享快速建立直观认识；
* [小红书](https://www.xiaohongshu.com/)和微信公众号上的研究分享也可以作为发现论文的入口，感兴趣的内容应进一步查阅原论文；
* 在确定具体研究问题时，应寻找可供参考的基线方法（baseline），了解其数据集、评价指标、实验设置和对比结果，提前规划自己的实验。优先关注近一年内的相关工作，同时保留有代表性的经典基线。

阅读论文时，应优先关注领域内的顶级会议、顶级期刊和具有代表性的工作。例如：

* 综合机器学习：NeurIPS、ICML、ICLR、AAAI；
* 自然语言处理：ACL、EMNLP、NAACL、EACL；
* 计算机视觉：CVPR、ICCV、ECCV；
* 代表性期刊：JMLR、TPAMI、IJCV、TKDE 等。

论文的发表平台、引用量、作者及其研究单位、代码仓库的 Star 数量等都可以作为参考。选择复现论文时，还应关注代码和数据是否公开，以及现有算力能否支持。

### 3. 从一个大方向逐步进入具体问题

接触一个新的研究方向时，建议按照下面的思路逐步深入：

1. **阅读综述和典型论文**：使用“研究方向 + survey/review/tutorial”等关键词检索综述和教程。对于热门方向，也可以通过 [Bilibili](https://www.bilibili.com/)、[小红书](https://www.xiaohongshu.com/)等平台上的讨论建立直观认识，再结合综述和论文深入了解该方向的研究目标、常用数据集和评测指标；
2. **寻找感兴趣的问题**：结合现有方法的不足，寻找自己感兴趣的具体问题。可以在组内师兄师姐已有工作的基础上继续探索，也可以通过阅读论文寻找新问题，并与导师讨论研究的价值和可行性；
3. **深入阅读与实践**：围绕小方向继续检索论文，选择有公开代码的工作进行复现和分析，逐步形成系统而具体的认识。

对于发展很快的新方向，可以阅读 arXiv 上新的论文和技术报告，但应注意区分预印本和已经过同行评审的论文。

---

## 学习资料

每位同学的基础不同，可以根据已有知识和实践需要，有选择地学习以下内容，如果涉及方向选择可与我商量优先学习哪些。

### 1. Python 基础（可跳过）

Python 是人工智能领域常用的编程语言，应优先掌握。可以自行查找教程，先熟悉基本语法、常用数据结构和程序组织方式，学会配置运行环境、使用编程工具、运行代码并理解主要逻辑。入门阶段不必花大量时间钻研所有细节，可以在后续论文复现和实验中逐步查漏补缺。已有相关基础的同学可跳过这一部分。

**参考资料**：

* [Python 基础快速了解](https://www.bilibili.com/video/BV1KE421A7rV/)
* [廖雪峰 Python 教程](https://liaoxuefeng.com/books/python/introduction/)
* [菜鸟教程：Python 3 教程](https://www.runoob.com/python3/python3-tutorial.html)


### 2. 人工智能与大模型基础

#### 2.1 神经网络与深度学习基础

**学习目标**：理解神经网络、前向传播、反向传播和梯度下降的基本原理，了解 CNN、ResNet、RNN 等常见模型架构，并掌握 PyTorch 的核心组件，例如损失函数、模型和优化器等。

**参考资料**：

* [李沐-动手学深度学习](https://zh.d2l.ai/)-优先学习
* [李宏毅-深度学习教程](https://www.bilibili.com/video/BV122QRBcExF/)

李沐的读论文系列视频也非常好！推荐观看！

#### 2.2 大语言模型（LLMs）

**学习目标**：掌握 Transformer 的核心机制，包括 Self-Attention、Positional Encoding 等，理解 Decoder-only 与 Encoder-Decoder 架构的区别，并了解 GPT、LLaMA、Qwen 等典型大语言模型。

**参考资料**：

* [Happy-LLM (Datawhale)](https://datawhalechina.github.io/happy-llm/)-优先学习
* [Hugging Face LLM Course](https://huggingface.co/learn/llm-course/chapter1/1)
* [Stanford CS336: Language Modeling from Scratch](https://cs336.stanford.edu/)
* [Attention Is All You Need](https://arxiv.org/abs/1706.03762)
* [Large Language Models: A Survey](https://arxiv.org/abs/2402.06196)（2025 年更新，大语言模型综述）
* [Towards Large Reasoning Models: A Survey of Reinforced Reasoning with Large Language Models](https://arxiv.org/abs/2501.09686)（2025，大模型推理综述）
* [Towards Transparent AI: A Survey on Explainable Large Language Models](https://arxiv.org/abs/2506.21812)（2025，大模型可解释性综述）

#### 2.3 多模态大模型

**学习目标**：了解多模态大模型的基本原理。

**参考资料**：

* [Happy-LLM (Datawhale)](https://datawhalechina.github.io/happy-llm/)-优先学习
* 多模态大模型论文串讲：[上](https://www.bilibili.com/video/BV1Vd4y1v77v/)，[下](https://www.bilibili.com/video/BV1fA411Z772/)
* [Hugging Face：Vision Language Models 入门](https://huggingface.co/learn/computer-vision-course/en/unit4/multimodal-models/vlm-intro)
* [CLIP: Learning Transferable Visual Models From Natural Language Supervision](https://arxiv.org/abs/2103.00020)
* [BLIP-2: Bootstrapping Language-Image Pre-training](https://arxiv.org/abs/2301.12597)
* [LLaVA: Visual Instruction Tuning](https://arxiv.org/abs/2304.08485)
* [Qwen3-VL Technical Report](https://arxiv.org/abs/2511.21631)
* [Multimodal Large Language Models: A Survey](https://arxiv.org/abs/2506.10016)（2025，多模态大模型综述）
* [A Survey on Mechanistic Interpretability for Multi-Modal Foundation Models](https://arxiv.org/abs/2502.17516)（2025，多模态大模型可解释性综述）
* [Video-LMM Post-Training: A Deep Dive into Video Reasoning with Large Multimodal Models](https://arxiv.org/abs/2510.05034)（2025，多模态大模型视频理解与推理综述）

#### 2.4 智能体（Agent）

**学习目标**：理解大模型 Agent 的基本概念，了解 Agent 的工具使用、记忆、规划方法以及 Multi-Agent 系统的基本概念。

**参考资料**：

* [Hello-Agents](https://github.com/datawhalechina/hello-agents)-优先学习
* [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629)
* [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/)
* [Harness Engineering for Self-Improvement（Lilian Weng）](https://lilianweng.github.io/posts/2026-07-04-harness/)
* [Hugging Face Agents Course](https://huggingface.co/learn/agents-course/en/unit0/introduction)
* [Large Language Model Agent: A Survey on Methodology, Applications and Challenges](https://arxiv.org/abs/2503.21460)（2025，大模型智能体综述）
* [Multi-Agent Collaboration Mechanisms: A Survey of LLMs](https://arxiv.org/abs/2501.06322)（2025，多智能体协作综述）

#### 2.5 强化学习

**学习目标**：了解强化学习中的状态、动作、奖励和策略等基本概念，结合代码实践理解典型算法。

**参考资料**：

* [动手学强化学习：在线教程](https://hrl.boyuai.com/chapter/intro)
* [Hands-on-RL：配套代码仓库](https://github.com/boyu-ai/Hands-on-RL)
* [PPO: Proximal Policy Optimization Algorithms](https://arxiv.org/abs/1707.06347)（2017）
* [DQN: Human-level control through deep reinforcement learning](https://www.nature.com/articles/nature14236)（Nature，2015）
* [The Landscape of Agentic Reinforcement Learning for LLMs: A Survey](https://arxiv.org/abs/2509.02547)（智能体强化学习综述）

---

## 实战演练

完成前面的基础学习后，请选择一篇感兴趣的论文（也可以与我商量来选择），**自行检索论文对应的开源代码和数据，完成复现，并制作一份 PPT，讲清楚论文内容、结果、代码复现结果**。

本次复现选题不限定未来的研究方向，可以根据兴趣和实际条件任选一项。重点是通过实践，学会阅读论文、理解代码、运行实验和分析结果，逐步掌握能够迁移到其他方向的学习方法与科研思路。

**完成后，请主动联系我，并附上汇报 PPT、代码或复现说明以及实验结果，安排交流汇报。**

通过实战演练后，会结合大家的基础、兴趣和实践情况，一起讨论具体研究方向。

### 1. 选择论文

下面按方向列出一些论文和入门代码供参考，也鼓励大家根据兴趣，自行寻找相关方向论文和开源代码进行复现。自主选题时，**优先选择近一年内发表，或对应 GitHub 代码仓库 Star 较多的工作**，同时结合代码与数据的完整性、运行说明和现有算力，判断是否适合开展复现。

如果算力不足，可以在方法和代码支持的前提下，选择同系列的较小模型先跑通流程。例如，论文使用 Qwen2.5-32B 时，可以尝试用 Qwen2.5-1.5B 开展实验。汇报时应说明模型替换和其他实验设置的变化，并据此分析与原论文结果的差异。

#### GUI Agent

* [What Happens Before Decoding? Prefill Determines GUI Grounding in VLMs](https://arxiv.org/abs/2605.12549)
* [MVP: Multiple View Prediction Improves GUI Grounding](https://arxiv.org/abs/2512.08529)

#### Agent Skill

* [XSkill: Continual Learning from Experience and Skills in Multimodal Agents](https://arxiv.org/abs/2603.12056)
* [Ace-Skill: Bootstrapping Multimodal Agents with Prioritized and Clustered Evolution](https://arxiv.org/abs/2605.08887)

#### 时间序列处理

* [Time-LLM: Time Series Forecasting by Reprogramming Large Language Models](https://arxiv.org/abs/2310.01728)

#### 强化学习

可以结合学习资料中的 PPO、DQN 论文，选择以下入门代码开展实战：

* [动手学强化学习：第 12 章 PPO 算法（Notebook）](https://github.com/boyu-ai/Hands-on-RL/blob/main/%E7%AC%AC12%E7%AB%A0-PPO%E7%AE%97%E6%B3%95.ipynb)
* [动手学强化学习：第 7 章 DQN 算法（Notebook）](https://github.com/boyu-ai/Hands-on-RL/blob/main/%E7%AC%AC7%E7%AB%A0-DQN%E7%AE%97%E6%B3%95.ipynb)

#### 图像质量评估

* [AIGC Image Quality Assessment via Image-Prompt Correspondence](https://openaccess.thecvf.com/content/CVPR2024W/NTIRE/html/Peng_AIGC_Image_Quality_Assessment_via_Image-Prompt_Correspondence_CVPRW_2024_paper.html)
* [MoE-AGIQA: Mixture-of-Experts Boosted Visual Perception-Driven and Semantic-Aware Quality Assessment for AI-Generated Images](https://openaccess.thecvf.com/content/CVPR2024W/NTIRE/papers/Yang_MoE-AGIQA_Mixture-of-Experts_Boosted_Visual_Perception-Driven_and_Semantic-Aware_Quality_Assessment_for_CVPRW_2024_paper.pdf)

#### 知识图谱

* [SimKGC: Simple Contrastive Knowledge Graph Completion with Pre-trained Language Models](https://arxiv.org/abs/2203.02167)
* [Multi-View Riemannian Manifolds Fusion Enhancement for Knowledge Graph Completion](https://doi.org/10.1109/TKDE.2025.3538110)
* [KnowFormer: Revisiting Transformers for Knowledge Graph Reasoning](https://arxiv.org/abs/2409.12865)

#### 大模型自我反馈与迭代改进

* [Self-Refine: Iterative Refinement with Self-Feedback](https://arxiv.org/abs/2303.17651)

#### 智能体推理

* [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629)

#### 多智能体

* [Cut the Crap: An Economical Communication Pipeline for LLM-based Multi-Agent Systems](https://arxiv.org/abs/2410.02506)

#### Agent 记忆

* [A-MEM: Agentic Memory for LLM Agents](https://arxiv.org/abs/2502.12110)
* [LightMem: Lightweight and Efficient Memory-Augmented Generation](https://arxiv.org/abs/2510.18866)

#### Agent 安全

* [DRIFT: Dynamic Rule-Based Defense with Injection Isolation for Securing LLM Agents](https://arxiv.org/abs/2506.12104)

#### 模型协同

* [Confidence-Calibrated Small-Large Language Model Collaboration for Cost-Efficient Reasoning](https://arxiv.org/abs/2603.03752)
* [Confidence-Guided Stepwise Model Routing for Cost-Efficient Reasoning](https://arxiv.org/abs/2511.06190)
* [SpecReason: Fast and Accurate Inference-Time Compute via Speculative Reasoning](https://arxiv.org/abs/2504.07891)

### 2. 复现要求

* **读懂论文与代码**：能够说明论文研究的问题、核心方法，以及关键方法在代码中的实现位置。
* **完成一次完整实验**：不要求完整复现论文全部实验，但需要在至少 1 个数据集上跑通完整算法流程，并得到结果；强化学习任务则在至少 1 个环境中完成训练与评估。
* **体现自己的理解**：可以使用 AI 辅助阅读和调试，但需要自己检查代码与结果。

### 3. 制作 PPT 并汇报

建议制作一份 PPT，准备 **10–15 分钟**的汇报，围绕以下内容展开：

1. **论文基本信息**：论文题目、主要作者及所属单位、发表时间与平台，以及代码仓库来源和 GitHub Star 数量。
2. **研究问题与方法**：现有工作存在哪些问题？论文的研究动机是什么，提出了什么方法？
3. **论文实验**：使用了哪些数据集或环境、评价指标、实验设置和对比方法？主要结果是什么？
4. **自己的结果与思考**：展示复现结果，说明与原论文设置和结果的差异，以及仍未解决的问题。

汇报要有条理，结合示意图、实验图表和具体案例，避免整页堆砌文字，也不要只复述论文内容。论文内容部分的 PPT 可参考[论文分享示例：GUI Agent](论文分享GUI%20Agent.pptx)。
