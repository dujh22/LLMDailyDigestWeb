# 2026-11-12 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进走向多层系统实装**：今天有 5 项工作覆盖模型结构、终端策略、训练环境、Harness 与基础设施，[机制干预](#ai-transformer)允许智能体热插拔自生成模块，[Terminal-RSI](#terminal-rsi)和[NeoHorse-1.5-Flash Preview](#neohorse-1-5-flash-preview-agent-rsi)则展示了长程执行与在线训练中的递归迭代。
- **Harness 与基础设施成为可演化对象**：[EvolveNet](#evolvenet-harness)通过并行改动、合并与回滚积累跨工作负载经验，[InfraRSI](#infrarsi)则把同类闭环用于分布式训练优化，表明系统级自进化正从概念验证进入可量化的工程收益阶段。
- **记忆与世界上下文强化部署后学习**：[WICL](#wicl)把仿真排练反馈固化为可跨场景、跨具身复用的任务记忆，[WikiTrace](#wikitrace)进一步用成败摘要和原始轨迹为记忆提供可核查证据，分别推进了经验获取与错误记忆修正。
- **自主科研形成“认知—实验—复现”闭环**：[Sage-Taiyi](#sage-taiyi)以元认知动态管理证据、假设和研究目标，[ProTEUS](#proteus)用物理约束世界模型与实验反馈完成蛋白质闭环进化，[ReproBridge](#reprobridge)则补齐科研成果的标准化复现载体。
- **评测重点转向复杂决策与隐性污染风险**：[MMDM](#mmdm)系统检验长上下文、大选项空间下的多任务决策能力，[FinDendro](#findendro)发现模型无法可靠声明自身时间知识边界，说明自我报告不能替代可审计的防泄漏设计。
- **热点延伸集中在生成模型与高效蒸馏**：9 条低相关性热点涵盖少步流式视频、端到端语音、3D 重建及在线蒸馏，例如[APEX](#apex)的条件迁移视频生成与[SplatAnything](#splatanything-3dgs)的跨场景 3DGS 归一化。

## 对当前研究的启发
- **SystemEvolve**：[机制干预](#ai-transformer)与[EvolveNet](#evolvenet-harness)分别把可热插拔模型模块和共享 Harness 纳入生成、验证与回滚闭环，可共同构成系统级自改写的分层搜索空间。
- **Awesome-RSI**：[Terminal-RSI](#terminal-rsi)使原本无法完成任务的 27B 智能体获得新能力，为判断 RSI 是否真正扩展能力边界提供了比同分布提分更有价值的案例。
- **AgentEvolve**：[EvolveNet](#evolvenet-harness)按改动作用范围合并多客户端经验，提示部署时自进化可从单智能体私有反思扩展到跨工作负载的共享 Harness 演化。
- **MemoryEvolve**：[WikiTrace](#wikitrace)将记忆结论绑定成败摘要与原始轨迹，为长期记忆加入可追溯核查和纠错机制，可直接缓解错误经验反复复用造成的退化。
- **RobotEvolve**：[WICL](#wicl)展示了冻结模型通过仿真排练生成任务记忆并跨具身迁移的路线，可作为无需参数更新的机器人持续适应模块。
- **AgentTrainEvolve**：[NeoHorse-1.5-Flash Preview](#neohorse-1-5-flash-preview-agent-rsi)把多模型差分诊断、环境进化和在线学习串联起来，为将执行失败稳定转化为课程与参数更新提供了完整范式。
- **InfraEvolve**：[InfraRSI](#infrarsi)以真实性能测量验证并沉淀跨硬件优化，结合[Flide](#flide)的精确状态分叉，可分别推进训练基础设施自搜索与决策推理状态复用。
- **ResearchEvolve**：[Sage-Taiyi](#sage-taiyi)的显式证据—假设监控与[ReproBridge](#reprobridge)的可执行成果封装，可用于同时提升科研智能体的研究策略调整能力和实验复现率。
- **EvalEvolve**：[FinDendro](#findendro)证明知识截止日期和模型自我声明都不足以排除泄漏，提示动态评测必须依赖外部时间隔离、数据溯源与可执行审计。
- **PhysicalEvolve**：[ProTEUS](#proteus)以快速物理约束预测筛选候选、再由真实实验反馈修正世界模型，为物理世界自进化提供了高成本实验下的有效闭环模板。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-12/  

