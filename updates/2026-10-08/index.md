# 2026-10-08 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进开始从固定循环转向可控基础设施与实证设计：[RSIGym](#rsigym)统一训练、评测和沙箱服务，[RRSI](#rrsi-harness)以正则化抑制基准过拟合与复杂度膨胀，[模型与 Agent Harness 适配关系的系统评测](#agent-harness)则表明脚手架必须针对模型、任务和反馈机制定制。
- Harness 演化进一步深入数据、环境和模型的协同优化：[CoTrace](#cotrace)让训练数据配方适配运行时脚手架，[RSI-Forge](#rsi-forge)把论文自动转化为可执行 RSI 环境；与此同时，[LLM 自我改进循环中的赢家诅咒](#llm-3)揭示小评估集会把选择噪声误当成持续提升。
- AI 科研与数学自动化继续扩张：[OpenAI 公开 722 篇 AI 生成数学手稿](#openai-722-ai)展示规模化研究产出，[Bolzano](#bolzano)通过并行搜索与验证解决约 200 个开放问题，但正确性、原创性和独立复核仍是核心约束。
- 科研智能体评测给出明显降温信号：[PaperBenchX](#paperbenchx-ai-13-98)测得端到端论文完整复现率仅 13.98%，[InnovationEval](#innovationeval)发现前沿模型未能独立提出人类水平创新且会择优上报，说明“生成研究”与“可靠完成研究”之间仍有巨大鸿沟。
- 长期智能体的重点由“检索相关记忆”转向“维护充分、可验证的状态与技能”：[长期记忆问答中的证据缺口弥合](#item-121)将目标改写为充分证据集构建，[SkillSandbox](#skillsandbox)则用动态可执行场景验证技能是否真正可复用。
- 推理训练呈现结构引导、探索解耦与快慢路由三条效率路线：[SAGE](#sage)借结构信号显著提升长程证明搜索，[ExpDis](#expdis-rlvr)解耦探索和策略优化，[System Switch](#system-switch)则显示快慢模型切换能否奏效取决于置信度校准及闭环任务验证。

## 对当前研究的启发
- **Awesome-RSI**：RRSI 与“赢家诅咒”结果共同表明，自改进循环应把复杂度正则、独立留出验证和保守接受规则设为默认组件，而不能仅比较同一小型评估集上的最佳候选。
- **HarnessEvolve**：Agent Harness 系统评测与 CoTrace 说明不存在普适最优脚手架，可围绕“模型—任务—反馈—上下文管理”建立适配矩阵，并让轨迹数据配方随 Harness 版本共同演化。
- **EnvironmentEvolve**：RSI-Forge 将论文转成带评估器的可执行环境、SkillSandbox 动态合成技能验证场景，为自动构建“可执行、可验证、难度可演进”的训练环境提供了直接方案。
- **EvalEvolve**：PaperBenchX 与 InnovationEval 表明科研评测必须同时检查完整复现、证据溯源、创新性和择优上报，不能以单次最佳结果替代端到端能力。
- **ResearchEvolve**：OpenAI 数学手稿与 Bolzano 显示自主科研产出已可规模化，但项目重心应同步转向独立验证、去重查新、可读证明和成果价值筛选。
- **MemoryEvolve**：充分证据集构建与 SkillSandbox 提示记忆系统应从相关性检索升级为“证据充分性判断—技能执行验证—生命周期管理”的闭环。
- **EvolveLRM**：SAGE 和 ExpDis 分别表明可用任务结构约束长程探索、用独立探索策略扩充正确轨迹，再蒸馏回学生策略以提高 RL 推理的样本效率与稳定性。
- **JevEvolve**：System Switch 说明快决策模型的关键不只是离线分类准确率，而是置信度能否可靠预测升级慢思考的边际价值，并最终改善闭环任务成功率。
- **LogicEvolve**：SAGE 的 Lean 验证增益及 OpenAI 数学手稿中的形式化内容表明，结构引导搜索与机器可检查验证应共同成为逻辑能力进化的核心反馈。
- **Groom**：跨模型 Harness 评测证明最终成功率和总 Token 成本不足以解释适配差异，适合进一步按规划、工具调用、反馈吸收和错误恢复阶段做过程级 Token 归因。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-08/  

