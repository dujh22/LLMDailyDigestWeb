# 2026-10-20 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 具身智能自进化成为今日主线：商汤 [SenseNova-RoboRSI](#sensenova-roborsi) 以执行反馈和递归改进强化冻结模型，[EVO-WAM](#evo-wam) 则通过“想象—验证—学习”闭环生成可训练轨迹，显示推理时经验积累与训练侧数据飞轮正在汇合。
- 机器人能力边界与 Harness 设计得到更清晰的实证：[HexaShell](#hexashell-vlm) 以轻量编程框架刷新 RoboDojo 表现，而 [GPT-6-Astra 具身评测](#gpt-6-astra) 表明精细接触、状态验证、长程执行和失败恢复仍是落地瓶颈。
- 记忆与持续个性化从外挂存储走向模型、运行时和训练基础设施协同：[MemT 1.0](#memt-1-0-300b-rsi) 引入可训练原生记忆分支，[CarryOn](#carryon) 用任务对象压缩长程上下文，[Personal AI](#personal-ai) 则尝试将个人经验持续沉淀为专属参数能力。
- 智能体评测进一步转向过程、证据与真实动态环境：[BizAgentBench](#bizagentbench) 揭示结果正确会掩盖违规执行和工具成本，[Into the Unknown](#into-the-unknown) 暴露科研智能体缺乏证据支撑的问题，强调仅看最终产出已不足以判断能力。
- 系统工程侧强调低成本路由、职责隔离与可扩展训练环境：[HiRoute](#hiroute-jev) 用 Jev 动态切换快慢模型，[Meta 薄编排器模式](#meta) 以确定性路由隔离故障，[OpenMobile-2](#openmobile-2) 则用可控环境和原生工具扩展移动智能体训练；热点延伸方面，交互式视频生成开始以推测采样降低延迟。

## 对当前研究的启发
- **RobotEvolve**：[SenseNova-RoboRSI](#sensenova-roborsi) 与 [EVO-WAM](#evo-wam) 分别提供“冻结模型下的执行反馈改进”和“世界模型自想象轨迹回灌”两条可组合的机器人持续进化路径。
- **AgentEvolve**：[SenseNova-RoboRSI](#sensenova-roborsi) 验证了统一 Harness 可将交互经验转化为推理时改进，而 [CarryOn](#carryon) 的对象化任务状态可作为技能与工作流记忆的低成本载体。
- **MemoryEvolve**：[MemT 1.0](#memt-1-0-300b-rsi) 与 [CarryOn](#carryon) 可用于对比参数化原生记忆和对象化外部记忆在写入、复用、遗忘及推理成本上的取舍。
- **Groom**：[BizAgentBench](#bizagentbench) 的确定性过程检查与 LiveMACE 的完整决策轨迹表明，应把违规步骤、冗余工具调用和偶然成功纳入 token 利用归因。
- **JevEvolve**：[HiRoute](#hiroute-jev) 直接给出了以任务复杂度和上一阶段胜任度为信号学习快慢模型升级边界的长程工作流范式。
- **ResearchEvolve**：[Into the Unknown](#into-the-unknown) 中九种前沿智能体均未完成开放式续研任务，说明科研闭环必须引入逐项要求验证和声明—证据绑定，而不能只评判论文成稿。
- **AgentTrainEvolve**：[Scene-Designer](#scene-designer-3d) 的 Critic 引导 GRPO 与 [OpenMobile-2](#openmobile-2) 的可控应用环境表明，可执行环境、确定性验证器和自动经验生成应作为长程 Agent RL 的一体化基础设施。
- **SystemEvolve**：[Meta 薄编排器模式](#meta) 提示系统级演化应保留一个只负责确定性路由与可靠性检查的稳定内核，再让上下文隔离的专项智能体独立迭代。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-20/  

