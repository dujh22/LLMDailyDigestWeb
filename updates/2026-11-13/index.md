# 2026-11-13 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **部署期智能体自进化**成为主线：[VbD](#vbd) 通过 Actor—Evaluator 脚手架协同演化实现无外部反馈改进，[HyperSkill](#hyperskill-grpo) 以可审计超图技能库实现免训练提升，[MIGRO](#migro) 则让长期经验可跨模型迁移。
- **智能体训练向长程信用分配与“脚手架＋权重”联合演化推进**：[TreeOPSD](#treeopsd) 用树式轮次信用估计提升 Deep Research，[知识在脚手架、可靠性在权重](#item-26) 展示了仅依赖部署日志协同更新技能规则与 LoRA 的路径。
- **评测重点从最终得分转向过程有效性与持续改进真实性**：[TestPrism](#testprism-coding-agent) 揭示单参考实现会将测试生成成功率高估一倍以上，[RSI 持续进步评测](#rsi-rsibench-data-s-gym) 与 [RSI-PDEbench](#rsi-pdebench) 分别补充版本轨迹审查和科学任务中的递归改进验证，[终止滞后](#item-32) 则暴露编码智能体解题后继续消耗资源的问题。
- **形式化验证开始直接参与数学与系统算法发现**：[Claude Code 形式化三元哥德巴赫猜想](#claude-code) 在大规模 Lean 工程中发现原证明错误，[AutoAssumption](#autoassumption-ml) 更进一步通过放宽可验证假设自动发现 KV 淘汰和权重剪枝算法。
- **训练与系统效率出现可直接复用的方法**：[重新审视“RL 泛化、SFT 记忆”](#rl-sft-sft) 表明数据来源、规模和解法多样性可使 SFT 追平甚至超过 RL；[TraceKV](#tracekv-kv) 与 [KernelMosaic](#kernelmosaic-cuda-kernel) 分别推进无训练 KV 压缩和可验证 CUDA Kernel 自动优化。
- **热点延伸**集中于跨模态表征对齐、按需精度解码、GPU 科学计算求解器及智能体推理服务调度，但相关性较低，适合作为外围趋势观察。

## 对当前研究的启发
- **AgentEvolve**：[VbD](#vbd) 与 [HyperSkill](#hyperskill-grpo) 表明冻结权重后仍可通过执行—评估闭环和可审计技能库持续提升，可作为部署期自进化的两类互补基线。
- **AgentTrainEvolve**：[TreeOPSD](#treeopsd) 的树式轮次信用估计可用于改善长程 Agentic RL 的稀疏奖励归因，而 [脚手架与 LoRA 协同演化](#item-26) 提供了经验同时写入显式策略和参数可靠性的训练范式。
- **Awesome-RSI**：[RSI 持续进步评测](#rsi-rsibench-data-s-gym) 与 [RSI-PDEbench](#rsi-pdebench) 给出了“版本轨迹＋预算控制＋历史峰值＋未见任务”审查框架，可用于区分真实持续改进与单次刷榜。
- **EvalEvolve**：[TestPrism](#testprism-coding-agent) 证明评测必须覆盖多样化正确与错误实现，否则单一参考答案会系统性高估智能体能力。
- **Groom**：[终止滞后](#item-32) 提供了“首次正确时刻—实际停止时刻”的过程级指标，可直接用于归因 Coding Agent 在重复验证和无效探索上的 token 浪费。
- **MemoryEvolve**：[MIGRO](#migro) 将经验定义为独立于宿主模型的持久状态，为跨模型共享、压缩和迁移长期记忆提供了清晰接口范式。
- **GeneralizeEvolve**：[重新审视“RL 泛化、SFT 记忆”](#rl-sft-sft) 提醒泛化对比必须对齐 rollout 预算和数据混合，不能把数据覆盖差异误归因于训练算法。
- **JevEvolve**：[日志化 Bandit 反馈决策头](#bandit) 展示了在缺少完整标签时持续校准动作概率与选择性风险的可行方案，适合快决策模型从部署日志中在线改进。
- **CodeEvolve**：[Claude Code 形式化证明](#claude-code) 与 [KernelMosaic](#kernelmosaic-cuda-kernel) 共同说明，可执行验证器既能发现人类工程中的隐蔽错误，也能形成代码智能体的数据与优化飞轮。
- **InfraEvolve**：[AutoAssumption](#autoassumption-ml) 将系统优化转化为“放宽形式化假设—重新证明—生成并实测代码”的闭环，可扩展到缓存、剪枝与算子算法的自动发现。
- **CacheEvolve**：[TraceKV](#tracekv-kv) 的策略校准、敏感度感知分解和全局秩分配提供了按推理策略重要性分配固定 KV 预算的具体实现路线。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-13/  

