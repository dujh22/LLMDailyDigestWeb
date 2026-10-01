# 2026-09-30 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进从模型迭代转向“脚手架—实验—验证”全栈闭环**：除 AI 深度参与研发的 [Naive-N0.5-Flash](#naive-ai-ai-naive-n0-5-flash) 外，[RSI-Master](#rsi-master) 用结构化实验约束自主后训练，而 [审计脚手架而非检查点](#item-114) 进一步指出，持续突破上限依赖扩展工具、验证器与任务分解所定义的可达空间。
- **智能体评测加速走向动态、过程化与真实部署驱动**：今天出现大量长程、工具、GUI、科研和安全基准，其中 [TraceDance](#tracedance) 从线上不良轨迹自动造题，[WebPageBench](#webpagebench-ui) 用事件日志与可控 UI 变体验证行为，[SEABench](#seabench) 则纵向审计自进化更新带来的安全失配。
- **长期智能体的核心竞争点集中到记忆、状态与上下文治理**：[连续上下文管理](#item-58) 和 [FlowState](#flowstate-llm) 分别以逐轮压缩和语义执行状态降低上下文成本，[GenMem](#genmem) 与 [MemDream](#memdream) 则把稳定寻址、主动诊断和持续修复纳入记忆演化闭环。
- **多智能体扩展同时暴露协作质量、通信与群体安全问题**：[Noam Brown谈多智能体扩展与递归自我改进](#noam-brown) 强调并行测试时计算和弱脚手架下的协作涌现，[SAGE](#sage) 与 [BaRe-Mem](#bare-mem) 分别探索动态专家路由和可靠性记忆，而 [共享载体 AI 病毒](#item-50) 展示了持久化记忆跨智能体传播攻击的现实风险。
- **后训练研究密集攻关蒸馏、信用分配与能力边界课程**：从单 Token 稀疏监督的 [极端稀疏监督以单Token更新提升大模型推理能力](#token)，到解耦信用方向与幅度的 [DCSD](#dcsd)、在能力边界持续造题的 [Frontier Learning](#frontier-learning)，共同指向更少监督、更准归因和更高样本效率。
- **自主科研从创意生成迈向可验证、可复现实验闭环**：[AI Has Taste](#ai-has-taste) 展示数学选题—证明—审查闭环，[Quine](#quine) 和 [DoAtlas-2](#doatlas-2) 将世界模型、因果设计与真实实验验证用于生物医学发现，[MechBench](#mechbench-ai) 则开始区分现象拟合与真正的机制发现。

## 对当前研究的启发
- **Awesome-RSI**：[审计脚手架而非检查点](#item-114) 与 [RSI-Master](#rsi-master) 表明 RSI 应重点记录可达编辑空间、实验 DAG 和验证约束，而不能只比较连续检查点的分数增长。
- **DataEvolve**：[AutoDataBench](#autodatabench) 可作为自生成训练任务的逐样本验收框架，[Frontier Learning](#frontier-learning) 则提供用遗憾信号持续把数据分布推向模型能力边界的方法。
- **EnvironmentEvolve**：[F4R](#f4r) 将真实失败重建为针对性仿真环境，[阿里云 Agent Sandbox](#agent-sandbox) 提供可并发、可恢复的隔离执行底座，两者可组合成失败驱动的环境生产闭环。
- **EvalEvolve**：[TraceDance](#tracedance)、[WebPageBench](#webpagebench-ui) 与 [SEABench](#seabench) 分别提供部署故障造题、等价界面变体和纵向演化审计机制，可共同支撑动态 Agent 基准的生成与有效性校验。
- **EvolveLLM**：[仅靠自我回溯微调提升智能体，无需强化学习](#item-36) 说明可直接把模型自产的失败回溯转化为在线微调信号，为低成本持续学习提供替代 RL 的路线。
- **EvolveLRM**：[DCSD](#dcsd) 和 [ReSPO](#respo) 分别从步骤信用校准与离策略梯度饥饿切入，可用于提升推理模型自蒸馏及轨迹复用阶段的训练稳定性。
- **Groom**：[TokenCast](#tokencast-llm) 的分段 Token 成本预测与 [AgentPerfBench](#agentperfbench) 的真实轨迹负载可结合，用于建立按规划、工具调用和恢复阶段归因的过程级 Token 利用率指标。
- **HarnessEvolve**：[ContextEvo](#contextevo)、[EvoCUE](#evocue) 和 [Harness Learning](#harness-learning) 分别展示上下文策略、局部控制程序及完整求解流程的自适应，可形成多粒度 harness 演化体系。
- **JevEvolve**：[论点与署名](#item-83) 揭示快评估器也会受来源—立场一致性偏差影响，因此 Jev 式低延迟裁判在持续校准时应加入来源反事实样本与偏差审计。
- **LogicEvolve**：[SPRING](#spring-smt) 用 SMT 求解器验证中间步骤并奖励有效新演绎，为逻辑能力自进化提供了比纯模型裁判更可靠的过程奖励。
- **MemoryEvolve**：[GenMem](#genmem) 的稳定符号地址、[MemDream](#memdream) 的离线主动修复与 [修复后的智能体经验能否迁移至相关任务](#item-157) 的迁移评估共同提示，记忆演化需同时优化可寻址性、故障预防和跨任务真实效用。
- **ResearchEvolve**：[MechBench](#mechbench-ai) 对“规律恢复”和“机制发现”的区分可作为科研智能体评测核心维度，而 [COEVOLVE](#coevolve) 的证据迁移机制可扩大并行假设搜索而不破坏分支独立性。
- **SwarmEvolve**：[BaRe-Mem](#bare-mem) 说明可用在线可靠性后验动态控制顾问影响，[同质 LLM 辩论中的崩塌与纠正测量](#llm-3) 则提供区分群体纠错与多数意见崩塌的过程级评价方法。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-30/  

