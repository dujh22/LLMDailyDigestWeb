# 2026-10-09 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从单体规则迭代扩展到多智能体与安全闭环：[Memento 3](#memento-3)以可修订规则手册和严格验证持续学习世界模型，[MASS](#mass)协同进化工作流与模型能力，[ReSI](#resi)则把自动红队、模型更新和能力保留纳入循环。
- 推理模型自进化开始精细控制数据质量与信用分配：[R-Quest](#r-quest)通过有效性、新颖性反馈抑制多轮自训练坍缩，[SCAPO](#scapo)利用半事实干预改善词元级信用分配，分别从训练数据和策略优化两端提升稳定性。
- 记忆、技能与环境形成经验驱动的持续学习主线：[AgentGarten](#agentgarten)提供可持续试错的代码化交互世界，[RoboRSI](#roborsi)以责任归因和验证后发布演化机器人技能，[Hippocam](#hippocam)则将连续经历整合为可复用的意图结构化长期记忆。
- 科研智能体的重点转向实验效率与证据可信：[语言模型作为 AI 研究世界模型](#item-31)预测实验干预结果，[DataSense-Bench](#datasense-bench-ai)评测高价值数据识别能力，[研究契约](#item-46)和[TRACE](#trace)分别约束科研声明与审计验证器脆弱性；OpenAI 批量发布 AI 证明引发的[数学界争议](#openai-ai)进一步凸显验证和署名问题。
- 多智能体与执行系统的收益和风险同步放大：[协作引发种群失控阈值](#item-24)刻画群体越过临界点后的自强化扩张，[HarnessSQL](#harnesssql-sql)则展示把真实执行环境完整引入训练可显著改善智能体准确率与泛化。
- 热点延伸集中于世界模型、长视频与生成加速，包括[Long-WAM](#long-wam)、[UniWAM](#uniwam)、[SGF+](#sgf)和[GRACE](#grace)，显示长程时序建模与推理成本仍是多模态系统的共同瓶颈。

## 对当前研究的启发
- **Awesome-RSI**：[Memento 3](#memento-3)、[MASS](#mass)与[ReSI](#resi)共同表明，RSI 框架应同时显式进化知识载体、优化流程和安全机制，并以严格验证及能力保留约束每轮更新。
- **EvolveLRM**：[R-Quest](#r-quest)的新颖性过滤与[SCAPO](#scapo)的半事实信用分配可组合成“高价值问题生成—稳定词元更新”的多轮推理自训练方案。
- **MemoryEvolve**：[Hippocam](#hippocam)的意图分层整合和[Memento 3](#memento-3)的可验证规则手册，为统一情景压缩、细节恢复与记忆修订提供了两类互补表示。
- **ResearchEvolve**：[语言模型作为 AI 研究世界模型](#item-31)可用于预算受限的实验预筛选，而[研究契约](#item-46)可把最终科研声明绑定到预先批准且可审计的执行证据。
- **EvalEvolve**：[DataSense-Bench](#datasense-bench-ai)将数据价值判断纳入科研智能体评测，[TRACE](#trace)则提供区分真实能力提升、验证器漏洞和运行随机性的必要审计流程。
- **EnvironmentEvolve**：[AgentGarten](#agentgarten)的确定性物理环境与实时渲染组合，以及[HarnessSQL](#harnesssql-sql)的真实执行训练，说明环境应同时满足高交互吞吐、可验证反馈和训练时原生接入。
- **SwarmEvolve**：[MASS](#mass)展示了群体工作流与模型可协同进化，但[协作引发种群失控阈值](#item-24)提示必须监测规模临界点并限制协作导致的自强化扩张。
- **HarnessEvolve**：[HarnessSQL](#harnesssql-sql)证明执行框架不应只是评测外壳，而可直接进入监督学习与强化学习；[TRACE](#trace)则要求同步披露和审计验证器行为。
- **LogicEvolve**：[SCAPO](#scapo)提供提升域外推理泛化的训练信号，而[数学家呼吁抵制 OpenAI 批量发布 AI 生成证明](#openai-ai)表明逻辑能力演化必须配套机器可检验证据、人工理解与署名规范。
- **DataEvolve**：[R-Quest](#r-quest)证明持续自训练的数据筛选不能只看可解性，还应显式估计新颖性以防问题分布和学习信号逐轮坍缩。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-09/  

