# 2026-10-08 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 智能体脚手架开始从“自动改写”转向受约束、可复用的系统演化：[RRSI](#rrsi-harness)抑制迭代过拟合与复杂度膨胀，[RSR](#rsr)将专用脚手架经验递归重写为通用训练轨迹，[EVISKILL](#eviskill)则以可回放证据沉淀和修正技能。
- 长周期自我改进的稳定性成为核心问题：[自生成反馈破坏测试时训练的长期稳定性](#item-26)揭示闭环更新会持续退化；[MemAdapter](#memadapter)与[超越记忆：用显式信念状态驱动长时程智能体](#item-41)分别从记忆校准和显式状态维护降低错误累积。
- 动态评测正覆盖科学任务与真实纵向交互：[AutoSciBench](#autoscibench)让任务难度随智能体能力自动演进，[RealCompanion](#realcompanion)则用最长 120 天真实对话检验远程记忆、相关性判断与过度推断。
- 推理能力提升更加依赖结构先验、跨域迁移和可审计状态：[SAGE](#sage)用代数与双曲结构显著改善长程推理，[NAT-ARC](#nat-arc-arc)将自然图像预训练迁移至抽象视觉推理，而[AlphaGo作者：LLM尚未掌握可审计的搜索式推理](#alphago-llm)强调搜索、证据验证和信念更新仍是关键缺口。
- 大规模多智能体并非简单堆叠即可获得线性收益：[万级多智能体扩展](#item-7)指出增益主要来自并行测试时计算且伴随奖励错配风险，[Raven](#raven-harness-harness)则尝试通过自动编排可组合 Harness 支撑跨域长程协作。
- 自动化科研同时展现可用成果与验证瓶颈：[AutoSella](#autosella)发现了可跨分子泛化的更快几何弛豫算法，而[OpenAI 公开 722 篇 AI 生成数学手稿](#openai-722-ai)将正确性验证和大规模科研产出的质量筛选推向前台。

## 对当前研究的启发
- **Awesome-RSI**：RRSI 的候选生成与筛选正则化，加上自生成反馈研究提出的独立真实数据验证，可组合为防止递归迭代追逐噪声和闭环退化的双重护栏。
- **HarnessEvolve**：RRSI、RSR 与 EVISKILL 分别提供约束演化、跨脚手架轨迹迁移和证据化技能修正机制，可用于构建“生成—迁移—验证”一体化 Harness 演进闭环。
- **DataEvolve**：自生成反馈在 128K token 更新中出现闭环退化，说明数据飞轮必须在每轮训练前设置独立真实数据验收，而不能仅依赖模型自身生成与评价。
- **EvolveLLM**：RSR 表明可把专用 Harness 的成功轨迹重写为通用模型训练数据，但应结合外部验证过滤重写过程中累积的自洽错误。
- **EvolveLRM**：SAGE 在可由 Lean 验证的长程任务上取得近 8 倍提升，说明把任务结构直接注入探索过程可作为纯奖励塑形之外的高效训练路线。
- **LogicEvolve**：NAT-ARC 的视觉先验迁移与显式搜索、证据验证、信念更新的主张共同指向“强表征先验＋可审计符号状态”的混合推理架构。
- **MemoryEvolve**：PoS 的显式信念状态、MemAdapter 的反事实校准和 RealCompanion 的纵向评测可串成记忆写入、冲突修复与长期有效性验证的完整链路。
- **EvalEvolve**：AutoSciBench 可依据求解轨迹和评判反馈持续生成更难任务，适合作为动态基准自动对准能力边界的实现模板。
- **ResearchEvolve**：AutoSella 证明智能体可产出具备收敛性与跨分子泛化的真实算法改进，而 722 篇数学手稿事件表明规模化产出必须配套形式验证、复现和价值筛选管线。
- **SwarmEvolve**：Raven 的模块化 Harness 编排可作为群体结构演化载体，但万级智能体分析提示优化目标应聚焦边际收益、通信成本和奖励错配，而非智能体数量。
- **EnvironmentEvolve**：HERA 的脚手架—环境协同演化表明，可将不确定情形和可靠拒答能力共同纳入自动课程，使环境难度演化同时服务能力与安全校准。
- **JevEvolve**：SSR 将开放式推理改为自然语言候选选择，为快决策模型承担高频搜索动作筛选、仅将低置信决策升级给慢模型提供了直接范式。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-08/  

