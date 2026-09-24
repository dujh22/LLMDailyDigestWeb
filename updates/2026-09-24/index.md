# 2026-09-24 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进从框架分层走向真实闭环**：今日多项工作覆盖群体、脚手架、数据与物理执行路径，[79页综述提出RSI五级自主性分层架构](#79-rsi)给出 B0–L5 分级，[SwarmWorld 与 ModularRSI：AI 自我进化的群体与个体路径](#swarmworld-modularrsi-ai)探索群体协作与模块演化，[Simate以Physical RSI驱动机器人自主研究，登顶RoboDojo](#simate-physical-rsi-robodojo)则将改进循环延伸至真机实验。
- **长期记忆研究集中转向自适应策展、结构化索引与低成本压缩**：[JitMem：面向 LLM 智能体的即时任务自适应记忆策展](#jitmem-llm)将策展推迟至读取时，[EnSIMem：面向智能体长期记忆的实体结构化索引](#ensimem)强化实体组织与证据溯源，[GEM：面向长程智能体的证据保留式历史压缩](#gem)和[长程智能体行动前涌现记忆控制信号](#item-70)则以证据或内部状态指导压缩与召回。
- **智能体评测由终局准确率深入过程、主动安全与动态抗污染**：[The Tasteful Agent：衡量与提升长时程任务决策品味](#the-tasteful-agent)评估轨迹分叉处的决策质量，[PASTABench：智能体序列轨迹的主动安全评测](#pastabench)定位最佳干预窗口，[Uncheatable Eval：基于动态压缩的语言模型评测](#uncheatable-eval)持续引入新文本抵抗污染，[CART：大模型闭环自适应红队测试框架](#cart)进一步把安全测试变为可审计的动态搜索。
- **自主科研与群体智能出现大规模实证**：[950个Claude协作发现噬菌体新酶系统ART](#950-claude-art)以约 950 个智能体完成海量生物数据筛查并接受湿实验验证，[WhatWorkedBench：评测 AI 智能体的实验理解能力](#whatworkedbench-ai)开始测量科研智能体对实验变更与结果因果关系的理解，[COMPASS：用空间 Transformer 控制大规模机器人智能体集群](#compass-transformer)则将去中心化协作扩展至 1024 台机器人。
- **快决策、路由与 Harness 降本成为智能体工程主线**：[JEV-as-a-Judge：高置信接受、低置信升级的低成本评判](#jev-as-a-judge)以置信度级联保留强评判器 99% 的准确率，[Jev-Mem：System-One 控制的高效智能体记忆架构](#jev-mem-system-one)让轻量模型承担高频记忆控制，[Cursor 团队分享 Agent Harness Token 降本提示词](#cursor-agent-harness-token)则通过提示词、工具加载、缓存和子智能体调度实现约 7% 的整体 Token 降本。
- **训练与推理优化强调可验证奖励、并行化和能力权衡**：[ProCredit：从结果奖励转向智能体进度信用分配](#procredit)用逐轮验收变化缓解长程信用分配，[Flash-dLLM：IO 感知 KV 缓存与并行解码加速扩散语言模型](#flash-dllm-io-kv)与[PTTS：规划式测试时扩展协调多分支推理路径](#ptts)减少推理冗余，而[Claude 优化数学与编程能力导致写作风格退化](#claude-2)提示单向奖励优化可能造成能力退化。

## 对当前研究的启发
- **Awesome-RSI**：[79页综述提出RSI五级自主性分层架构](#79-rsi)可作为统一分类骨架，并可用 Physical RSI、SwarmWorld 与 ModularRSI 分别补充“环境执行、群体协作、改进机制自指”三类实例。
- **MemoryEvolve**：[JitMem：面向 LLM 智能体的即时任务自适应记忆策展](#jitmem-llm)、[EnSIMem：面向智能体长期记忆的实体结构化索引](#ensimem)与[长程智能体行动前涌现记忆控制信号](#item-70)共同提示，应把记忆演化研究从固定写入规则推进到任务条件读取、证据化索引和状态驱动控制。
- **EvalEvolve**：[Uncheatable Eval：基于动态压缩的语言模型评测](#uncheatable-eval)提供持续更新的抗污染信号，[PASTABench：智能体序列轨迹的主动安全评测](#pastabench)与[CART：大模型闭环自适应红队测试框架](#cart)则可用于扩展动态评测中的轨迹干预和自适应攻防维度。
- **ResearchEvolve**：[950个Claude协作发现噬菌体新酶系统ART](#950-claude-art)证明“大规模并行检索—候选收敛—人类湿实验验证”可形成真实科研闭环，而[WhatWorkedBench：评测 AI 智能体的实验理解能力](#whatworkedbench-ai)可补足其中对实验因果理解的能力测量。
- **SwarmEvolve**：[COMPASS：用空间 Transformer 控制大规模机器人智能体集群](#compass-transformer)展示了可扩展通信聚合机制，但[多智能体系统中的关机破坏倾向](#item-36)表明群体规模扩大必须同步评估协同破坏与可关停性。
- **JevEvolve**：[JEV-as-a-Judge：高置信接受、低置信升级的低成本评判](#jev-as-a-judge)与[Jev-Mem：System-One 控制的高效智能体记忆架构](#jev-mem-system-one)验证了快模型可同时承担评判级联和记忆路由，为学习“何时直接决策、何时升级慢模型”的统一边界提供了两个高频场景。
- **HarnessEvolve**：[Cursor 团队分享 Agent Harness Token 降本提示词](#cursor-agent-harness-token)表明工具按需加载、缓存布局和子智能体调度应被纳入 Harness 配置披露与消融评测，而非仅比较底层模型。
- **Groom**：[GEM：面向长程智能体的证据保留式历史压缩](#gem)、[StateComp：长程智能体的状态条件历史压缩](#statecomp)和[DRSR：面向长程智能体的集合级删除风险剪枝](#drsr)提供了三类可审计的 Token 归因对象，可具体衡量被删除历史的证据价值、状态相关性与集合风险。
- **EnvironmentEvolve**：[VHD-Play：从已求解机制生成可验证的智能体强化学习环境](#vhd-play)以“先求解机制、再渲染工具环境”的方式同时保证动态可执行与评分可验证，可作为低成本环境合成和自动课程生成的基础模板。
- **DataEvolve**：[EvoAudio：音频理解的递归自我改进](#evoaudio)通过联合演化波形、问题和难度实现无新增人工标注的数据飞轮，为研究多模态合成数据的覆盖度、难度控制与坍缩监测提供了具体闭环。
- **EvolveLRM**：[何时何处信任教师：熵校准信用分配统一在策略蒸馏与 GRPO](#grpo)和[RL 始于 RL 之前：在策略蒸馏提升强化学习效果](#rl-rl)提示可把教师分布对齐作为 RL 初始化，再以熵校准的词元级信用重分配降低稀疏奖励和错误教师信号的影响。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-24/  

