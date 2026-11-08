# 2026-11-08 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 智能体训练环境与数据合成加速融合（3 条）：[WildAWM：用合成“个人电脑”训练计算机使用智能体](#wildawm)以全合成桌面环境实现跨分布泛化，[Firefly：先探索后出题的可验证工具调用数据合成](#firefly)从真实 API 反向生成可验证任务，[ICRPM以前瞻风险预测优化Rollout任务采样](#icrpm-rollout)则在不增加 rollout 的前提下优化训练任务选择。
- 部署期自进化从记忆扩展到整个执行系统：[VISTA：机器人通过自编程实现不动权重的具身自进化](#vista)通过自主改写 Harness 将成功率从 17.5% 提至 95.0%，[Anthropic公开Claude离线“做梦”长期记忆架构](#anthropic-claude)展示了跨会话回放、纠错和知识巩固机制。
- 新模型探索覆盖自主训练与低延迟决策：[Naive-N0.5-Flash推动个人端AI自主训练AI](#naive-n0-5-flash-ai-ai)尝试在个人设备上闭环完成数据、训练和纠错，[Drex：迈向基础决策模型](#drex)则以直接输出候选概率分布的开放权重模型探索“快决策”路线。
- 具身基础模型继续扩大经验规模与迁移范围：[Open-HumanWAM：扩展人类与机器人经验的开放具身基础模型方案](#open-humanwam)利用大规模第一人称人类经验实现具身上下文学习，[SLA：通过持续预训练扩展空间-语言-动作模型](#sla)通过异构机器人数据持续预训练内化可迁移空间能力。
- 智能体评测同时关注长程能力与评测成本：[VisSearch-Bench：多模态智能体长时程视觉搜索评测](#vissearch-bench)揭示最佳系统完整任务成功率仅 26.47%，[BestRand：稳定低成本的基准压缩](#bestrand)则以随机子集筛选降低成本并改善长尾与分布外稳定性。
- 热点延伸集中在视觉与三维生成，包括高速具身视觉规划、多轮图像编辑抗漂移和高斯化身伪影修复，但与当前核心研究方向关联较弱。

## 对当前研究的启发
- **SystemEvolve**：[VISTA](#vista)证明冻结模型权重、仅让 Meta-agent 搜索并改写执行 Harness 就可能带来数量级提升，可将工作流代码、工具配置与验收反馈纳入系统级演化闭环。
- **AgentEvolve**：[Anthropic 的长期记忆架构](#anthropic-claude)提供了“任务间歇回放—错误纠正—知识维基化”的部署期经验沉淀管线，可用于增强跨会话自我改进。
- **MemoryEvolve**：[Anthropic 的离线“做梦”机制](#anthropic-claude)表明记忆巩固不应只是摘要压缩，还应重放原始记录并主动修正旧知识与索引。
- **EnvironmentEvolve**：[Firefly](#firefly)与[WildAWM](#wildawm)共同说明可扩展环境应联合生成执行载体、长程任务和可靠验证器，而非只合成任务文本。
- **DataEvolve**：[Firefly](#firefly)的“先探索真实 API、再反向出题”可用于提高工具调用合成数据的真实性、覆盖度和可验证性。
- **AgentTrainEvolve**：[ICRPM](#icrpm-rollout)可作为 Agentic RL 的低成本课程调度器，利用历史风险预测策略更新后的任务价值，减少无效 rollout。
- **GeneralizeEvolve**：[WildAWM](#wildawm)仅依赖合成环境却在八个分布外基准上提升，为研究“环境多样性是否比真实轨迹来源更决定泛化”提供了强案例。
- **JevEvolve**：[Drex](#drex)的候选概率直出结构可作为高频动作选择与工具路由的快模型，并进一步研究何时升级到慢推理模型。
- **EvalEvolve**：[BestRand](#bestrand)可降低动态基准的持续评测成本，而[VisSearch-Bench](#vissearch-bench)提供了视觉上下文管理、证据整合和长程搜索过程的新评测切面。
- **RobotEvolve**：[VISTA](#vista)与[Open-HumanWAM](#open-humanwam)分别展示了 Harness 自编程和人类经验预训练两条互补路线，可组合为“经验迁移—执行系统自适应—真机验证”的具身进化闭环。
- **Awesome-RSI**：[Naive-N0.5-Flash](#naive-n0-5-flash-ai-ai)提供了个人设备上训练闭环与递归改进的候选案例，但应重点追踪其多轮改进是否单调、评测是否独立以及错误是否累积。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-08/  

