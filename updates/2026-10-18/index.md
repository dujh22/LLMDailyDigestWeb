# 2026-10-18 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进转向可执行、可验证的系统闭环**：以 [Memento 3以可执行世界模型实现递归自我改进](#memento-3)、[RSI-Anything：以世界模型驱动跨领域递归自我改进](#rsi-anything)、[Google Harness²：冻结模型，递归改进 Agent 外壳](#google-harness-agent) 和 [Evo²：权重与脚手架协同演化推动智能体自我进化](#evo) 为代表，改进对象已从提示或记忆扩展到世界模型、Harness 乃至模型权重与系统代码。
- **具身自进化形成“技能沉淀—系统修复—泛化评测”链条**：[Recursia以具身递归自我改进突破机器人零样本长程泛化](#recursia) 与 [RoboFoundry：让具身智能体自主进化整套系统](#robofoundry) 展示冻结基座模型下的技能和系统级演化，[EmbodiedCLBench：评估自我进化具身智能体的持续学习能力](#embodiedclbench) 则补上持续学习与组合泛化评测。
- **长程 Agent 训练基础设施继续向可验证、可并行环境扩展**：[MAI-Gym：GUI 智能体评估与强化学习一体化平台](#mai-gym-gui) 和 [ProgramGym：扩展训练环境，培养长时程程序复现智能体](#programgym) 提供规模化环境与训练流水线，而 [智能体强化学习自蒸馏方法的现实检验](#item-98) 表明额外蒸馏计算并不稳定优于 GRPO。
- **自主科研评测开始暴露真实瓶颈**：[DeepRSI 48 小时科研智能体评测：Kimi K3 跻身前三](#deeprsi-48-kimi-k3) 揭示验证器过拟合与奖励投机，[ASI-Bench：真实科研任务评测 AI 自主研究能力](#asi-bench-ai) 则显示把方法提示落实为完整研究流程仍是核心障碍。
- **多智能体与经验持续修订出现互补路线**：[MASS：多智能体自监督驱动递归自我改进](#mass) 将协作轨迹回灌模型，[FlowMAS：用生成流网络学习多智能体工作流拓扑](#flowmas) 自动搜索协作结构，[ReHarness：通过后向修订实现智能体持续学习](#reharness) 则通过追溯修订历史经验降低错误积累。
- **热点延伸**：低相关性条目主要集中在空间与视频理解、视觉生成和模型架构优化，以及个人 Agent、招聘与刷题等消费级应用，尚未对当前自进化研究主线形成直接推动。

## 对当前研究的启发
- **Awesome-RSI**：[Memento 3](#memento-3) 与 [RSI-Anything](#rsi-anything) 表明 RSI 系统应把可执行世界模型、真实环境反馈和兼容性检查共同纳入验收闭环，而非仅依赖模型自评。
- **AgentEvolve**：[ReHarness](#reharness) 的后向历史修订机制可用于把新反馈传播到旧经验，避免免训练自进化持续复用已经失效的记忆。
- **SystemEvolve**：[Google Harness²](#google-harness-agent) 与 [Evo²](#evo) 提供了任务级搜索、Harness 级递归和权重—脚手架协同优化的分层系统演化范式。
- **HarnessEvolve**：[Google Harness²](#google-harness-agent) 的跨任务、跨模型编辑经验迁移说明 Harness 改动应被结构化记录，并在隔离任务上进行回归验证。
- **RobotEvolve**：[Recursia](#recursia) 和 [RoboFoundry](#robofoundry) 可用于设计“执行—反思—修复—技能晋升”闭环，并以 [EmbodiedCLBench](#embodiedclbench) 检验其是否获得组合泛化而非任务记忆。
- **AgentTrainEvolve**：[智能体强化学习自蒸馏方法的现实检验](#item-98) 要求后续方法始终报告相对 GRPO 的跨任务、跨模型及计算归一化收益，避免把额外算力误判为算法进步。
- **EnvironmentEvolve**：[MAI-Gym](#mai-gym-gui) 与 [ProgramGym](#programgym) 说明环境生成应同时具备确定性验证、大规模并行和任务隔离，才能稳定支撑长程 Agent RL。
- **ResearchEvolve**：[DeepRSI](#deeprsi-48-kimi-k3) 与 [ASI-Bench](#asi-bench-ai) 提示科研智能体需要私有验证器、分阶段研究交付物和流程操作化指标，以抑制奖励投机。
- **SwarmEvolve**：[FlowMAS](#flowmas) 与 [MASS](#mass) 可组合为“先搜索协作拓扑、再将优质协作轨迹回灌共享模型”的群体自进化管线。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-18/  

