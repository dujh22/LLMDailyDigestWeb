# 2026-10-09 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从单体反思走向“工作流、显式世界模型与参数更新策略”共同演化：[MASS](#mass) 以多智能体工作流进化和自生成轨迹训练同步提升任务与自优化能力，[Memento 3](#memento-3) 用可修订规则手册和严格验证构建冻结模型的持续改进闭环，[Agentic-TTT](#agentic-ttt) 则让智能体自主选择测试时训练算法。
- 推理模型自进化进一步聚焦长期稳定性和细粒度信用分配：[R-Quest](#r-quest) 以有效性、新颖性反馈避免十轮自训练中的数据坍缩，[SCAPO](#scapo) 通过半事实干预改善 GRPO 的词元级归因；[RoboRSI](#roborsi) 将局部责任归因和验证后发布延伸到机器人技能演化。
- 记忆与技能系统开始强调结构化巩固而非简单轨迹堆积：[Hippocam](#hippocam) 以意图层次整合长期经历，[Memento 3](#memento-3) 将经验沉淀为可验证规则，两者都支持无须持续更新基础模型权重的学习。
- 科研智能体研究覆盖“实验决策—数据感知—过程审计”全链路：[语言模型作为 AI 研究世界模型](#item-31) 用结果预测提高有限预算下的干预选择效率，[DataSense-Bench](#datasense-bench-ai) 检验智能体识别高价值训练数据的能力，[研究契约](#item-46) 与 [TRACE](#trace) 分别约束科研声明和诊断验证器脆弱性。
- 环境与多智能体系统同时显现能力扩展和失控风险：[AgentGarten](#agentgarten) 构建可持续试错并传承经验的具身环境，[HarnessSQL](#harnesssql-sql) 将真实执行框架原生纳入训练，而[智能体生态中的种群失控阈值](#item-24) 表明协作可能在越过临界规模后触发自强化扩张；[ReSI](#resi) 提供了循环红队与能力保留约束下的主动防线。
- 热点延伸主要集中于长上下文世界行动模型、超长视频生成与生成系统压缩，展示了显著的工程进展，但与当前自进化研究主线关联较弱。

## 对当前研究的启发
- **Awesome-RSI**：[MASS](#mass) 与 [Memento 3](#memento-3) 表明 RSI 评测应同时追踪任务能力、改进机制能力及外部验证约束，而不能只比较迭代前后的最终分数。
- **EvolveLRM**：[R-Quest](#r-quest) 的问题有效性与新颖性双重过滤可用于抑制多轮自训练的数据坍缩，[SCAPO](#scapo) 的半事实干预则提供了更可靠的词元级信用分配方案。
- **MemoryEvolve**：[Hippocam](#hippocam) 的意图层次和递归前缀整合可作为长期记忆巩固结构，使经验既能压缩复用，又能在需要时恢复细节。
- **ResearchEvolve**：[语言模型作为 AI 研究世界模型](#item-31) 可用于在真实实验前预测干预收益，而[研究契约](#item-46) 能把实验选择、执行证据和最终声明绑定成可审计科研闭环。
- **EvalEvolve**：[TRACE](#trace) 的固定轨迹重评分与行为核验可帮助动态基准区分真实能力提升、验证器漏洞和运行随机性。
- **EnvironmentEvolve**：[AgentGarten](#agentgarten) 的确定性代码世界加实时渲染，以及 [HarnessSQL](#harnesssql-sql) 的真实执行环境训练，提供了兼顾可扩展经验生成与可验证反馈的两类环境模板。
- **SwarmEvolve**：[MASS](#mass) 展示了群体工作流与模型能力协同演化的收益，但[种群失控阈值](#item-24) 提醒项目必须将群体规模、协作密度和失配智能体扩张纳入安全指标。
- **HarnessEvolve**：[HarnessSQL](#harnesssql-sql) 说明应让训练与评测共享真实执行 harness，[TRACE](#trace) 则可用于审计 harness 验证器是否制造虚假能力增益。
- **LogicEvolve**：[SCAPO](#scapo) 的半事实稳定性信号可用于识别真正支撑答案的推理词元，为提升逻辑推理的分布外泛化和过程忠实度提供训练抓手。
- **Groom**：[TRACE](#trace) 的成对实验和固定轨迹重评分可扩展为 token 级过程归因，判断成本变化究竟来自有效推理、冗余执行还是评测噪声。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-09/  

