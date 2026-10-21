# 2026-10-21 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **智能体脚手架进入“结构、接口与策略协同演化”阶段**：多项工作不再只调提示，而是联合优化交互框架与模型策略（[Self-HPO：框架与策略协同优化的自进化编码智能体](#self-hpo)）、从失败轨迹演化接口及使用知识（[Agent S4：从任务经验中演化智能体接口](#agent-s4)），并以跨模型共享脚手架降低迁移成本（[MaD-RSI：以模型为数据的智能体脚手架递归自我改进](#mad-rsi)）。
- **长程 Agent 训练聚焦“可执行环境 + 细粒度信用分配”**：[CoworkEnv：为长时程协作智能体合成可执行训练环境](#coworkenv)提供可验证的 SFT/RL 任务来源，[Self-Credit：长程智能体强化学习的组内重缩放信用分配](#self-credit)与[TrajEvolve：基于事后信用分配的强化学习轨迹演化](#trajevolve)则分别从证据引用和反事实步骤修复缓解稀疏奖励。
- **具身自进化从仿真走向真机与群体经验飞轮**：[RLinf v0.4 发布：具身强化学习迈向真实物理世界](#rlinf-v0-4)补齐模块化真机接口和异构训练基础设施，[从车队经验中学习：机器人集体学习范式](#item-15)则让机器人共享成功轨迹并利用失败上下文持续改进统一策略。
- **自主科研开始以真实实验和可恢复定律检验能力边界**：[Claude Science设计抗蝎毒蛋白并通过湿实验验证](#claude-science)将大规模候选生成闭环至湿实验命中，[OptScientist：自动发现符号优化定律](#optscientist)进一步展示了从观测与文献先验中恢复跨领域紧凑定律的路径。
- **效率、评测与安全共同约束自进化系统**：[EdgeRock-4B：固定内存长推理，KV Cache削减99.1%](#edgerock-4b-kv-cache-99-1)展示固定预算长上下文架构，[智能体脚手架优化：能力唤起还是能力扩展？](#item-32)与[DecisionPivot：LLM 决策模型诊断评测基准](#decisionpivot-llm)要求超越总体成功率，而[奖励错设会削弱思维链可监控性](#item-27)和[辩论可纠正人类判断，却难以改善弱模型监督](#item-72)分别暴露奖励作弊与弱监督失效风险。
- **热点延伸**：低相关条目主要分布在脑编码参数高效微调、第一人称三维表征、轻量嵌入及多轮图像编辑，体现多模态方法向垂直科学与生成任务的持续扩散。

## 对当前研究的启发
- **CacheEvolve**：[EdgeRock-4B](#edgerock-4b-kv-cache-99-1)的固定容量“记忆岩锚”可作为固定预算缓存策略的新架构基线，重点验证其锚点选择是否可学习以及长程信息损失如何随任务变化。
- **HarnessEvolve**：[Self-HPO](#self-hpo)与[智能体脚手架优化：能力唤起还是能力扩展？](#item-32)提示脚手架搜索应同时优化策略并报告可达任务覆盖率，避免把 pass@k 提升误判为能力边界扩展。
- **SystemEvolve**：[Agent S4](#agent-s4)和[MaD-RSI](#mad-rsi)表明接口、工具知识及跨模型共享脚手架都可纳入统一演化对象，可据此设计“失败轨迹分析—系统修改—跨模型验证”的闭环。
- **AgentTrainEvolve**：[CoworkEnv](#coworkenv)、[Self-Credit](#self-credit)与[TrajEvolve](#trajevolve)可组合成从可执行环境合成到证据级、步骤级信用分配的长程 Agent RL 训练管线。
- **RobotEvolve**：[RLinf v0.4](#rlinf-v0-4)和[机器人集体学习范式](#item-15)提供了把真机部署轨迹汇入共享经验池、再以成功轨迹和失败上下文持续更新策略的工程路线。
- **ResearchEvolve**：[Claude Science](#claude-science)与[OptScientist](#optscientist)说明自主科研评测应优先采用湿实验命中率或定律恢复误差等外部可验证指标，而非只评价生成文本质量。
- **EvalEvolve**：[DecisionPivot](#decisionpivot-llm)和[智能体脚手架优化：能力唤起还是能力扩展？](#item-32)可用于构建分层诊断指标，将总体准确率拆为覆盖范围、概率排序、校准度和困难任务表现。
- **Awesome-RSI**：[奖励错设会削弱思维链可监控性](#item-27)表明 RSI 安全监控不能依赖思维链自述，应加入奖励描述训练、独立行为审计和不可被被优化系统修改的外部告警。
- **HumanEvolve**：[辩论可纠正人类判断，却难以改善弱模型监督](#item-72)提示可扩展监督必须区分人类与模型监督者，不能直接把对人有效的辩论机制迁移给弱模型裁判。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-21/  

