# 2026-10-18 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进转向“可执行、可验证、可迁移”的系统闭环**：[Memento 3](#memento-3)以可执行世界模型满分通关 ARC-AGI-3，[Google Harness²](#google-harness-agent)递归演化冻结模型的 Agent 外壳，[Evo²](#evo)则进一步协同优化模型权重与代码脚手架。
- **具身自进化从技能积累扩展到整套系统与环境协同演化**：[RoboFoundry](#robofoundry)统一进化上下文、记忆、技能和接口，[Recursia](#recursia)以双层递归技能栈突破零样本长程泛化，[CoDA](#coda)让仿真数据引擎与机器人策略共同演化。
- **自主科研加速走向真实训练与实体实验闭环**：[Athanor](#athanor)已能在真实 GPU 沙箱中自主完成模型后训练，[Google 自主湿实验室](#google-research-verid)则将可追溯实验执行、适配体发现和蛋白设计接入物理世界。
- **多智能体进化开始同时优化协作结构与共享模型**：[MASS](#mass)将工作流搜索所得优质轨迹回灌共享模型，显示群体协作经验可以成为递归自改进的训练信号。
- **评测结果进一步暴露“模型能力、Harness 与改进算法”之间的混淆**：[Gemini 4 Argon 的 ARC-AGI-3 结果](#gemini-4-argon-arc-agi-3-verified-97-5)因 Harness 不同从 49.8% 变为 97.5%，而[智能体强化学习自蒸馏现实检验](#item-98)发现十种方法均无法稳定超过 GRPO。
- **记忆、语义层与快慢决策成为降低长程智能体成本的三条工程主线**：[Hy-Memory-30B-A3B](#hy-memory-30b-a3b)学习长期记忆写入，[EvoOntology](#evoontology-data-agent)按执行轨迹演化业务语义层，[JevAgentHarness](#jevagentharness-llm)以置信度路由将成本降低 81.1%～89.0%。

## 对当前研究的启发
- **Awesome-RSI**：[Memento 3](#memento-3)、[Google Harness²](#google-harness-agent)与[自我改进门控边界](#item-166)共同表明，RSI 应把可执行状态、外部验证合同和有限预算下的更新准入作为核心设计，而不能依赖无约束自评。
- **AgentEvolve**：[RoboFoundry](#robofoundry)证明可将上下文、记忆、技能和接口纳入同一免训练晋升闭环，可用于扩展当前仅演化反思或技能库的研究边界。
- **HarnessEvolve**：[Gemini 4 Argon 的 Harness 分差](#gemini-4-argon-arc-agi-3-verified-97-5)说明 Harness 配置足以改变能力结论，后续评测必须固定并完整披露适配器、工具协议和执行预算。
- **RobotEvolve**：[CoDA](#coda)与[Recursia](#recursia)提示可把数据引擎、技能栈和动作策略视为相互反馈的共同演化对象，而非只更新单一机器人策略。
- **ResearchEvolve**：[Athanor](#athanor)和[Google 自主湿实验室](#google-research-verid)分别给出了计算实验与实体实验的闭环模板，可据此设计兼具隔离验收、证据追踪和真实执行的科研智能体。
- **AgentTrainEvolve**：[智能体强化学习自蒸馏现实检验](#item-98)表明额外蒸馏计算不等于稳定增益，项目应优先建立跨任务、跨模型规模且计入总算力的统一 GRPO 对照。
- **MemoryEvolve**：[Hy-Memory-30B-A3B](#hy-memory-30b-a3b)将写入协议学习为可归因策略，提示长期记忆研究应从手工规则转向以最终任务贡献监督写入、淘汰和框架选择。
- **SwarmEvolve**：[MASS](#mass)把工作流搜索与共享模型训练交替进行，为“群体结构演化产生训练信号、训练后模型再反哺群体”的双层共进化提供了直接方案。
- **DataEvolve**：[EvoOntology](#evoontology-data-agent)表明数据智能体可从执行失败中生成可版本化语义补丁，使业务本体本身成为持续演化、可回滚的数据资产。
- **JevEvolve**：[JevAgentHarness](#jevagentharness-llm)验证了按选择校准置信度的快慢路由可大幅降本，适合进一步研究路由边界如何随交互日志持续更新。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-18/  

