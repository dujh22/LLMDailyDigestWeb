# 2026-09-25 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 自我改进闭环从模型权重扩展到脚手架、数据与轨迹： [ModularRSI](#modularrsi-harness) 在冻结模型下迭代 Harness，[SEAL](#mit-seal) 让模型生成自编辑并更新权重，[DataFlex-RL](#dataflex-rl-rl) 与 [OPD](#opd) 则分别优化 RL 数据调度和在策略轨迹学习。
- 长期记忆走向可审计、可演化的外部知识系统：[Meta“组织第二大脑”](#meta) 以显式程序、专家反馈和回归测试维护机构知识，[自回归视频记忆综述](#item-7) 则从五个维度统一梳理时序状态持久化机制。
- 动态评测与可靠性成为能力验证主线：[薛定谔代码仓库](#llm-swe-bench) 用功能等价变换揭示 SWE-bench 中的记忆依赖，[HappyWorld-Bench](#happyworld-bench) 面向视频、空间和具身交互评测世界模型的状态一致性与长程可靠性。
- 具身与视频研究共同聚焦长程状态更新和闭环反馈：[Spatial-Interactor](#spatial-interactor) 从物理交互轨迹学习空间状态转移，[PackLab](#packlab) 打通装箱仿真、训练与评测，[RewardVerse](#rewardverse) 提供动态评分标准驱动的可解释视频奖励。
- 自主科研工作流继续向端到端推进：[AI Skill 自动发现科研 Idea 并运行实验](#ai-skill-idea) 和 [AI自主跑实验并生成论文](#item-14) 展示从创意、实验到写作的自动化实践，[从 AI Build AI 到真正 RSI](#ai-build-ai-rsi) 则讨论跨代码、科学与具身场景的自进化闭环。
- 新型决策与系统能力呈现多样化探索：[Jev](#jev) 引发类型安全、概率化快决策模型研究，[Claude Opus 5.5](#claude-opus-5-5-3d) 展示纯代码构建视觉应用的能力，[GeoPair](#geopair-transformer) 则以免训练方式保几何压缩 Transformer。

## 对当前研究的启发
- **Awesome-RSI**：[ModularRSI](#modularrsi-harness) 与 [SEAL](#mit-seal) 分别验证了外部脚手架和内部权重两条自改进路径，可用于构建“改进对象—反馈信号—验证机制”的统一 RSI 分类框架。
- **HarnessEvolve**：[ModularRSI](#modularrsi-harness) 表明基于执行轨迹自动修改并回归验证模块化 Harness，能在冻结模型下持续增益且跨模型迁移，可作为 Harness 演化流水线的直接原型。
- **MemoryEvolve**：[Meta“组织第二大脑”](#meta) 将知识外置、显式推理程序、专家反馈和回归测试组合成可审计闭环，为长期记忆的安全更新、错误回滚与组织级共享提供了具体架构。
- **DataEvolve**：[SEAL](#mit-seal) 的自主合成数据与学习策略生成结合 [DataFlex-RL](#dataflex-rl-rl) 的动态选择、重加权和领域混合，可形成“生成—估值—配比—训练”的数据进化闭环。
- **EvolveLLM**：[SEAL](#mit-seal) 通过强化学习优化自编辑、再以内层监督微调落实权重更新，为研究模型如何自主设计持续学习策略及控制遗忘提供了可复现实验范式。
- **EvolveLRM**：[DataFlex-RL](#dataflex-rl-rl) 的统一数据策略比较框架与 [OPD](#opd) 的在策略逐 token 蒸馏，可用于同时研究 RL 推理训练中的数据配比、公平对照和稠密反馈。
- **EvalEvolve**：[薛定谔代码仓库](#llm-swe-bench) 证明功能等价的动态仓库变换能够区分仓库线索记忆与真实推理，为构建抗污染、可持续生成变体的代码智能体评测提供了关键方法。
- **ResearchEvolve**：[AI Skill 自动发现科研 Idea 并运行实验](#ai-skill-idea) 与 [AI自主跑实验并生成论文](#item-14) 提供了端到端科研自动化案例，可进一步加入新颖性审查、实验复现和结果回归测试形成可信科研闭环。
- **JevEvolve**：[Jev](#jev) 周边对选项敏感性、模型评判和智能体记忆的快速研究扩散，提示应优先建立快决策模型的校准评测，并从交互日志学习快慢模型路由边界。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-25/  

