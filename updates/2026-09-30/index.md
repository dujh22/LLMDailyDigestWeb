# 2026-09-30 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进从模型迭代走向脚手架与系统协同演化**：从 AI 主导研发闭环的 [Naive-N0.5-Flash](#naive-ai-ai-naive-n0-5-flash)、结构化实验驱动的 [RSI-Master](#rsi-master)，到强调扩展可达编辑空间的 [审计脚手架而非检查点](#item-114) 与联合演化路由和技能的 [RSI-Router](#rsi-router)，研究重点转向如何突破固定改进机制的收益上限。
- **长程智能体的训练与执行基础设施加速成熟**：[Agent Sandbox](#agent-sandbox) 提供大规模隔离执行底座，[Planarian](#planarian) 支持状态快照、回滚与分支探索，[KV-streams](#kv-streams)、[PEARL](#pearl-prefill-decode) 和 [Nereus](#nereus) 则分别优化上下文缓存、Rollout 吞吐与动态后训练资源调度。
- **动态、过程化智能体评测成为主线**：大量工作从真实部署失败、可执行事件和可控变体构造评测，包括 [TraceDance](#tracedance)、[WebPageBench](#webpagebench-ui)、[AutoDataBench](#autodatabench) 与 [Codoku](#codoku)；同时 [Arena 裁判审计](#arena-llm) 和 [同质 LLM 辩论测量](#llm-3) 表明最终分数可能掩盖评判偏差与过程崩塌。
- **长期记忆转向可压缩、可演化且可治理的状态系统**：[连续上下文管理](#item-58) 与 [FlowState](#flowstate-llm) 降低长程上下文成本，[GenMem](#genmem) 和 [MemDream](#memdream) 支持记忆持续演化与主动修复，而 [EP-Mem](#ep-mem) 与 [共享载体 AI 病毒](#item-50) 分别凸显披露控制和跨智能体记忆传播风险。
- **智能体安全聚焦执行前干预、契约绑定与真实事故**：[FCD](#fcd) 防止工具实现切换造成安全语义漂移，[Veer](#veer-web) 与 [SEAD](#sead) 在动作执行前调整或验证状态；与此同时 [Medicare 门户入侵](#openai-medicare) 和 [Muse 越权事件](#meta-muse) 暴露了沙箱、授权、隐私与通报机制的现实缺口。
- **自主科研与多智能体搜索继续扩展到真实科学闭环**：[AI Has Taste](#ai-has-taste) 形成数学选题—证明—审查闭环，[Quine](#quine) 和 [DoAtlas-2](#doatlas-2) 分别连接湿实验药物筛选与因果生物医学发现，[自主量化因子挖掘](#item-55) 则显示同等预算下并行搜索优于顺序搜索。

## 对当前研究的启发
- **Awesome-RSI**：[审计脚手架而非检查点](#item-114) 给出了固定可达编辑集合必然收益递减的理论判断，可据此把 RSI 评测重点从单次模型增益扩展到工具、验证器与任务分解空间是否持续增长。
- **DataEvolve**：[AutoDataBench](#autodatabench) 的逐样本生产验收和 [通过预测误差将内部表征转化为模型改进](#item-65) 的无标签价值估计，可组合为“生成—验收—价值归因”的数据自进化闭环。
- **EnvironmentEvolve**：[F4R](#f4r) 将真实执行失败重建为定向仿真环境，提供了以失败轨迹自动生成课程并开展仿真—现实联合训练的具体路径。
- **EvalEvolve**：[TraceDance](#tracedance) 从部署缺陷自动生成针对性基准，而 [WebPageBench](#webpagebench-ui) 用事件日志和等价 UI 变体验证稳健性，两者可共同支撑真实轨迹驱动、可执行且抗表面捷径的动态评测。
- **EvolveLLM**：[EvoIn](#evoin) 先在脚手架中演化决策流程再将其内化为模型轨迹，为验证“外部工作流能力能否稳定迁移进模型参数”提供了直接范式。
- **EvolveLRM**：[潜空间推理涌现可泛化的循环搜索算法](#item-43) 与 [DCSD](#dcsd) 分别说明递归潜空间计算和方向—幅度解耦信用分配可能提升长度泛化与训练稳定性。
- **Groom**：[TokenCast](#tokencast-llm) 的分段 Token 成本预测和 [AgentPerfBench](#agentperfbench) 的真实轨迹负载可用于建立按规划、工具交互与上下文增长阶段归因的 Harness Token 利用率基线。
- **HarnessEvolve**：[ContextEvo](#contextevo) 通过轨迹失效分析定向更新上下文策略，结合 [AutoRef](#autoref) 的冻结模型脚手架搜索，可用于研究 Harness 改进对模型排名与任务收益的独立贡献。
- **JevEvolve**：[JevVibe](#jevvibe) 展示了快分类器在安全代码修复中的低成本前置引导价值，而 [来源—立场一致性偏差](#item-83) 提醒持续校准时必须控制身份与来源特征造成的判断捷径。
- **LogicEvolve**：[SPRING](#spring-smt) 用 SMT 求解器验证中间演绎并生成过程奖励，为构建可验证、可扩展且能惩罚无信息步骤的逻辑自进化训练信号提供了方案。
- **MemoryEvolve**：[MemDream](#memdream) 的离线主动探测修复与 [修复后的智能体经验能否迁移至相关任务](#item-157) 的多基线评估，可用于区分记忆修复、经验复用和真实跨任务能力迁移。
- **ResearchEvolve**：[AI Night-Scientist](#ai-night-scientist) 以强化学习控制何时偏离常规推理，[PEAR](#pear-autoresearch) 以证据状态和置信度门控验证，两者可结合以平衡科研创意探索与可靠实验收敛。
- **SwarmEvolve**：[BaRe-Mem](#bare-mem) 通过在线可靠性记忆调节顾问影响，[SAGE](#sage) 动态选择并迁移优势智能体策略，为群体系统联合演化成员可信度、路由和协作结构提供了互补机制。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-30/  

