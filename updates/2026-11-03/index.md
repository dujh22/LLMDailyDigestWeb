# 2026-11-03 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从机制探索走向风险治理：[Astra 直接编程神经网络权重，显著提升 Qwen 数学能力](#astra-qwen)尝试绕过梯度下降直接修改模型，[R²Orch](#r-orch)以自博弈和技能内化迭代智能体编排，而[Anthropic招股书警示模型逼近RSI阈值](#anthropic-rsi)则将能力加速与安全监督问题推至产业层面。
- 部署期智能体演化集中在记忆、工作流与可靠执行：[Meta提出路由式持续学习架构Routed CL](#meta-routed-cl)隔离并复用任务经验，[SeaFlow](#seaflow)依据反馈修订代码优先工作流，[RECEIPT](#receipt)修复工具交互中的假成功，[MemUse](#memuse)则把记忆评测推进到“是否真正影响行动”。
- 训练环境与长程任务开始强调可执行、可验证和真实深度：[终端长程任务的真实深度测量与合成](#item-30)以必要顺序交互刻画难度，[LegoEnv](#legoenv)通过环境原子模块化重组扩大训练环境供给。
- 评测可靠性暴露关键缺口：[不可能代码，评分几乎不变：代码评判模型复现实验](#item-39)发现强评判器会高估语法无效代码，提示自进化系统不能直接把模型评分当作可信奖励。
- 新模型与推理系统同步推进：[商汤开源循环架构模型 SenseNova Loop-9B-Preview](#sensenova-loop-9b-preview)以参数共享换取有效计算深度，[美团发布原生多模态模型 LongCat-2.5](#longcat-2-5)强化长程智能体能力，[CacheWeave](#cacheweave-kv)则学习选择重计算以降低 KV 缓存成本；低相关热点延伸主要集中在旗舰模型传闻和视觉生成。
- 科研与具身基础设施加速落地：[腾讯混元发布 Hyra 2.0：通用 Agent 研发可复用科学工具](#hyra-2-0-agent)展示持续沉淀科研工作流的生产系统，[优必选发布Thinker-Sim具身智能仿真平台](#thinker-sim)则打通场景重建、合成数据、评测与 Real2Sim2Real 闭环。

## 对当前研究的启发
- **Awesome-RSI**：[Astra](#astra-qwen)与[R²Orch](#r-orch)分别把自改进对象推进到模型权重和智能体编排器，但代码评判失真结果表明每轮改进都必须配置外部可执行验证而非依赖自评。
- **AgentEvolve**：[SeaFlow](#seaflow)的可审计代码工作流与[Meta Routed CL](#meta-routed-cl)的经验隔离路由，可组合成“按任务选经验—执行—依据反馈修订工作流”的冻结参数演化闭环。
- **AgentTrainEvolve**：[终端长程任务的真实深度测量与合成](#item-30)提供了比回合数更可靠的课程难度信号，可用于控制长程 Agentic RL 的任务生成与递进训练。
- **EnvironmentEvolve**：[LegoEnv](#legoenv)证明将意图、规则、数据和服务器拆成可验证原子，有助于把环境进化从整题生成转为可复用组件的组合搜索。
- **MemoryEvolve**：[MemUse](#memuse)提示记忆系统应评估记忆交付后是否改变决策及结果，而非只报告检索命中率或最终成功率。
- **Groom**：[RECEIPT](#receipt)的系统调用观测与[MemUse](#memuse)的使用点追踪可直接扩展过程级 token 归因，区分有效工具反馈、无效等待与未被利用的记忆开销。
- **EvalEvolve**：[不可能代码，评分几乎不变](#item-39)说明代码评测必须将编译、执行和测试证据设为硬门控，避免 LLM 评判器对表面合理输出给出虚高奖励。
- **CacheEvolve**：[CacheWeave](#cacheweave-kv)将块选择器与重计算预算联合学习，为固定显存预算下动态决定“保留还是重算”提供了直接方案。
- **ResearchEvolve**：[Hyra 2.0](#hyra-2-0-agent)的状态持久化、证据复核和技能沉淀表明，科研智能体应把可复用模型与工作流作为跨任务持续演化的核心产物。
- **RobotEvolve**：[Thinker-Sim](#thinker-sim)可作为环境生成、轨迹采集、能力评测和 sim-to-real 回灌的一体化底座，支持机器人训练闭环的规模化实验。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-03/  

