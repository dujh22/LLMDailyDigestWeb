# 2026-11-03 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进同时向模型权重、智能体系统与治理层推进：[Astra 直接编程神经网络权重，显著提升 Qwen 数学能力](#astra-qwen)展示无梯度的权重空间编程，[R²Orch：通过技能内化与自博弈实现智能体编排的递归自我改进](#r-orch)形成任务选择—失败内化闭环，而[Anthropic招股书警示模型逼近RSI阈值](#anthropic-rsi)将能力加速与安全保障失配正式提升为产业风险。
- 长程智能体的训练与持续学习转向“深任务、可演化环境、经验路由”主线：[终端长程任务的真实深度测量与合成](#item-30)以必要顺序交互深度重构任务度量，[LegoEnv：通过模块化重组实现智能体环境自演化](#legoenv)提供可复用环境原子，[Meta提出路由式持续学习架构Routed CL](#meta-routed-cl)则验证了隔离并复用经验可同时提升奖励、降低成本。
- 智能体评测进一步从最终成功率深入执行过程与真实可用性：[MemUse：在使用点评估智能体记忆](#memuse)检查记忆是否真正影响行动，[不可能代码，评分几乎不变：代码评判模型复现实验](#item-39)暴露代码评判器对无效输出的系统性失真，[RECEIPT：测量并修复智能体工具调用的返回假设](#receipt)则直接修补工具交互中的假成功与超时。
- 科研与具身智能体加速走向闭环运行系统：[腾讯混元发布 Hyra 2.0：通用 Agent 研发可复用科学工具](#hyra-2-0-agent)强调状态持久化、证据复核和技能沉淀，[REA：异步脑-小脑控制的路由式具身智能体运行时](#rea)探索快慢控制异步协同，[优必选发布Thinker-Sim具身智能仿真平台](#thinker-sim)打通 Real2Sim2Real 数据、评测与任务编排。
- 模型与推理系统侧出现循环计算、原生多模态和学习式缓存三条进展：[商汤开源循环架构模型 SenseNova Loop-9B-Preview](#sensenova-loop-9b-preview)以参数共享扩展有效深度，[美团发布原生多模态模型 LongCat-2.5](#longcat-2-5)强化长程 Agentic 能力，[CacheWeave：学习重计算的高效位置无关 KV 缓存](#cacheweave-kv)则以原生块选择器权衡重计算、精度与吞吐。
- 热点延伸主要集中于尚未获官方确认的闭源旗舰模型爆料、视频先验驱动的图像生成，以及高效三维跟踪；热度较高，但对当前核心研究方向的直接证据有限。

## 对当前研究的启发
- **Awesome-RSI**：[Astra 权重空间编程](#astra-qwen)把自我改进对象从提示与代码推进到模型参数本身，而[R²Orch](#r-orch)与代码评判失真结果共同提示，RSI 闭环必须配置独立、可执行且抗作弊的验证信号。
- **AgentTrainEvolve**：[终端长程任务的真实深度测量与合成](#item-30)和[LegoEnv](#legoenv)可组合成按真实交互深度生成课程、再通过模块化环境持续扩展训练分布的 Agentic RL 数据管线。
- **AgentEvolve**：[Routed CL](#meta-routed-cl)表明按任务路由和隔离经验能够在冻结或少改模型的部署阶段提升复用效率，可与即时技能检索结合为分层经验库。
- **MemoryEvolve**：[MemUse](#memuse)提供了比检索命中率更直接的记忆效用指标，可据“记忆是否改变后续行动及结果”反向优化写入、检索和淘汰策略。
- **EnvironmentEvolve**：[LegoEnv](#legoenv)的意图、规则、数据与服务器原子化设计，为环境组件独立验证、失败组件定向修复及跨域重组提供了可落地表示。
- **EvalEvolve**：[不可能代码，评分几乎不变](#item-39)证明强 LLM 评判器也可能忽略最基本的可执行性约束，代码与 Agent 评测应强制加入确定性执行检查并审计评判器敏感度。
- **Groom**：[RECEIPT](#receipt)与[MemUse](#memuse)分别给出了工具返回协议和记忆使用点的过程证据，可用于细化 token 消耗究竟转化成了有效工具执行还是有效记忆利用。
- **ResearchEvolve**：[Hyra 2.0](#hyra-2-0-agent)将证据复核、任务状态持久化和工具沉淀集成到真实研发流程，为长期科研智能体建立“产出—核验—技能化”的持续演化闭环提供了系统模板。
- **RobotEvolve**：[Thinker-Sim](#thinker-sim)可作为规模化环境与轨迹生产层，[REA](#rea)则提供真机侧快策略执行、慢模型升级和异常恢复的运行时分工，两者可衔接为 sim-to-real 闭环。
- **CacheEvolve**：[CacheWeave](#cacheweave-kv)将缓存块选择变成可训练决策，说明固定预算缓存研究可从启发式淘汰进一步转向联合学习“保留、丢弃与重计算”。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-03/  

