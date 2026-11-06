# 2026-11-06 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 智能体演化开始从人工设计脚手架转向“演化脚手架—能力回迁—策略复用”闭环：[Harness-S](#harness-s) 将同源脚手架挽救出的能力迁回单一策略，[Strategist](#strategist) 则把可执行推理蓝图作为跨任务持续演化的对象。
- 递归自我改进与自主科研进一步强调真实反馈和闭环验证：[WeightLoop](#weightloop) 依据实验结果直接编程权重，[自递归软硬件脚手架驱动自主光学实验](#item-64) 将硬件、软件、模型与实验协议一并纳入递归修订，[FrontierPhysics](#frontierphysics) 则揭示科研智能体仍受推理严谨性和专家直觉制约。
- 自进化评测从最终得分转向泛化与证据可靠性：[SelfImprove-Bench](#selfimprove-bench) 用 G0–G4 阶梯检验能力增益能否迁移，而 [Agent-as-a-Judge 中的确认偏差](#agent-as-a-judge) 表明即使拥有决定性工具证据，权威归因提示仍可能显著扭转判决。
- 长期记忆研究聚焦“状态修订”与“压缩后的安全保持”：[StateGraph](#stategraph) 用依赖图和反事实验证选择性失效过时记忆，[ARCBench](#arcbench) 则发现规则即使被摘要保留，也可能在后续工具调用中被错误解释为授权。
- 后训练的能力边界受到集中审视：[RLVR只优化解题路径选择，未提升内在推理能力](#rlvr-4) 指向采样重加权而非表征扩展，[在策略蒸馏用于强化学习后能力巩固的泛化局限](#item-14) 则揭示分布内保持可能以分布外遗忘为代价。
- 推理系统优化同时推进算法自动发现、长上下文稀疏化与可执行评测：[SpecPilot](#specpilot) 自动搜索投机解码方案，[递归稀疏注意力](#item-22) 以对数选择成本外推至百万词元，[ServerBench](#serverbench-llm) 则检验编码智能体能否自主设计正确且高效的专用服务系统。

## 对当前研究的启发
- **AgentEvolve**：[Strategist](#strategist) 表明可将推理流程外化为可检索、测试和修订的蓝图，为冻结参数条件下积累跨任务策略提供了直接实现路径。
- **AgentTrainEvolve**：[Harness-S](#harness-s) 提供了先用演化脚手架生成成功经验、再通过强化学习将能力迁回单体策略的训练范式。
- **Awesome-RSI**：[WeightLoop](#weightloop) 与 [SelfImprove-Bench](#selfimprove-bench) 分别补上实验反馈驱动的自修改机制和分层泛化评测，可用于检验 RSI 是否产生可迁移而非局部的真实改进。
- **ResearchEvolve**：[自递归软硬件脚手架驱动自主光学实验](#item-64) 说明科研闭环应允许智能体同时修订实验装置、控制软件、模型和协议，而 [FrontierPhysics](#frontierphysics) 可作为端到端能力诊断模板。
- **EvalEvolve**：[Agent-as-a-Judge 中的确认偏差](#agent-as-a-judge) 说明主动取证不足以保证可靠评判，评测系统还需隔离先验提示并测试证据与权威归因冲突时的稳健性。
- **MemoryEvolve**：[StateGraph](#stategraph) 可用于实现依赖感知的记忆级联失效，而 [ARCBench](#arcbench) 提醒摘要评测必须验证规则是否被正确执行，不能只检查文本是否保留。
- **GeneralizeEvolve**：[RLVR只优化解题路径选择，未提升内在推理能力](#rlvr-4) 与 [在策略蒸馏用于强化学习后能力巩固的泛化局限](#item-14) 共同要求把 OOD 策略迁移和内部表征变化纳入后训练增益判定。
- **SystemEvolve**：[SpecPilot](#specpilot) 和 [ServerBench](#serverbench-llm) 展示了以真实吞吐、成本与正确性为反馈，让智能体自动发现推理算法并设计服务系统的完整闭环。
- **CacheEvolve**：[递归稀疏注意力](#item-22) 的树状 KV 缓存与分层候选选择提供了固定预算下实现百万词元外推的新结构路线。
- **RobotEvolve**：[PyRUA-DataFarm](#pyrua-datafarm-llm) 可用于低成本扩展带精确动作标注的真机训练数据，[CUE](#cue) 则提供了以主动物理交互持续校准数字孪生的 sim-to-real 闭环。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-06/  

