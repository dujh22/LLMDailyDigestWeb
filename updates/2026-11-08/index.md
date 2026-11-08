# 2026-11-08 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 智能体训练环境与数据合成成为今日主线（3 项）：[WildAWM：用合成“个人电脑”训练计算机使用智能体](#wildawm)验证纯合成电脑环境可带来跨基准泛化，[Firefly：先探索后出题的可验证工具调用数据合成](#firefly)则打通真实 API 探索、反向出题与离线验证闭环。
- 智能体持续进化覆盖推理与训练两侧：[Anthropic公开Claude离线“做梦”长期记忆架构](#anthropic-claude)以跨会话回放、纠错和知识维基沉淀经验，[Naive-N0.5-Flash推动个人端AI自主训练AI](#naive-n0-5-flash-ai-ai)进一步尝试让个人设备自主完成训练全流程。
- 快决策模型与训练效率均有新进展：[Drex：迈向基础决策模型](#drex)用候选概率分布替代开放式生成以降低决策延迟，[ICRPM以前瞻风险预测优化Rollout任务采样](#icrpm-rollout)则在不增加 rollout 的前提下优化高风险任务选择。
- 具身基础模型继续向大规模异构经验与迁移泛化推进：[Open-HumanWAM：扩展人类与机器人经验的开放具身基础模型方案](#open-humanwam)融合 5 万小时第一人称人类经验与机器人数据，[SLA：通过持续预训练扩展空间-语言-动作模型](#sla)探索将三维空间理解内化为可迁移能力。
- 评测侧开始同时关注长程能力与成本：[VisSearch-Bench：多模态智能体长时程视觉搜索评测](#vissearch-bench)揭示当前系统完整任务成功率仍不足三成，[BestRand：稳定低成本的基准压缩](#bestrand)则改善低成本子集评测的长尾误差；热点延伸集中在视觉规划、多轮图像编辑和三维化身修复。

## 对当前研究的启发
- **EnvironmentEvolve**：WildAWM 与 Firefly表明环境生成应联合设计可执行载体、长程任务和可靠验证器，并用分布外表现检验合成环境是否真正扩展能力。
- **AgentTrainEvolve**：Firefly的“先探索 API、再反向出题”可直接用于构造工具调用课程，而 ICRPM 可作为无需额外 rollout 的风险感知任务调度器。
- **MemoryEvolve**：Claude的离线“做梦”架构提供了可落地的记忆巩固范式，即定期回放原始轨迹、纠正旧结论并重组为可检索的分层知识。
- **GeneralizeEvolve**：WildAWM仅凭合成环境就在八个分布外基准上提升，为研究“环境多样性是否带来真实跨域泛化”提供了强实验样板。
- **JevEvolve**：Drex直接输出有限候选的概率分布，适合作为快决策模块的开放基线，并可进一步研究其与慢推理模型之间的动态升级边界。
- **EvalEvolve**：VisSearch-Bench与BestRand分别补足长时程多模态智能体的过程能力测量和低成本稳定评测，可组合用于持续更新但预算受限的评测体系。
- **RobotEvolve**：Open-HumanWAM与SLA说明可将大规模第一人称人类视频和异构机器人数据统一纳入持续预训练，以增强跨本体迁移与具身上下文学习。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-08/  

