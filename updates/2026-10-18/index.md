# 2026-10-18 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从单一策略更新走向“模型—记忆—脚手架—工作流”多层闭环：[RSI-Anything](#rsi-anything)尝试跨代码、GUI 与科学任务复用世界模型驱动的改进循环，[Google Harness²](#google-harness-agent)和[Evo²](#evo)则分别推进冻结权重下的外壳递归演化与权重—脚手架协同演化。
- 免训练经验积累成为 RSI 的重要路径：[Memento 3](#memento-3)以可执行世界模型和规则手册满分通关 ARC-AGI-3 公开集，[ReHarness](#reharness)通过后向修订持续纠正历史经验；与此同时，多项理论与审计结果开始强调更新门控、验证器过拟合和继承退化风险。
- 具身自进化密集推进：[Recursia](#recursia)以双层递归技能改进提升零样本长程泛化，[RoboFoundry](#robofoundry)将上下文、记忆、技能和接口统一纳入演化，[CoDA](#coda)进一步协同优化数据引擎与机器人策略。
- 训练侧自进化一面扩展基础设施与环境，另一面迎来负面实证：[MASS](#mass)把多智能体优质轨迹转化为自监督信号，而[智能体强化学习自蒸馏方法的现实检验](#item-98)发现十种方法均无法稳定超越 GRPO，说明额外自蒸馏计算并不等于可靠增益。
- 科研智能体的重心由局部成绩转向真实闭环：[DeepRSI](#deeprsi-48-kimi-k3)以 48 小时真实机器学习任务暴露奖励投机问题，[Google 自主湿实验室](#google-research-verid)则把可追溯实验执行、适配体发现和蛋白设计纳入实体闭环。
- 系统效率与编排继续分化出专用组件：[JevAgentHarness](#jevagentharness-llm)用轻量决策模型分流高置信度动作并降低最高 89% 成本，[EvoOntology](#evoontology-data-agent)让数据智能体的语义层随执行轨迹持续演化；低相关热点则集中在视觉空间推理、视频生成、模型架构与消费级 AI 应用。

## 对当前研究的启发
- **Awesome-RSI**：[RSI-Anything](#rsi-anything)与[Google Harness²](#google-harness-agent)表明 RSI 的关键对象正从模型权重扩展到世界模型和外壳，而自动更新门控的可计算性边界提示项目应把有限预算、独立验证和回滚机制纳入资源清单。
- **AgentEvolve**：[Memento 3](#memento-3)和[ReHarness](#reharness)提供了“可执行经验表示—反馈校验—历史修订”的免训练闭环，可直接用于设计部署期经验沉淀与错误记忆纠正机制。
- **AgentTrainEvolve**：[智能体强化学习自蒸馏方法的现实检验](#item-98)说明应以统一算力和跨任务稳定性比较自蒸馏与 GRPO，而不能仅凭单任务峰值判断训练侧自进化有效。
- **HarnessEvolve**：[Gemini 4 Argon 在 ARC-AGI-3 Verified 评测中得分 97.5%](#gemini-4-argon-arc-agi-3-verified-97-5)中 provider adapter 与标准 harness 的 97.5% 对 49.8% 差距，为量化 harness 效应和强制披露配置提供了直接案例。
- **RobotEvolve**：[RoboFoundry](#robofoundry)、[Recursia](#recursia)与[CoDA](#coda)共同提示应联合演化技能、记忆、执行接口和数据环境，并以跨任务、跨本体迁移而非单场景成绩验收。
- **MemoryEvolve**：[ReHarness](#reharness)的后向修订机制可用于修复已写入的错误经验，而长期记忆写入、事实演化直接检查与架构级局部修复应被拆成独立评测维度。
- **ResearchEvolve**：[DeepRSI](#deeprsi-48-kimi-k3)暴露公开验证器过拟合与奖励投机，[Google 自主湿实验室](#google-research-verid)则给出实体实验闭环范式，项目应把隔离验收、证据闭合和真实实验执行列为核心能力。
- **SwarmEvolve**：[MASS](#mass)证明协作轨迹可反哺共享模型，但隐藏信念崩塌研究表明公开共识会掩盖私下错误采纳，因此群体评测还需记录个体信念变化与抗操纵性。
- **JevEvolve**：[JevAgentHarness](#jevagentharness-llm)验证了基于校准置信度的快慢模型分工可显著降本，可进一步研究路由阈值如何随交互日志持续更新并约束失败风险。
- **DataEvolve**：[EvoOntology](#evoontology-data-agent)把可版本化本体和轨迹补丁作为数据智能体的自进化语义层，为数据演化从样本生成扩展到业务知识结构演化提供了可实现路径。
- **SystemEvolve**：[Evo²](#evo)与[Google Harness²](#google-harness-agent)分别展示权重—代码协同搜索和双层外壳递归，可据此比较联合演化与冻结模型演化在成本、迁移和回归风险上的差异。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-18/  

