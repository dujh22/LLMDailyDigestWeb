# 2026-09-30 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从概念验证走向系统化工程：[Naive AI 开源 AI 研发模型 Naive-N0.5-Flash](#naive-ai-ai-naive-n0-5-flash)展示 AI 深度参与研发闭环，[RSI-Master：以结构化实验引导自主模型改进](#rsi-master)以研究 DAG 和受约束实验降低作弊，而[审计脚手架而非检查点：智能体编程递归自我改进的平稳性二分](#item-114)进一步指出持续突破依赖扩展工具、验证器与任务分解所定义的可达空间。
- Harness 自进化成为能力迁移与长程适应的关键路径：[EvoIn：融合演化与内化的智能体微调框架](#evoin)将脚手架中演化出的流程内化进模型，[ARISE：面向能力缺口演化的智能体强化学习](#arise)则让评估准则、技能和训练样本围绕未解决能力协同演化。
- 智能体评测明显转向真实轨迹、动态任务与自进化闭环：[TraceDance：从真实部署轨迹自动构建智能体行为基准](#tracedance)从线上缺陷反向生成评测，[AutoDataBench：评测智能体能否生成自我改进所需数据](#autodatabench)直接衡量数据飞轮能力，[MechBench：评测 AI 科研智能体的机制发现能力](#mechbench-ai)则区分规律拟合与真正的机制发现。
- 多智能体扩展开始同时关注协作收益与信息可靠性：[Noam Brown谈多智能体扩展与递归自我改进](#noam-brown)讨论并行 Agent 的测试时扩展与协作涌现，[BaRe-Mem：面向稳健自适应智能体咨询的贝叶斯可靠性记忆](#bare-mem)通过在线估计顾问可靠性抑制误导信息。
- 自主科研继续向可验证闭环推进：[AI Has Taste：从数学反例搜索走向自主出题](#ai-has-taste)以多智能体完成选题、证明、反例搜索和审查，MechBench 则为科研系统是否发现底层机制提供了更严格的测量标尺。
- 推理训练、安全执行与基础设施同步补强：[SPRING：SMT 求解器引导的逻辑推理过程奖励](#spring-smt)引入可验证的中间步骤奖励，[潜空间推理涌现可泛化的循环搜索算法](#item-43)展示递归潜空间搜索的长度泛化；与此同时，[阿里云 Agent Sandbox：面向智能体的云上安全执行底座](#agent-sandbox)提供生产级隔离，而[共享载体 AI 病毒：跨智能体记忆跳跃攻击](#item-50)揭示持久化共享状态带来的新型传播风险。

## 对当前研究的启发
- **Awesome-RSI**：[审计脚手架而非检查点](#item-114)与[RSI-Master](#rsi-master)共同提示，RSI 清单应重点区分“固定搜索空间内优化”与“可达操作空间自身扩展”，并纳入实验作弊和策略锁定的审计维度。
- **HarnessEvolve**：[EvoIn](#evoin)提供了“先在脚手架中演化、再内化为模型能力”的可执行路线，可用于研究 Harness 改进能否跨任务、跨模型稳定迁移。
- **EvalEvolve**：[TraceDance](#tracedance)可作为从真实部署失败持续生成动态基准的模板，而[AutoDataBench](#autodatabench)把自进化所需数据的生产效率与验收质量纳入了评测对象。
- **DataEvolve**：[AutoDataBench](#autodatabench)表明数据自进化不能只评最终训练增益，还应逐样本测量任务可执行性、验收通过率与生产成本。
- **MemoryEvolve**：[BaRe-Mem](#bare-mem)说明长期记忆不仅要存储经验，还可持续维护来源可靠性后验，以控制错误信息在多智能体协作中的影响权重。
- **SwarmEvolve**：[Noam Brown谈多智能体扩展](#noam-brown)与[BaRe-Mem](#bare-mem)分别给出并行协作扩展和不可靠成员治理的思路，可共同用于设计规模扩大后仍稳健的群体协议。
- **ResearchEvolve**：[AI Has Taste](#ai-has-taste)展示了从失败研究路线中产生可证伪猜想的闭环，而[MechBench](#mechbench-ai)可用于检验这种闭环究竟发现了机制还是仅复现经验规律。
- **EnvironmentEvolve**：[Agent Sandbox](#agent-sandbox)的 MicroVM 隔离、状态恢复和弹性并发可作为可执行、可复现训练环境服务化的工程参考。
- **EvolveLLM**：[ARISE](#arise)将能力缺口识别、评估准则和技能训练协同演化，为持续自我改进中的自动课程构造提供了具体方案。
- **EvolveLRM**：[潜空间推理涌现可泛化的循环搜索算法](#item-43)提示可将“是否学得可重复执行的搜索回路”作为判断潜空间推理能否越过训练深度的重要指标。
- **LogicEvolve**：[SPRING](#spring-smt)展示了用 SMT 求解器验证中间演绎并形成过程奖励的路径，可同时增强逻辑训练信号的正确性、细粒度和可审计性。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-30/  

