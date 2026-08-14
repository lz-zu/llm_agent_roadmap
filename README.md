# 科研入门学习指南

## 学习目标

本学习指南面向刚开始接触科研的本科生和研究生，希望帮助同学逐步掌握编程、信息检索、论文阅读和代码实践等基本能力，并对本研究小组的方向形成初步认识。

> 本指南中的资料主要用于提供学习入口，遇到不懂的问题时，应主动搜索、阅读文档并动手实践。

---

## 科研思路与基本习惯

在学习具体知识之前，应先建立主动检索、独立判断和动手验证的习惯。工具可以提高效率，但真正重要的是发现问题、理解问题并验证结论的能力。

### 1. 善用 AI，但不要依赖 AI

ChatGPT、Codex、Claude Code可以辅助学习、编程和科研，但不能代替独立思考，也不能保证所有回答都正确。

* 可以使用 ChatGPT 解释概念、比较方法、辅助阅读论文、整理思路和检查文字表达；
* 可以使用 [Codex](https://learn.chatgpt.com/docs/codex/cli) 阅读代码仓库、梳理程序流程、修改代码、定位报错，也可以辅助完成论文复现和论文撰写；
* AI 有时会为了“完成任务”而采取捷径，例如忽略失败样本、弱化检查条件、生成冗余代码，甚至让实验结果看起来虚高；
* 对 AI 生成的代码要对实验日志和原始结果要仔细检查，对重要事实和论文结论要回到原始资料核对；
* 面对复杂任务时，应将任务拆分成若干小步骤，逐步完成、逐步检查。

#### 示例：使用 ChatGPT 辅助阅读论文

可以将论文 PDF 提交给 ChatGPT，再通过提示词将论文转化为容易理解的文字，快速了解文章脉络和主要内容。但这种方式可能忽略公式、实验细节和部分上下文。如果论文重要，仍需要自己认真阅读原文。

下面提供一个可供参考的提示词：

````text
用纯文字解释我给你的PDF，它来自一篇计算机学科领域的高质量论文，按以下流程操作：
- 我会给你文章的pdf。
- 收到我的内容，请用 Markdown 格式输出解释，放在代码块中。请严格按照以下结构排版：
# 摘要
# 1. 引言
## 1.1 其中的第一部分内容
# 2. 相关工作（如果第二部分是这个内容）
## 2.1 内容
...依此类推。
- 不要添加想象或超出所给内容的信息。所有解释仅基于文章提供的信息。
- 明确、完整地解释内容，不遗漏任何关键信息。对难以理解的部分可以适当详细解释，帮助读者全面理解。
- 解释要专业、自然，帮助读者理解，避免让内容显得像是 AI 生成。不要添加无用注释。
- 仅输出收到的全部内容截至当前的解释结构。每次都输出至目前为止收到的所有段落的解释。
- 若遇模糊或难以理解的概念，应尽量根据上下文解释，并用清晰简明的语言表达。
- 读者是一个初学者，你需要用通俗易懂的语言来讲解，必须的时候，添加对各类概念和理论的解释
重要：
1. 不要包含公式，只用文字解释。
2. 不遗漏任何文中信息，重要之处可多句解释。
3. 解释应遵循原文结构和思路，重要部分可详述。
4. 保持表达专业并自然，帮助读者理解。
5. 避免显露为 AI 生成，例如不添加无用注释。
## Output Format
请将解释内容以 Markdown 格式输出，整体放入代码块。例如：
```shell
# 1. 引言
## 1.1 其中的第一部分内容（视情况或更多的小标题）
<引用部分的纯文字说明>
## 1.2 其中的第二部分内容
# 2. 相关工作（如果第二部分是这个内容）
## 2.1 内容
<第二部分的纯文字说明>
```
### Output Verbosity
如相关概念难以解释，请检索最新的知识，并给出介绍，说明为什么这么做，有什么优势，帮助读者理解
````

#### 使用 Codex 辅助科研和编程

可以在 VS Code 中安装 Codex 扩展，也可以在桌面端或终端中使用。使用过程中，应逐渐形成适合自己的任务描述和检查习惯，并将长期有效的项目约定写入 `AGENTS.md`。

Codex 还支持使用 [Skill](https://learn.chatgpt.com/docs/build-skills) 保存和复用特定工作流程。Skill 并非越多越好：如果某个 Skill 不适合当前任务或经常带来冗余步骤，应及时停用或删除，避免增加不必要的上下文和 Token 消耗。

### 2. 主动检索，并学会判断资料质量

科研初期要广泛的阅读文献，不要太有局限性，当遇到陌生概念、代码报错或新的研究问题时，应先主动搜索，例如在google、bilibili、知乎甚至小红书。

* 使用 Google 搜索论文、官方文档、代码仓库，以及相关学者和实验室的主页；
* 使用 [Google Scholar](https://scholar.google.com/) 检索学术论文，可通过参考文献和谷歌学术查看“被引用”论文，梳理研究脉络；
* 使用 Bilibili 上的中文课程、论文讲解和技术分享快速建立直观认识。
* 不要小看小红书的帖子和微信公众号的推送，现在很多强组都会在小红书和微信上宣传。
* 在确定研究方向前，找到可以参考的论文baseline，查看他的实验表格，能否用于我们的论文撰写，从而提前规划好实验部分，选择的baseline最好是一年内的。

阅读论文时，应优先关注领域内的顶级会议、顶级期刊和具有代表性的工作。例如：

* 综合机器学习：NeurIPS、ICML、ICLR、AAAI；
* 自然语言处理：ACL、EMNLP、NAACL、EACL；
* 计算机视觉：CVPR、ICCV、ECCV；
* 代表性期刊：JMLR、TPAMI、IJCV、TKDE 等。

论文的发表平台、引用量、作者和研究单位、代码仓库的 Star 数量等都可以作为参考，选择复现论文时，还应关注是否公开代码和数据、以及现有算力能否支持。

### 3. 从一个大方向逐步进入具体问题

接触一个新的研究方向时，建议按照下面的思路逐步深入：

1. **阅读综述和典型论文**：使用“研究方向 + survey/review/tutorial/overview”等关键词检索综述和教程。对于热门方向，也可以通过 Bilibili、小红书等平台上的讨论建立直观认识，基于综述和论文深入了解该方向研究目标、常用数据集和评测指标；
2. **寻找感兴趣的问题**：结合现有方法的不足，选择一个自己感兴趣的具体小方向。可以与导师讨论，可以继承组里师兄已经有基础方向，也可以通过阅读论文自行寻找；
3. **深入阅读与实践**：围绕小方向继续检索论文，选择有公开代码的工作进行复现和分析，逐步形成系统而具体的认识。

对于发展很快的新方向，可以阅读 arXiv 上新的论文和技术报告，但应注意区分预印本和已经过同行评审的论文。

---

## 学习资料

对于具体的人工智能学习内容，因每个人基础不同，可以有选择性的学习。

### 1. Python 基础（可跳过）

Python作为人工智能使用最广泛的编程语言，应优先掌握，可以自己查找相关的教程学习，学习过程中不要求掌握全部细节和难点，注意不要花费大量的时间，能做到配置运行环境、编程软件、能运行代码、读懂代码、了解基本概念即可，但是要对整体编程语言有清晰的认知，后续在动手复现论文和实验中逐步查漏补缺。

**参考资料**：

* [python基础快速了解](bilibili.com/video/BV1KE421A7rV/)
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

**学习目标**：理解大模型 Agent 的基本概念，能够区分 Agent 与普通对话型 LLM，掌握 ReAct 等基础 Agent 方法的原理与实现，并了解 Agent 的工具使用、记忆、规划方法以及 Multi-Agent 系统的基本概念。

**参考资料**：

* [Hello-Agents](https://github.com/datawhalechina/hello-agents)-优先学习
* [ReAct: Synergizing Reasoning and Acting in Language Models](https://arxiv.org/abs/2210.03629)
* [LLM Powered Autonomous Agents](https://lilianweng.github.io/posts/2023-06-23-agent/)
* [Hugging Face Agents Course](https://huggingface.co/learn/agents-course/en/unit0/introduction)
* [Large Language Model Agent: A Survey on Methodology, Applications and Challenges](https://arxiv.org/abs/2503.21460)（2025，大模型智能体综述）
* [Multi-Agent Collaboration Mechanisms: A Survey of LLMs](https://arxiv.org/abs/2501.06322)（2025，多智能体协作综述）



## 3 论文复现要求

* 不要求完整复现论文的全部实验，但需要在至少 1 个数据集上跑通完整流程并得到结果；
* 未能复现论文结果并不代表失败，应分析模型、数据、环境和实现上的差异；
* 优先选择代码和数据公开的代表性论文，尽量复用现有框架；
* 讲自己的研究时，要有条理，不要过分简略，ppt不要全都是文字
