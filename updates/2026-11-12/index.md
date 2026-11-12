# 2026-11-12 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进从模型权重扩展到架构、脚手架与运行时系统**：今天集中出现 6 项相关进展，[机制干预](#ai-transformer)动态热插拔模型模块，[EvolveNet](#evolvenet-harness)协作演化共享 Harness，[Terminal-RSI](#terminal-rsi)让终端智能体递归重写自身，[InfraRSI](#infrarsi)则把闭环延伸到训练基础设施优化。
- **Agent 经验积累开始强调可核查记忆与跨场景复用**：[WikiTrace](#wikitrace)用原始轨迹和成败证据约束记忆修正，[WICL](#wicl)把仿真排练反馈固化为可迁移任务记忆，[AgentBaton](#agentbaton)进一步依据任务进度实现长程执行中的模型接力。
- **自主科研形成“元认知—实验闭环—可复现成果”链条**：[Sage-Taiyi](#sage-taiyi)动态管理证据、假设与研究策略，[ProTEUS](#proteus)以实验反馈闭环搜索高活性蛋白变体，[ReproBridge](#reprobridge)则显著提高科研智能体复现实验的成功率。
- **评测重点转向决策复杂度、数据泄漏与真实物理执行**：[MMDM](#mmdm)系统刻画快决策模型在长上下文和大选项空间中的局限，[FinDendro](#findendro)揭示模型无法可靠判断自身时间知识边界，[Embodied First Exam](#embodied-first-exam)将编码智能体评测扩展到 47 种机器人和 1156 项任务。
- **热点延伸集中于生成模型与低层模型技术**：低相关性条目覆盖少步视频生成、端到端语音、量化和三维重建，代表工作包括 [APEX](#apex)、[WaveGen](#wavegen)与[SplatAnything](#splatanything-3dgs)，适合作为外围技术趋势跟踪。

## 对当前研究的启发
- **SystemEvolve**：[机制干预](#ai-transformer)与[EvolveNet](#evolvenet-harness)表明可将“可热插拔模块生成”和“带验证回滚的 Harness 合并”纳入同一系统级演化闭环，而不必把自改进局限于权重更新。
- **Awesome-RSI**：[Terminal-RSI](#terminal-rsi)提供了从自我重写到策略精炼并获得新任务能力的完整案例，可用于补充 RSI 是否产生能力跃迁而非单纯基准增益的评测维度。
- **AgentEvolve**：[WikiTrace](#wikitrace)说明部署时经验演化应保留洞见、任务结果与原始轨迹之间的可追溯链接，使智能体能够主动核查并撤销有害经验。
- **MemoryEvolve**：[WICL](#wicl)与[WikiTrace](#wikitrace)分别给出跨具身任务记忆和证据关联纠错机制，可组合研究“经验固化—迁移复用—失败回溯”的长期记忆生命周期。
- **AgentTrainEvolve**：[NeoHorse-1.5-Flash Preview](#neohorse-1-5-flash-preview-agent-rsi)把执行反馈、多模型差分诊断和环境进化转为在线训练信号，可作为多轮 Agentic RL 数据飞轮的工程参考。
- **InfraEvolve**：[InfraRSI](#infrarsi)通过真实硬件验证、全局性能建模和跨硬件经验沉淀取得最高 2.75 倍加速，直接验证了基础设施优化可以构造成可复用的递归搜索闭环。
- **ResearchEvolve**：[Sage-Taiyi](#sage-taiyi)、[ProTEUS](#proteus)与[ReproBridge](#reprobridge)共同提示自主科研系统应同时显式维护假设与证据、接入真实实验反馈，并将环境和执行决策封装为可复现成果。
- **EvalEvolve**：[FinDendro](#findendro)证明模型的知识截止日期声明不足以防止泄漏，动态评测需要引入外部可验证的时间隔离与数据谱系，而不能依赖模型自我报告。
- **JevEvolve**：[MMDM](#mmdm)可用于定位快决策模型在大候选空间和复杂逻辑依赖下的能力边界，[Flide](#flide)则提供复用分支状态、降低高频结构化决策成本的执行路径。
- **RSI创业**：[无涯智远的实时 RSI 路线](#rsi)显示“发布后持续学习”正形成独立产品叙事，其超网络低成本参数更新方案值得跟踪实际遗忘控制、在线成本与商业可交付性。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-12/  

