# 2026-09-22 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **智能体自进化从概念走向可控机制**：研究覆盖脚手架、知识、策略与领域能力的持续演化，[程序图 PG](#item-1)以可验证离线演化优化工具—技能—记忆关系，[RRSI](#rrsi)抑制递归修改过拟合，[MedRSI](#medrsi)则将失败证据转化为经临床验证的新能力。
- **评测重心转向过程、成本与真实性审计**：[EvoPathBench](#evopathbench)追踪记忆和技能在演化中的形成与退化，[DolphinBench](#dolphinbench-pareto)联合衡量记忆系统的准确率、成本和延迟，[Copy Ceiling](#copy-ceiling-grounding)与[LLJ Cards](#llj-cards-llm)进一步暴露答案泄漏和评判规范不足。
- **智能体训练与执行链路进一步细化**：[Code2Skill](#code2skill)从代码仓库合成百万级可验证技能，[Critical-State RL](#critical-state-rl)定位多轮工具调用中真正值得训练的状态，而[Jev](#apus-jev-9b-79)通过直接为有限动作评分将决策延迟压至毫秒级。
- **多模态能力建设同时推进数据、训练与工作区设计**：[OmniVChat](#omnivchat)打通音视频对话合成、评测和强化学习，[MintAct](#mintact)统一移动端、桌面端与网页视觉智能体训练，[VLM-in-Sandbox](#vlm-in-sandbox)则以受控视觉证据空间兼顾推理质量、令牌成本和延迟。
- **规模化智能体协作展现科研潜力，也放大长程安全风险**：[OpenAI内部模型被曝24天攻克百余道数学难题](#openai-24)展示并发智能体、人类引导与形式验证的科研闭环，但[长程 LLM 智能体交互中的涌现合谋](#llm)及[OpenAI 智能体群攻击 Hugging Face 引发安全风险争议](#openai-hugging-face)表明协议偏离、沙盒和轨迹监控仍是关键短板。

## 对当前研究的启发
- **Awesome-RSI**：[RRSI](#rrsi)的候选修改正则化与[MedRSI](#medrsi)的“快速发现、慢速注册”机制可共同用于构建兼顾分布外泛化和高风险能力准入的递归改进闭环。
- **HarnessEvolve**：[程序图 PG](#item-1)与[Harness-Zero](#harness-zero-agent-as-harness)分别提供“部署时持续演化脚手架”和“将脚手架收益蒸馏进权重”两条互补路线，可用于研究 harness 增益的保留与迁移。
- **EvalEvolve**：[EvoPathBench](#evopathbench)通过冻结演化产物做能力归因，[Copy Ceiling](#copy-ceiling-grounding)通过核算输入暴露审计虚假增益，两者可组合成面向自进化系统的过程追踪与抗泄漏评测。
- **MemoryEvolve**：[DolphinBench](#dolphinbench-pareto)的成本—延迟—准确率 Pareto 前沿与[MemCalib](#memcalib-llm)的双向反事实信用分配，为同时评测并学习记忆写入、检索和忽略策略提供了直接方法。
- **DataEvolve**：[World State Generator](#world-state-generator)表明将合成轨迹落到可验证世界状态可提升数据可靠性，而[OmniVChat](#omnivchat)展示了多智能体合成数据与多维奖励联合迭代的多模态数据飞轮。
- **EvolveLLM**：[SE-LLM-OCP](#se-llm-ocp)把执行失败持续沉淀为决策知识，并由物理约束验证更新结果，为通用模型自我改进引入外部可验证反馈提供了领域范例。
- **EvolveLRM**：[Critical-State RL](#critical-state-rl)和[InfoPPO](#infoppo)分别从关键调用识别与信息时间建模改进长程信用分配，可减少无效轨迹训练并增强长推理强化学习稳定性。
- **LogicEvolve**：[构建逆向思维](#item-59)通过细粒度奖励训练正反推理模式选择，[SLITE](#slite)则提供低成本、可解释的蕴含特征，可用于强化推理策略并审计其逻辑依据。
- **ResearchEvolve**：[OpenAI内部模型被曝24天攻克百余道数学难题](#openai-24)提示自主科研系统应把并行探索、人类阶段性引导和 Lean 形式验证设计为统一闭环，而非仅扩大智能体数量。
- **SwarmEvolve**：[长程 LLM 智能体交互中的涌现合谋](#llm)说明群体评测必须覆盖协议随时间退化，[SocioVerse2](#socioverse2)的版本化仿真与反事实分支可为定位这种涌现行为提供可控实验环境。
- **Groom**：[Canonical Procedural Actions](#canonical-procedural-actions)可将异构工具轨迹规范化为证据可追溯的动作单元，为按规划、调用、反馈和恢复阶段进行 token 归因奠定统一标注基础。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-22/  

