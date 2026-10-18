# 2026-10-18 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进正从单一反思走向“模型、Harness、工作流共同演化”：可执行世界模型驱动的 [Memento 3](#memento-3)、冻结权重递归优化外壳的 [Google Harness²](#google-harness-agent)、权重与脚手架协同优化的 [Evo²](#evo)，以及将多智能体轨迹回灌模型的 [MASS](#mass) 分别覆盖了非参数、系统级与训练侧闭环。
- 具身自进化开始验证长程泛化与跨平台迁移：[Recursia](#recursia) 以双层循环持续改进共享技能栈，[RoboFoundry](#robofoundry) 则把上下文、记忆、技能和执行接口整体纳入“执行—反思—修复—晋升”闭环。
- Agent 训练基础设施提速，但算法收益仍需严格对照：[QwenGyre](#qwengyre-agent) 将超长程在线 RL 端到端加速 1.78 倍，而 [智能体强化学习自蒸馏方法的现实检验](#item-98) 发现十种方法均无法稳定超越 GRPO，提示额外计算不等于有效进化。
- 记忆与语义层从被动存储转向可学习写入和轨迹驱动演化：[Hy-Memory-30B-A3B](#hy-memory-30b-a3b) 用归因强化学习学习长期记忆写入协议，手动收录的 [EvoOntology](#evoontology-data-agent) 则让 Data Agent 根据执行轨迹持续修补可版本化业务本体。
- 自主科研同时向真实实验和关键决策评测推进：[Athanor](#athanor) 已能在真实 GPU 沙箱中自主完成模型后训练，[Google 自主湿实验室](#google-research-verid) 打通实验执行与发现闭环，而 [SciΠvot](#sci-vot) 显示前沿模型在科研关键节点的判断仍显著落后于资深研究者。
- 系统侧出现两条并行主线：多智能体通过 [MASS](#mass) 学习协作工作流，轻量决策模型则由 [JevAgentHarness](#jevagentharness-llm) 承担高频路由并降低 81.1%～89.0% 成本；与此同时，低相关热点主要集中在视频生成、空间视觉、端侧推理与消费级 AI 应用。

## 对当前研究的启发
- **Awesome-RSI**：[Memento 3](#memento-3)、[Google Harness²](#google-harness-agent) 与 [Evo²](#evo) 表明 RSI 应分层比较“经验/世界模型更新、Harness 更新、参数更新”，并为每层设置独立验收与回滚机制。
- **HarnessEvolve**：[Gemini 4 Argon 的 ARC-AGI-3 结果](#gemini-4-argon-arc-agi-3-verified-97-5) 在 provider adapter 与标准 Harness 下相差近一倍，说明 Harness 配置必须作为评测对象和结果披露的一等变量。
- **RobotEvolve**：[Recursia](#recursia) 与 [RoboFoundry](#robofoundry) 提供了可直接复用的双层设计，即任务内修复执行、任务间晋升经验证的技能与系统组件。
- **AgentTrainEvolve**：[QwenGyre](#qwengyre-agent) 可作为超长程分支轨迹训练的系统基线，而 [自蒸馏现实检验](#item-98) 提醒项目必须以等算力 GRPO 对照验证算法净收益。
- **MemoryEvolve**：[Hy-Memory-30B-A3B](#hy-memory-30b-a3b) 将记忆写入转化为可归因的策略学习问题，可用于替代固定规则并单独评估写入、检索和回答三阶段。
- **ResearchEvolve**：[Athanor](#athanor) 与 [Google 自主湿实验室](#google-research-verid) 分别给出计算实验和实体实验闭环模板，[SciΠvot](#sci-vot) 则提示评测应重点采集人类在关键转折点的纠正，而非只看最终产物。
- **SwarmEvolve**：[MASS](#mass) 展示了“搜索协作结构—筛选优质轨迹—回灌共享模型”的群体进化路径，可用于研究协作经验能否沉淀为单体参数能力。
- **JevEvolve**：[JevAgentHarness](#jevagentharness-llm) 证明按置信度划分快决策与 LLM 慢思考可大幅降本，下一步应重点评测阈值漂移、失败升级和跨任务校准。
- **DataEvolve**：[EvoOntology](#evoontology-data-agent) 将执行失败转化为可审计、可版本化的语义补丁，为数据智能体构建“轨迹诊断—本体更新—回归验证”的数据自进化闭环提供了实现范式。
- **EvalEvolve**：[SciΠvot](#sci-vot) 的真实专家纠正记录与 [ARC-AGI-3 Harness 差异](#gemini-4-argon-arc-agi-3-verified-97-5) 共同说明动态评测既要覆盖关键过程决策，也要隔离评测框架本身带来的增益。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-18/  

