# 2026-11-13 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **部署期智能体自进化转向可验证的技能、记忆与脚手架协同**：[VbD](#vbd)以环境证据协同演化执行器和评估器，[HyperSkill](#hyperskill-grpo)演化可审计的超图技能库，[MIGRO](#migro)则实现跨模型长期记忆迁移。
- **智能体评测进一步暴露参考答案、停止策略和对抗审计的系统性缺陷**：[TestPrism](#testprism-coding-agent)将 Coding Agent 测试生成合格率从表面上的 59.67% 修正至 28.00%，[终止滞后](#item-32)揭示“已经解题却继续消耗”，而[能力隐藏压力测试](#item-47)表明固定检测器难以抵御自适应攻击。
- **强化学习研究聚焦长程信用分配、有效探索与训练范式辨析**：[TreeOPSD](#treeopsd)以树式信用分配提升深度研究智能体，[有效熵与 VEPO](#llm)约束探索集中于有效推理空间，[重新审视“RL 泛化、SFT 记忆”](#rl-sft-sft)则显示数据来源和解法多样性足以显著缩小乃至逆转二者差距。
- **形式验证开始同时支撑大型证明工程和新算法发现**：[Claude Code 形式化三元哥德巴赫猜想](#claude-code)在约 19.4 万行 Lean 工程中发现原证明错误，[AutoAssumption](#autoassumption-ml)进一步通过机器可检查的假设搜索发现新的缓存淘汰与剪枝算法。
- **推理系统与快决策模型继续压低智能体运行成本**：[TraceKV](#tracekv-kv)提供免训练、策略保持的低秩 KV 压缩，[Gemini Decision 1](#google-gemini-decision-1)则以单次前向传递完成多模态选择、评分和置信度输出。
- **热点延伸集中于跨模态表征、动态精度和智能体服务**：低相关性条目分别探索[柏拉图表征假说](#item-11)、[按需升至 8-bit 的解码](#8-bit)及[Evolving Infra](#evolving-infra-llm)，反映表征分析与推理基础设施仍在快速演进。

## 对当前研究的启发
- **AgentEvolve**：[VbD](#vbd)与[HyperSkill](#hyperskill-grpo)表明，冻结权重后可把主动验证、技能蒸馏和检索协议共同纳入部署期演化闭环。
- **AgentTrainEvolve**：[TreeOPSD](#treeopsd)将轮次信用估计、后验蒸馏和残差更新结合，可直接借鉴为长程 Agentic RL 的细粒度归因方案。
- **EvalEvolve**：[TestPrism](#testprism-coding-agent)和[能力隐藏压力测试](#item-47)共同说明，进化式评测必须引入多实现判定与自适应对手，不能依赖单一参考答案或固定攻击集。
- **HarnessEvolve**：[终止滞后](#item-32)提示 harness 应记录“首次正确时刻”、后续动作及答案回退，并把停止策略独立于最终成功率评估。
- **EvolveLRM**：[有效熵与 VEPO](#llm)提供了比原始输出熵更贴近有效推理探索的目标，而[RL 与 SFT 再比较](#rl-sft-sft)要求实验严格对齐 rollout 预算和数据多样性。
- **CodeEvolve**：[AutoAssumption](#autoassumption-ml)展示了“形式化假设放宽—证明重推导—代码生成—执行验证”的可复用算法进化闭环。
- **MemoryEvolve**：[MIGRO](#migro)的宿主适配接口与跨模型持久状态，为记忆从特定模型私产转为可迁移、可压缩的智能体资产提供了架构模板。
- **JevEvolve**：[Gemini Decision 1](#google-gemini-decision-1)验证了单次前向的结构化评分产品形态，可作为 Jev 快决策、置信度输出及慢模型升级路由的直接对标。
- **InfraEvolve**：[TraceKV](#tracekv-kv)说明可用策略校准信号自动分配低秩缓存预算，[AutoAssumption](#autoassumption-ml)则进一步证明缓存算法本身可以由智能体形式化搜索。
- **HumanEvolve**：[学生使用 AI 编写单元测试的研究](#item-40)表明效率提升可能伴随批判性检查和技能学习下降，产品评测应同时追踪交付质量与用户能力变化。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-13/  

