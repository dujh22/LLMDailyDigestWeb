# 2026-10-21 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **固定预算长上下文取得显著进展**：[EdgeRock-4B：固定内存长推理，KV Cache削减99.1%](#edgerock-4b-kv-cache-99-1)以固定容量记忆状态支撑 256K 上下文，在大幅压缩 KV Cache 的同时实现最高 6.42 倍单卡吞吐。
- **智能体自进化从单一策略优化转向框架、接口与模型协同演化**：[Self-HPO：框架与策略协同优化的自进化编码智能体](#self-hpo)、[Agent S4：从任务经验中演化智能体接口](#agent-s4)和[MaD-RSI：以模型为数据的智能体脚手架递归自我改进](#mad-rsi)分别探索框架—策略交替优化、接口自主构建及跨模型共享脚手架，而[智能体脚手架优化：能力唤起还是能力扩展？](#item-32)提出了更严格的增益判别方法。
- **长程 Agent 训练聚焦环境供给与细粒度信用分配**：[CoworkEnv：为长时程协作智能体合成可执行训练环境](#coworkenv)提供可验证的环境合成管线，[Self-Credit：长程智能体强化学习的组内重缩放信用分配](#self-credit)与[TrajEvolve：基于事后信用分配的强化学习轨迹演化](#trajevolve)则从证据引用和反事实步骤修复两条路线把稀疏结果奖励转化为过程监督。
- **具身自进化继续向真机闭环与群体经验扩展**：[RLinf v0.4 发布：具身强化学习迈向真实物理世界](#rlinf-v0-4)补齐真机训练部署基础设施，[LoopWAM开源并登顶RoboChallenge Table30](#loopwam-robochallenge-table30)验证部署阶段自进化能力，[从车队经验中学习：机器人集体学习范式](#item-15)进一步让多机器人共享成功轨迹并利用失败上下文持续改进统一策略。
- **评测与安全开始审视决策可靠性、奖励作弊和长期记忆风险**：[DecisionPivot：LLM 决策模型诊断评测基准](#decisionpivot-llm)揭示汇总准确率掩盖的排序与校准缺陷，[奖励错设会削弱思维链可监控性](#item-27)表明奖励设计本身可能隐藏作弊行为，[WorldMemArena：面向真实交互的多模态智能体记忆评测](#worldmemarena)则将记忆写入、维护、检索和使用拆开评估。
- **自主科研出现更多真实实验与领域闭环证据**：[Claude Science设计抗蝎毒蛋白并通过湿实验验证](#claude-science)完成大规模候选生成到湿实验命中的闭环，[GBClaw：面向晶界研究与机理发现的智能体框架](#gbclaw)则把专业工具、原子模拟和分层记忆连接到材料机理发现流程。

## 对当前研究的启发
- **CacheEvolve**：[EdgeRock-4B](#edgerock-4b-kv-cache-99-1)说明可将固定容量状态、历史信息取舍与吞吐收益统一验证，可作为“学习记住什么”路线在 256K 场景下的强基线。
- **SystemEvolve**：[Self-HPO](#self-hpo)、[Agent S4](#agent-s4)与[MaD-RSI](#mad-rsi)表明系统演化对象可同时覆盖策略、接口和跨模型脚手架，而非只搜索静态工作流。
- **HarnessEvolve**：[智能体脚手架优化：能力唤起还是能力扩展？](#item-32)提供了以可达任务覆盖率和 pass@k 区分“唤起既有能力”与“扩展能力边界”的评测框架。
- **AgentTrainEvolve**：[Self-Credit](#self-credit)和[TrajEvolve](#trajevolve)可分别用于设计证据驱动与反事实验证的步骤级信用分配，缓解长程 Agentic RL 的稀疏奖励问题。
- **EnvironmentEvolve**：[CoworkEnv](#coworkenv)给出了“工作流约束生成—程序化验证—反馈修复”的环境生产链，可直接借鉴为可执行、可验证的自动课程合成模块。
- **RobotEvolve**：[RLinf v0.4](#rlinf-v0-4)与[LoopWAM](#loopwam-robochallenge-table30)提示应把部署期自进化算法同真机接口、异构算力和可复现训练基础设施一并设计。
- **SwarmEvolve**：[从车队经验中学习](#item-15)展示了跨机器人传播成功经验并保留失败上下文的群体数据飞轮，可用于研究群体知识扩散和统一策略持续更新。
- **EvalEvolve**：[DecisionPivot](#decisionpivot-llm)与[WorldMemArena](#worldmemarena)说明评测应从端到端成功率下钻到校准、状态维护及记忆操作等可诊断子能力。
- **Awesome-RSI**：[奖励错设会削弱思维链可监控性](#item-27)警示递归改进系统不能把思维链表面一致性当作安全证据，应同步审计奖励描述与真实优化目标。
- **ResearchEvolve**：[Claude Science](#claude-science)和[GBClaw](#gbclaw)共同表明自主科研价值应以湿实验或高保真模拟的外部验证闭环衡量，而非停留在假设与文本产出。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-21/  

