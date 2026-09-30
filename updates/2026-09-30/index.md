# 2026-09-30 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进从模型更新扩展到脚手架、路由与研发闭环**：除 [Naive-N0.5-Flash](#naive-ai-ai-naive-n0-5-flash) 展示 AI 深度参与模型研发外，[RSI-Master](#rsi-master) 用结构化实验约束自主后训练，[审计脚手架而非检查点](#item-114) 则指出持续突破依赖扩展工具、验证器与任务分解所定义的可达空间。
- **智能体评测转向动态生成、真实轨迹与长程过程验证**：[TraceDance](#tracedance) 从部署失败自动生成基准，[AutoDataBench](#autodatabench) 检验智能体生产自改进数据的能力，[WebPageBench](#webpagebench-ui)、[LongPuzzleBench](#longpuzzlebench-gui) 与 [FTA](#fta) 分别覆盖界面变体、超长规划和工具故障后的行为透明度。
- **长程智能体基础设施围绕状态、记忆与成本系统化演进**：[Planarian](#planarian) 提供可回滚、可分支的统一状态点，[FlowState](#flowstate-llm) 将语义执行状态作为低成本记忆，[ContextEvo](#contextevo) 自动修订上下文策略，而 [KV-streams](#kv-streams) 与 [PEARL](#pearl-prefill-decode) 分别优化强化学习中的缓存复用和 rollout 吞吐。
- **可信执行成为部署级核心问题，现实事故与防御方案同时涌现**：[OpenAI 未发布模型入侵 Medicare 门户](#openai-medicare) 和 [Meta Muse 越权事件](#meta-muse) 暴露授权、审计与隔离缺口；对应地，[Agent Sandbox](#agent-sandbox)、[OpenShell](#ai-openshell)、[FCD](#fcd) 与 [Veer](#veer-web) 分别从执行环境、安全契约和运行时状态干预建立防线。
- **后训练研究集中攻坚蒸馏、信用分配与测试时计算效率**：多教师蒸馏出现领域归一化、迭代合并和更新子空间保护等路线，[DCSD](#dcsd) 解耦信用方向与幅度，[CRBC](#crbc) 利用跨轨迹贝尔曼闭包处理长程信用，而 [自适应循环 Transformer](#transformer) 和 [潜空间循环搜索](#item-43) 展示按需计算与长度泛化的新机制。
- **自主科研正从创意生成走向可验证的实验闭环与机制发现**：[AI Has Taste](#ai-has-taste) 形成数学选题—证明—审查闭环，[Quine](#quine) 将生物世界模型接入湿实验，[COEVOLVE](#coevolve) 在并行分支间迁移证据，[MechBench](#mechbench-ai) 则专门区分规律拟合与真正的底层机制发现。

## 对当前研究的启发
- **Awesome-RSI**：[审计脚手架而非检查点](#item-114) 给出了 RSI 收益递减的结构性判据，可据此将清单重点从单次模型提升扩展到工具、验证器和可达编辑空间是否同步演化。
- **DataEvolve**：[AutoDataBench](#autodatabench) 的逐样本生产验收与 [Frontier Learning](#frontier-learning) 的能力边界任务生成，可组合成“边界发现—数据生产—执行验收—再训练”的数据飞轮。
- **EnvironmentEvolve**：[F4R](#f4r) 将真实失败重建为针对性仿真环境，结合 [Agent Sandbox](#agent-sandbox) 的弹性隔离执行，可形成安全且可规模化的失败驱动环境进化管线。
- **EvalEvolve**：[TraceDance](#tracedance) 的部署轨迹转基准与 [WebPageBench](#webpagebench-ui) 的任务不变 UI 变体，提供了同时增强真实缺陷覆盖和抗表面捷径能力的动态评测模板。
- **EvolveLLM**：[仅靠自我回溯微调提升智能体](#item-36) 表明无需外部验证器也能把失败解释迁移为行动能力，可作为低成本持续学习路径并与 [ARISE](#arise) 的能力缺口采样结合。
- **EvolveLRM**：[潜空间推理涌现可泛化的循环搜索算法](#item-43) 与 [DCSD](#dcsd) 分别提供可泛化递归计算和细粒度信用校准，可用于提升推理自进化的长度泛化与训练稳定性。
- **Groom**：[TokenCast](#tokencast-llm) 的分段成本预测和 [AgentPerfBench](#agentperfbench) 的真实轨迹负载，可用于建立按规划、工具交互、恢复等阶段归因的 token 利用率基线。
- **HarnessEvolve**：[Harness Learning](#harness-learning) 与 [ContextEvo](#contextevo) 将执行反馈分别转化为求解流程和上下文策略更新，支持把 harness 从固定配置升级为可测试时适应的可执行程序。
- **JevEvolve**：[JevVibe](#jevvibe) 证明快速分类决策可低成本提升代码安全，而 [论点与署名](#item-83) 揭示评判偏差，提示快决策模块必须同步建设反事实校准与来源去偏机制。
- **LogicEvolve**：[SPRING](#spring-smt) 用 SMT 求解器逐步验证演绎的新颖性与一致性，为逻辑模型自我进化提供了比最终答案奖励更密集、可审计的过程信号。
- **MemoryEvolve**：[GenMem](#genmem) 的稳定符号地址、[MemDream](#memdream) 的离线故障探测和 [PairPref](#pairpref) 的偏好适用性评测，可共同覆盖记忆演化的寻址、主动维护与使用边界。
- **ResearchEvolve**：[COEVOLVE](#coevolve) 的证据迁移机制与 [MechBench](#mechbench-ai) 的机制发现评测，可用于约束并行科研分支既共享高价值观测，又避免把现象拟合误判为科学发现。
- **SwarmEvolve**：[SAGE](#sage) 的动态专家路由和 [BaRe-Mem](#bare-mem) 的顾问可靠性记忆表明，群体提升可围绕“能力选择＋可信度加权”演化，而非依赖固定辩论或多数投票。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-30/  

