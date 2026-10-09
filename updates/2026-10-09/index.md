# 2026-10-09 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **推理模型持续自进化**：两项高相关工作分别攻克数据坍缩与信用分配，[R-Quest](#r-quest) 以有效性和新颖性反馈支撑连续十轮稳定提升，[SCAPO](#scapo) 则借助半事实干预改善 GRPO 的词元级归因与分布外泛化。
- **可验证推理与自主科研**：[VeriLoop E2](#veriloop-e2-67-35) 将外部验证证据纳入状态提交和后训练闭环，并报告把黎曼猜想临界线零点比例下界推进至 67.35%，展示“生成—验证—递归改进”的科研路径。
- **环境与经验共同演化**：[AgentGarten](#agentgarten) 结合代码化物理世界、实时神经渲染和跨轮次经验手册，为具身智能体提供可持续试错、积累经验并改进策略的闭环环境。
- **长期个人智能体基础设施**：[nanoMuse](#nanomuse) 通过跨设备共享会话、可溯源文件记忆和动作安全审查，探索兼顾状态持久化、记忆来源追踪与执行安全的本地智能体。
- **热点延伸**：低相关性工作集中于世界—动作模型与长程视频、生成加速及智能体安全评测，包括 [Long-WAM](#long-wam)、[UniWAM](#uniwam)、[SGF+](#sgf) 和 [DecepEval](#decepeval-llm) 等。

## 对当前研究的启发
- **EvolveLRM**：[R-Quest](#r-quest) 的无效问题过滤与新颖性反馈可用于抑制多轮自训练的数据重复和能力坍缩，而 [SCAPO](#scapo) 的半事实词元信用可增强推理 RL 的训练稳定性与跨域泛化。
- **DataEvolve**：[R-Quest](#r-quest) 表明将“有效性”和“相对已有训练集的新颖性”联合用作筛选信号，可能比单纯按解题难度过滤更适合维持长期数据飞轮。
- **LogicEvolve**：[VeriLoop E2](#veriloop-e2-67-35) 的外部证据驱动状态提交与 [SCAPO](#scapo) 的半事实归因，分别提供了可验证递归推理和细粒度逻辑训练反馈的可复用机制。
- **ResearchEvolve**：[VeriLoop E2](#veriloop-e2-67-35) 展示了把数学验证证据直接接入假设迭代与后训练闭环的自主科研范式，可用于提高研究结论的可审计性。
- **EnvironmentEvolve**：[AgentGarten](#agentgarten) 的确定性代码环境与实时渲染解耦方案，可作为同时满足可执行、可复现和高频交互的具身环境合成架构。
- **MemoryEvolve**：[AgentGarten](#agentgarten) 的跨轮次经验手册和 [nanoMuse](#nanomuse) 的可溯源文件记忆，为长期记忆的经验沉淀、来源审计及跨设备共享提供了两种互补实现。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-09/  

