# 2026-10-08 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进转向“受约束、可验证的闭环”**：从抑制基准过拟合与复杂度膨胀的 [RRSI：正则化智能体 Harness 递归自我改进框架](#rrsi-harness)，到统一训练、评测和沙箱执行的 [RSIGym：灵活的递归自我改进研究环境](#rsigym)，研究重点正从能否自改进转向如何保证迭代稳定且收益真实。
- **AI 科研产出规模快速增长，但可靠复现仍是瓶颈**：[OpenAI 公开 722 篇 AI 生成数学手稿](#openai-722-ai) 与 [Bolzano：从专家引导证明搜索到自动求解开放问题](#bolzano) 展示规模化数学研究潜力，而 [PaperBenchX：AI端到端论文完整复现率仅13.98%](#paperbenchx-ai-13-98) 表明完整执行、证据溯源和独立核验仍远落后于结果生成。
- **评测开始与能力、环境和验证器共同演化**：[AutoSciBench：自主生成并迭代适配科学智能体评测基准](#autoscibench) 根据求解轨迹持续调节任务，[AppWorld 与 WorkArena 任务验证器盲点审计](#appworld-workarena) 则揭示执行式评分器可能放过错误副作用，动态出题与验证器审计需要同步推进。
- **经验与技能演化强调“证据化写入”**：[EVISKILL：以可回放证据驱动智能体技能演化](#eviskill) 通过证据卡、定向重执行和显式关联持续修正技能，显示非参数更新式学习也能形成可审计、可复用的能力积累。
- **推理训练同时优化探索质量与结构偏差**：[SAGE以结构信号纠正长程推理偏差](#sage) 用代数和双曲结构引导长程搜索，[ExpDis：解耦 RLVR 中的探索与优化](#expdis-rlvr) 则将新颖轨迹探索与学生策略更新分离，以减少探索扩张对训练稳定性的损害。
- **快决策模型进入“搜索监督—动态路由”阶段**：[Jev：从概率判断到搜索决策与多教师蒸馏](#jev) 验证轻量概率模型可为搜索提供低成本监督，[System Switch：快速决策模型何时应停下来思考？](#system-switch) 进一步表明快慢切换的关键是置信度校准，但离线路由收益仍需转化为闭环任务成功。

## 对当前研究的启发
- **Awesome-RSI**：[RRSI](#rrsi-harness) 与 [LLM 自我改进循环中的赢家诅咒](#llm-3) 共同提示，应把复杂度正则、独立留出评估和保守接受规则设为每轮自改进的默认门槛。
- **HarnessEvolve**：[模型与 Agent Harness 适配关系的系统评测](#agent-harness) 表明不存在跨模型普适最优 Harness，因此演化搜索应显式联合建模模型习惯、任务类型、反馈机制和上下文管理。
- **ResearchEvolve**：[Bolzano](#bolzano) 的并行搜索与验证智能体可作为开放问题研究流水线模板，但 [PaperBenchX](#paperbenchx-ai-13-98) 和 [InnovationEval](#innovationeval) 要求最终评价绑定隔离复现、证据溯源与防择优上报机制。
- **EvalEvolve**：[AutoSciBench](#autoscibench) 可用于构建随能力增长的任务生成闭环，而 [AppWorld 与 WorkArena 验证器审计](#appworld-workarena) 提示每次基准演化都应配套副作用检测和变异测试。
- **MemoryEvolve**：[EVISKILL](#eviskill) 提供了“证据卡—重执行—技能修订”的可落地记忆写入协议，可避免仅凭成功轨迹把偶然策略固化为长期技能。
- **EvolveLRM**：[SAGE](#sage) 与 [ExpDis](#expdis-rlvr) 表明可分别从结构先验和策略解耦两端改善长程探索，适合组合为“独立探索器生成、结构验证器筛选、学生策略蒸馏”的训练流程。
- **JevEvolve**：[Jev](#jev) 和 [System Switch](#system-switch) 说明快模型的核心指标不应只有分类准确率，还应评估概率校准、升级慢思考的边际价值及闭环执行收益。
- **EnvironmentEvolve**：[RSIGym](#rsigym) 的服务化环境适合作为多组件协同演化底座，而 [AppWorld 与 WorkArena 验证器审计](#appworld-workarena) 说明环境生成后必须经过源码引导的验证器压力测试。
- **Groom**：[模型与 Agent Harness 适配关系的系统评测](#agent-harness) 为过程级 token 归因提供了关键实验设计依据，即比较 Harness 时必须控制模型—任务适配，并分解反馈与上下文管理造成的成本差异。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-08/  

