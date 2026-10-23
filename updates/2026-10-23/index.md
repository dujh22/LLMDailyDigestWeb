# 2026-10-23 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **智能体学习从单次反思走向长程信用分配与结构演化**： [TWICE](#twice) 用同噪声反事实轨迹降低回合级信用分配方差，[苏格拉底式技能学习](#item-8) 通过教学—实践循环沉淀可迁移技能，[CMAS](#cmas) 则把非平稳环境下的智能体架构安全迭代纳入闭环。
- **长期记忆研究集中暴露“复杂不一定更好”与治理风险**：[复杂智能体记忆并非总是必要：朴素 Raw-RAG 基线更强](#raw-rag) 显示原始证据检索可胜过复杂记忆系统，[AfterDeleteBench](#afterdeletebench) 发现删除后的派生记忆仍可能泄密，推动记忆评测从检索准确率扩展到证据覆盖、状态治理和级联删除。
- **固定预算推理成为系统优化主线**：[OpenAttention](#openattention-1) 在仅读取 1% KV 缓存时保持接近稠密注意力的精度，[BeNice!](#benice-kv) 让循环模型跨递归共享 KV；同时 [MiniMax M3.1 Flash](#minimax-m3-1-flash-428b-token) 将稀疏注意力、量化感知训练和功耗调度整合进百万 Token 开放模型。
- **可执行环境、程序搜索与自主科研形成更完整的自进化闭环**：[WildAWM](#wildawm) 自动合成可验证的 GUI、MCP 与命令行长程任务，[AgenticEvolve](#agenticevolve) 让持久化智能体自主运行进化实验，[ADAPT for Science](#adapt-for-science) 则把历史设计与执行反馈用于科学系统优化。
- **快决策模型与生产级智能体同步落地**：[OpenAI Decisions API](#openai-decisions-api) 将低延迟候选评分与路由产品化，[RIPPLE](#ripple) 把故障恢复内化为长程编程策略；与此同时，[基于 Petri 网监督控制的智能体认证执行框架](#petri) 和[规格—判定器缺口研究](#item-49) 分别推进执行安全与代码评测有效性。
- **热点延伸聚焦连续多模态与空间智能评测**：[StreamEval](#streameval) 揭示流式视频系统的长期状态一致性短板，[SpatialScout](#spatialscout-vlm) 则考察 VLM 智能体在有限交互预算下的主动探索和三维建图能力。

## 对当前研究的启发
- **AgentTrainEvolve**：[TWICE](#twice) 的同噪声事实—反事实配对可作为长程 Agentic RL 的低方差信用分配器，而 [RIPPLE](#ripple) 表明阶段化训练能将失败反思真正内化为可执行恢复策略。
- **AgentEvolve**：[苏格拉底式技能学习](#item-8) 提供了“专家教学—自主实践—技能修订—跨任务复用”的免持续人工指导技能库演化范式。
- **MemoryEvolve**：[复杂智能体记忆并非总是必要：朴素 Raw-RAG 基线更强](#raw-rag) 建议先以原始证据覆盖率建立强基线，[AfterDeleteBench](#afterdeletebench) 则要求记忆写入时同步记录来源依赖以支持级联删除。
- **CacheEvolve**：[OpenAttention](#openattention-1) 的尾部代理和 [BeNice!](#benice-kv) 的跨递归 KV 共享，分别提供了注意力读取预算自适应与循环架构固定内存化的可实现路径。
- **EnvironmentEvolve**：[WildAWM](#wildawm) 展示了以执行质量门控统一保证合成环境可运行、任务可解和验证可靠性的环境生产流水线。
- **CodeEvolve**：[AgenticEvolve](#agenticevolve) 可借鉴为持久化编码智能体驱动的多岛程序搜索框架，而 [RIPPLE](#ripple) 可增强其长程实验中的故障诊断与恢复。
- **JevEvolve**：[OpenAI Decisions API](#openai-decisions-api) 验证了低延迟封闭集评分的产品形态，可进一步研究从交互日志中持续校准快模型并学习升级到慢思考的路由边界。
- **ResearchEvolve**：[ADAPT for Science](#adapt-for-science) 将“搜索位置”与“搜索方式”共同演化，为有限实验预算下的自主科研闭环提供了可复用的双层优化设计。
- **HarnessEvolve**：[基于 Petri 网监督控制的智能体认证执行框架](#petri) 可用于给工具 harness 增加最小干预的形式化安全层，而[规格—判定器缺口研究](#item-49) 提醒评测必须审计任务描述与隐藏测试是否衡量同一构念。
- **SystemEvolve**：[CMAS](#cmas) 的归档检索、类型化图编辑、影子回放与保守晋升机制，为架构自改进设置了可回滚且受风险约束的上线流程。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-23/  

