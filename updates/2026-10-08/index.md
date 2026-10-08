# 2026-10-08 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **智能体 Harness 开始从人工设计走向受约束的递归演化**：研究同时覆盖抑制迭代过拟合的 [RRSI：正则化智能体 Harness 递归自我改进框架](#rrsi-harness)、将专用脚手架经验重写为通用轨迹的 [RSR：递归自我重写扩展复杂任务执行轨迹](#rsr)、证据驱动的 [EVISKILL：以可回放证据驱动智能体技能演化](#eviskill)，以及自动组合专业智能体的 [Raven：面向可组合智能体的 Harness 之 Harness](#raven-harness-harness)。
- **持续学习的焦点转向闭环稳定性与记忆可信度**：[自生成反馈破坏测试时训练的长期稳定性](#item-26) 证明独立真实数据验证可阻断长期闭环退化，[MemAdapter：反事实适应缓解记忆诱导型谄媚](#memadapter) 与 [RealCompanion：真实纵向对话中的人类理解评测](#realcompanion) 则分别给出记忆校准方法和最长 120 天的真实评测。
- **推理能力提升更依赖结构先验和跨域迁移**：[SAGE以结构信号纠正长程推理偏差](#sage) 借助代数与双曲结构将 Lean 验证通过率提升至近 8 倍，[NAT-ARC：自然图像预训练迁移至ARC视觉推理](#nat-arc-arc) 则展示自然图像视觉先验向抽象推理迁移的可行性。
- **动态评测与自主科研闭环同步推进**：[AutoSciBench：自主生成并迭代适配科学智能体评测基准](#autoscibench) 让任务难度随能力演进，[语言模型发现更快的分子几何弛豫算法 AutoSella](#autosella) 展示智能体发现可泛化新算法的实例，而 [OpenAI 公开 722 篇 AI 生成数学手稿](#openai-722-ai) 将正确性验证与规模化质量筛选推到前台。
- **规模扩展同时带来收益边界与治理压力**：[万级多智能体扩展：能力增益、协作机制与对齐风险](#item-7) 指出群体收益主要来自并行测试时计算且呈次线性，[Hinton等22人警告RSI或触发智能爆炸](#hinton-22-rsi) 则把 AI 研发自动化反馈环的可见性、部署约束和治理机制列为紧迫议题。

## 对当前研究的启发
- **Awesome-RSI**：[RRSI](#rrsi-harness) 的候选生成与筛选正则化可作为抑制 RSI 基准过拟合和复杂度膨胀的具体机制，[自生成反馈破坏测试时训练的长期稳定性](#item-26) 进一步说明每轮更新前必须引入独立外部验证。
- **HarnessEvolve**：[RRSI](#rrsi-harness)、[RSR](#rsr) 与 [Raven](#raven-harness-harness) 分别提供受约束搜索、成功轨迹迁移和模块化编排三种 Harness 演化路径，可据此拆分统一的演化与评测接口。
- **EvolveLLM**：[RSR](#rsr) 表明可将异构脚手架产生的成功经验重写为通用训练轨迹，为模型吸收 Harness 层能力而不绑定特定执行框架提供方案。
- **EvolveLRM**：[SAGE](#sage) 说明在稀疏长程推理中注入可验证的代数结构和几何先验，可能比单纯增加采样或强化学习规模更有效。
- **LogicEvolve**：[NAT-ARC](#nat-arc-arc) 将自然图像预训练迁移到 ARC，提示逻辑能力进化可探索视觉表征先验与离散规则验证器的结合。
- **MemoryEvolve**：[MemAdapter](#memadapter) 的反事实校准与 [RealCompanion](#realcompanion) 的纵向证据溯源评测，可分别用于控制错误记忆影响和检验远程记忆是否被恰当调用。
- **EvalEvolve**：[AutoSciBench](#autoscibench) 通过求解轨迹和评判反馈持续生成新任务，为构建随智能体能力自动调难且不依赖固定题库的动态基准提供了直接范式。
- **EnvironmentEvolve**：[AutoSciBench](#autoscibench) 可将轨迹失误转化为下一轮科学任务生成信号，适合作为环境难度追踪模型能力边界的实现基础。
- **ResearchEvolve**：[AutoSella](#autosella) 证明智能体能够在收敛与跨分子泛化约束下自动改写科研算法，提示自主科研应把可执行验证和分布外测试嵌入发现闭环。
- **SwarmEvolve**：[万级多智能体扩展](#item-7) 的次线性收益结论表明群体演化不应只扩大智能体数量，而应重点优化任务可并行性、通信结构与奖励对齐。
- **DataEvolve**：[自生成反馈破坏测试时训练的长期稳定性](#item-26) 显示纯自生成数据闭环会累积退化，数据飞轮应在提交训练更新前保留独立真实数据门控。
- **Groom**：[EVISKILL](#eviskill) 的可回放证据卡和显式证据关联可用于把技能复用收益归因到具体执行片段，而非仅依据智能体自述或最终成功率。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-08/  

