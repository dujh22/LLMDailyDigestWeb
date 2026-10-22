# 2026-10-22 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进走向模型、脚手架与环境协同演化**：[CoEvo-RSI](#coevo-rsi)直面模型与执行框架的“脑—身体”错配，[ScholarEvolve](#scholarevolve-agent-harness)从科研文献持续演化 Harness，[DeepEvolve](#deepevolve)则把技能蒸馏与开放世界未来预测纳入递归闭环。
- **长程智能体训练与评测基础设施同步升级**：[FlashNext-RL](#flashnext-rl)支持单节点最高 131K 上下文的 Agentic RL，[Environment Duels](#environment-duels-llm)让模型互相创作和求解环境，[SWE-DIVE](#swe-dive)与[FrontierCS 2](#frontiercs-2)分别覆盖动态多轮编程和开放式计算机科学研发。
- **长期记忆研究同时出现正反两条证据**：[MemoryTax](#memorytax)显示强模型自主搜索原始历史可能胜过昂贵的预构建记忆，而[Uni-Mem](#uni-mem)尝试通过在线策略优化和事件级信用分配端到端学习记忆写入与检索。
- **自主科研进入大规模并行实验阶段**：[数千个 GPT‑Rosalind 智能体并行挖掘全脑 CRISPR 图谱](#gpt-rosalind-crispr)以 1946 个智能体在 32 分钟内分析约 800 万细胞，展示了多智能体科研从工作流原型走向规模化假说生产的潜力。
- **模型、数据与推理系统共同瞄准长程效率**：[Step 5 Preview](#step-5-preview-agent)以百万 token、上下文压缩和可验证环境面向长程 Agent，[LongZero](#longzero)用零外部数据合成长上下文训练任务，[Dreaming Learning](#dreaming-learning)缓解递归合成数据坍缩，而[面向智能体的 KV 缓存工程](#item-246)把缓存取舍直接开放给智能体控制。

## 对当前研究的启发
- **Awesome-RSI**：[CoEvo-RSI](#coevo-rsi)表明 RSI 不应只迭代模型或脚手架，而应联合保留、选择和合并二者的历史状态以避免能力与执行机制错配。
- **AgentEvolve**：[DeepEvolve](#deepevolve)提供了“轨迹内化—技能蒸馏—开放世界再验证”的部署期经验闭环，可用于检验免参数或轻量参数更新下的持续自进化。
- **HarnessEvolve**：[ScholarEvolve](#scholarevolve-agent-harness)展示了从文献自动实现、组合并评估 Harness 算法的路径，而[SWE-DIVE](#swe-dive)可作为检验其多轮需求适应能力的动态环境。
- **AgentTrainEvolve**：[FlashNext-RL](#flashnext-rl)证明长程软件工程 Agent 的 131K 上下文强化学习可在单节点落地，为扩展多轮 Agentic RL 提供了直接的系统实现参考。
- **EnvironmentEvolve**：[Environment Duels](#environment-duels-llm)把环境生成器与求解器置于同一竞争—学习循环，可用于研究难度是否能随模型能力自动对齐。
- **EvalEvolve**：[SWE-DIVE](#swe-dive)和[FrontierCS 2](#frontiercs-2)将评测推进到动态用户交互与真实开放式研发任务，可作为静态单轮基准之外的高难度演化评测种子。
- **MemoryEvolve**：[MemoryTax](#memorytax)与[Uni-Mem](#uni-mem)共同提示应把“是否建立显式记忆”纳入可学习决策，并以成本—准确率而非单纯召回率评价记忆系统。
- **ResearchEvolve**：[数千个 GPT‑Rosalind 智能体并行挖掘全脑 CRISPR 图谱](#gpt-rosalind-crispr)说明科研智能体的关键扩展点已从单体推理转向任务切分、并行调度和可实验验证的假说汇总。
- **SwarmEvolve**：[数千个 GPT‑Rosalind 智能体并行挖掘全脑 CRISPR 图谱](#gpt-rosalind-crispr)提供了近两千智能体真实科研协作案例，可用于分析大规模并行中的任务拓扑、冗余控制与结果归因。
- **DataEvolve**：[LongZero](#longzero)与[Dreaming Learning](#dreaming-learning)分别给出零外部数据任务合成和高温自采样抗坍缩方案，可组合成兼顾覆盖度与长期稳定性的合成数据飞轮。
- **JevEvolve**：[Our Own Jev](#our-own-jev-lora)验证了以单次前向传播和自托管 LoRA 完成类型化判断的可行性，可直接用于低成本筛选智能体编程数据。
- **CacheEvolve**：[面向智能体的 KV 缓存工程](#item-246)将 drop 与 repos 变成智能体可调用动作，为从固定缓存策略转向任务反馈驱动的自主缓存管理提供了接口范式。
- **NewModel**：[Step 5 Preview](#step-5-preview-agent)把百万 token、端到端上下文压缩和可验证环境训练整合进开放权重模型，可作为长程 Agent 模型设计的新基线。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-22/  

