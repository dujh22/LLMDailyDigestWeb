# 2026-10-24 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **Agent 训练与系统演化走向可执行闭环**：从 Harness 原生端到端强化学习框架 [OpenForge RL](#openforge-rl-harness)、可验证真实工作环境 [WorkForge](#workforge)，到以合成测试和帕累托优化降低 53% 成本的 [HarnessPro](#harnesspro-agent-53)，优化对象正由模型扩展到环境、脚手架与交付流程。
- **数据与知识层开始自主迭代**：[AutoSFT](#autosft) 用多智能体闭环分析短板并优化监督微调数据，[EvoOntology](#evoontology-data-agent) 则从执行轨迹识别知识缺口、持续更新业务本体，体现数据飞轮从样本生成向语义资产演化。
- **多智能体规模化的收益与风险同时显现**：[1946 个 AI 智能体并行分析小鼠脑 CRISPR 图谱](#1946-ai-crispr) 展示大规模科研编排价值，但[强模型指导使准确率下降 23.6 个百分点](#23-6) 表明通信协议与接收负担可能抵消群体信息优势。
- **推理模型研究转向训练来源、探索策略与过程忠实性**：[“Wait”标记来源追踪](#wait) 质疑部分推理行为由 RL 自主涌现的说法，[MOER](#moer) 通过专家前缀和失败回滚改善探索，[CausalCoT](#causalcot) 则以因果隔离降低思维链注意力泄漏。
- **真实环境评测暴露 Agent 能力与比较方法的脆弱性**：[OpenDS-World](#opends-world-web) 中最佳模型在真实开放 Web 深度搜索上仅达 39.0%，而[工具增强模型比较中的提示敏感性](#item-26) 显示工具调用差异还会放大评测方差；热点延伸则集中于 Skills 生态、可复用 RGBA 图层编辑及预算感知扩散特征适配。

## 对当前研究的启发
- **AgentTrainEvolve**：[OpenForge RL](#openforge-rl-harness) 的训练—推理解耦与 [WorkForge](#workforge) 的可验证长程环境可组合为面向不同 Harness 的规模化 Agentic RL 数据闭环。
- **HarnessEvolve**：[HarnessPro](#harnesspro-agent-53) 证明 Harness 可被自动搜索优化，而[工具增强模型比较中的提示敏感性](#item-26) 提醒评测必须同时披露提示措辞、调用频率和脚手架配置。
- **DataEvolve**：[AutoSFT](#autosft) 提供“诊断模型短板—改写训练数据—闭环评测”的自主数据工程范式，可用于研究数据价值评估与迭代坍缩控制。
- **AgentEvolve**：[EvoOntology](#evoontology-data-agent) 可将任务轨迹中的知识缺口沉淀为持续更新的语义层，为冻结参数 Agent 提供跨任务可复用的业务经验。
- **SwarmEvolve**：[1946 个 AI 智能体并行分析小鼠脑 CRISPR 图谱](#1946-ai-crispr) 与[通信导致准确率下降](#23-6) 的对照说明，群体扩展应优化通信拓扑、消息表达及接收能力匹配，而非单纯增加智能体和信息量。
- **EvolveLRM**：[“Wait”标记来源追踪](#wait)、[MOER](#moer) 与 [CausalCoT](#causalcot) 分别提供行为归因、探索控制和过程忠实性工具，可用于区分真正的 RL 能力增长与训练轨迹模仿。
- **ResearchEvolve**：[Mirendil 与 Recursive 的 RSI 自动研究闭环](#mirendil-recursive-rsi) 和 [CRISPR 多智能体分析](#1946-ai-crispr) 表明自主科研已可规模化执行，但仍需实验审计、证据关联与人类判断作为质量闸门。
- **EvalEvolve**：[OpenDS-World](#opends-world-web) 的真实开放 Web 任务及[工具调用提示敏感性研究](#item-26) 提示动态评测应同时覆盖环境变化、调用策略方差和跨来源证据质量。
- **HumanEvolve**：[元认知脚手架实验](#item-27) 显示适度增加任务分解与目标设定的“生产性摩擦”能改善知识回忆和迁移，可作为避免 AI 辅助知识工作去技能化的具体交互原则。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-24/  

