# 2026-10-24 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- Agent 训练与系统演化加速走向端到端闭环：[OpenForge RL](#openforge-rl-harness)打通 Harness 原生强化学习，[WorkForge](#workforge)规模化构建可验证真实工作环境，[HarnessPro](#harnesspro-agent-53)则以无标签协同进化同时优化任务成功率与成本。
- 数据与知识层开始成为可持续进化对象：[AutoSFT](#autosft)让多智能体闭环优化监督微调数据，[EvoOntology](#evoontology-data-agent)则从执行轨迹中发现知识缺口并持续更新业务本体。
- RSI 与自主科研出现更大规模的实践信号：[Mirendil 与 Recursive](#mirendil-recursive-rsi)展示模型训练及自动研究闭环，[GPT-Rosalind](#1946-ai-crispr)以 1946 个智能体并行完成大规模 CRISPR 图谱分析。
- Agent 评测进一步暴露 Harness 与协作协议的决定性影响：[工具增强模型比较](#item-26)会因提示措辞改变相对结果，[多智能体通信研究](#23-6)更发现强模型指导可令准确率下降 23.6 个百分点；[OpenDS-World](#opends-world-web)中前沿模型在真实深度搜索任务上的最佳准确率也仅为 39%。
- 推理研究转向过程忠实性与训练来源审计：[CausalCoT](#causalcot)通过因果上下文隔离降低注意力泄漏，[“Wait”标记追踪](#wait)则表明部分推理行为源自训练数据继承而非强化学习涌现。
- 热点延伸集中于 Skills 插件生态变化、可复用图像图层与预算感知视觉适配，以及个人 AI 入口、超级 App 权限和开放社区中的智能体治理问题。

## 对当前研究的启发
- **AgentTrainEvolve**：[OpenForge RL](#openforge-rl-harness)与[WorkForge](#workforge)可组合为“可替换 Harness 训练框架＋规模化可验证环境”的长程 Agentic RL 基础设施。
- **HarnessEvolve**：[工具增强模型比较](#item-26)证明提示措辞会经由工具调用频率改变模型排名，评测披露应纳入提示变体、调用轨迹及 Harness 配置的敏感性分析。
- **SystemEvolve**：[HarnessPro](#harnesspro-agent-53)展示了用合成测试和帕累托优化共同搜索系统通过率与成本的可行路径，可用于系统级自进化的多目标选择机制。
- **DataEvolve**：[AutoSFT](#autosft)可直接借鉴为“短板诊断—数据改写—训练—评测”闭环，而[EvoOntology](#evoontology-data-agent)进一步提示业务语义层也能由轨迹驱动持续演化。
- **SwarmEvolve**：[多智能体通信研究](#23-6)说明群体演化不能默认信息越多越好，应把接收能力、表达协议与处理成本共同纳入通信拓扑优化目标。
- **ResearchEvolve**：[GPT-Rosalind](#1946-ai-crispr)提供了大规模科研智能体并行编排及证据汇聚范式，[Mirendil 与 Recursive](#mirendil-recursive-rsi)则强调实验审计和人类判断必须进入自动研究闭环。
- **EvolveLRM**：[“Wait”标记追踪](#wait)提示评估 RL 所产生的新推理能力时必须先做训练谱系与轨迹数据归因，避免把模仿行为误判为自主涌现。
- **LogicEvolve**：[CausalCoT](#causalcot)可作为过程忠实性训练与评测的新工具，通过对子问题依赖图进行干预来区分真实因果推理与上下文泄漏。
- **HumanEvolve**：[元认知脚手架研究](#item-27)表明适度“生产性摩擦”虽增加认知负担，却能改善知识留存与脱离 AI 后的能力迁移，可作为增强型交互设计原则。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-24/  

