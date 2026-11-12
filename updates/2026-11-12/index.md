# 2026-11-12 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从策略层扩展到系统结构与运行时：[机制干预](#ai-transformer)可按内部信号热插拔模块，[Terminal-RSI](#terminal-rsi)通过自我重写获得新的长程执行能力，[EvolveNet](#evolvenet-harness)则以并行演化、合并和回滚持续改进共享 Harness。
- 记忆与具身学习进一步结合：[WICL](#wicl)把仿真排练反馈固化为可跨场景复用的任务记忆，[WikiTrace](#wikitrace)为记忆绑定成败摘要和原始轨迹以抑制错误累积，[Embodied First Exam](#embodied-first-exam)则规模化检验编码智能体的真实物理控制能力。
- 自主科研开始强调元认知、实验闭环与可复现交付：[Sage-Taiyi](#sage-taiyi)动态监控证据、假设和研究目标，[ProTEUS](#proteus)以实验反馈闭环搜索蛋白质突变，[ReproBridge](#reprobridge)把代码、环境和执行决策封装为智能体可复现的研究成果。
- 评测工作聚焦复杂决策、污染风险和确定性验证：[MMDM](#mmdm)系统刻画快决策模型在长上下文多任务场景中的边界，[FinDendro](#findendro)揭示模型无法可靠自报时间知识边界，[MotionGraphicsBench](#motiongraphicsbench)展示程序化验证优于主观模型评判。
- 基础设施优化正形成“智能体搜索—真实执行—经验沉淀”闭环：[InfraRSI](#infrarsi)自动生成并验证分布式训练优化，[Flide](#flide)以精确状态分叉复用加速分支决策，[在线策略蒸馏的训练—推理不匹配容忍度](#item-19)则给出 FP8 与异步 rollout 的可用效率预算。
- 热点延伸主要集中在少步视频生成、端到端语音和生成式世界演化，包括 [APEX](#apex)、[WaveGen](#wavegen) 与 [EvoWorld](#evoworld)，但与当前核心自进化主线的直接关联较弱。

## 对当前研究的启发
- **SystemEvolve**：[机制干预](#ai-transformer)与 [EvolveNet](#evolvenet-harness)表明系统演化可同时搜索模型内热插拔模块和模型外 Harness，并用作用域合并与验证回滚控制退化。
- **Awesome-RSI**：[Terminal-RSI](#terminal-rsi)提供了“自我重写产生原先不存在的任务能力”的强案例，可用于区分真正能力扩展与既有能力的提示释放。
- **AgentEvolve**：[WICL](#wicl)和 [WikiTrace](#wikitrace)提示部署期经验不应只压缩成结论，而应保留仿真反馈、任务成败与原始轨迹以支持跨场景复用和记忆纠错。
- **MemoryEvolve**：[WikiTrace](#wikitrace)给出了可直接采用的证据关联记忆单元，使错误记忆能够被追溯、核查和修订，而非持续污染后续任务。
- **InfraEvolve**：[InfraRSI](#infrarsi)证明跨硬件性能经验、全局性能建模和真实执行验证可以组成训练基础设施的自动进化闭环。
- **AgentTrainEvolve**：[在线策略蒸馏的训练—推理不匹配容忍度](#item-19)说明 rollout 精度和同步方式存在可测预算，可据模型特性联合搜索 FP8 配置与异步训练策略。
- **ResearchEvolve**：[Sage-Taiyi](#sage-taiyi)的元认知控制与 [ReproBridge](#reprobridge)的标准化成果封装可结合，使科研智能体不仅调整假设和实验，还能交付可审计复现的完整证据链。
- **EvalEvolve**：[FinDendro](#findendro)说明抗污染评测不能依赖模型自报知识边界，而应结合外部时间证据与 [MotionGraphicsBench](#motiongraphicsbench)式确定性验证器。
- **JevEvolve**：[MMDM](#mmdm)可用于定位快决策模型在长上下文、巨大候选空间和逻辑依赖下的失效边界，为快慢模型升级路由提供训练信号。
- **RobotEvolve**：[WICL](#wicl)展示了冻结模型通过仿真排练形成任务记忆并跨具身迁移的路径，可作为低成本真机持续改进前的经验生成层。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-12/  

