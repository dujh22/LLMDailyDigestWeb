# 2026-10-23 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **智能体训练转向长程信用分配与经验内化**：从以同噪声反事实降低方差的 [TWICE](#twice)、将故障恢复蒸馏进策略的 [RIPPLE](#ripple)，到知识与模型交替演化的 [SPLICE](#splice)，训练目标正从“任务成功”细化为可归因、可复用的过程能力。
- **长期记忆研究开始反思复杂架构并强化治理**：[Raw-RAG](#raw-rag) 以朴素原始证据检索超过多数复杂记忆系统，[AfterDeleteBench](#afterdeletebench) 则证明删除秘密后仍可能从派生记忆恢复信息，凸显证据覆盖、来源追踪和级联删除的重要性。
- **可执行环境与系统自进化同步推进**：[WildAWM](#wildawm) 和 [Trace2World](#trace2world-gui) 分别从合成任务与真实轨迹重建规模化生成训练环境，[CMAS](#cmas) 与 [AgenticEvolve](#agenticevolve) 则把架构和程序搜索本身纳入持续演化闭环。
- **固定预算推理成为系统优化主线**：[OpenAttention](#openattention-1) 以 1% KV 读取保持接近稠密注意力的精度；与此同时，[MiniMax M3.1 Flash](#minimax-m3-1-flash-428b-token) 将稀疏注意力、量化感知训练和功耗调度整合进百万 Token 开放模型。
- **快决策模型加速产品化并走向持续个性化**：[OpenAI Decisions API](#openai-decisions-api) 将分类、路由和评分封装为低延迟服务，[Jev-DLC](#jev-dlc) 进一步展示了利用接受与撤销反馈持续更新个体决策状态的路径。
- **热点延伸聚焦实时多模态与空间智能评测**：[StreamEval](#streameval) 暴露流式视频模型在请求执行和长期一致性上的短板，[SpatialScout](#spatialscout-vlm) 则将 VLM 智能体评测推进到有限预算下的主动探索与三维建图。

## 对当前研究的启发
- **AgentTrainEvolve**：[TWICE](#twice) 的同噪声事实—反事实轨迹可作为低方差回合级信用分配器，[RIPPLE](#ripple) 的阶段化训练则提供了把失败反思转化为可执行恢复策略的具体方案。
- **AgentEvolve**：[SPLICE](#splice) 表明推理时知识库演化可以用跨视角效用一致性过滤噪声经验，并与后续自蒸馏、强化学习形成闭环。
- **MemoryEvolve**：[Raw-RAG](#raw-rag) 与 [AfterDeleteBench](#afterdeletebench) 共同提示记忆系统应优先保留可追溯原始证据，并让删除操作沿派生关系级联传播，而非只优化摘要和检索结构。
- **EnvironmentEvolve**：[WildAWM](#wildawm) 的执行质量门控和 [Trace2World](#trace2world-gui) 的“行为重建—代码实现”解耦，可直接用于构建兼具可执行性、可验证性与规模化能力的环境生产线。
- **CacheEvolve**：[OpenAttention](#openattention-1) 的尾部代理与误差感知读取说明，固定预算 KV 管理可从单纯淘汰升级为对未读取信息进行统计补偿的自适应策略。
- **JevEvolve**：[OpenAI Decisions API](#openai-decisions-api) 验证了有限候选直接评分的产品需求，[Jev-DLC](#jev-dlc) 则提供了把用户接受和撤销压缩为持久因果状态的在线个性化机制。
- **HarnessEvolve**：[测试评分代码智能体基准中的规格—判定器缺口](#item-49) 表明 harness 必须显式审计自然语言规格与隐藏测试的一致性，否则排名会混入复现上游实现细节的能力。
- **CodeEvolve**：[AgenticEvolve](#agenticevolve) 证明持久化智能体可在进化岛屿中自主设计并运行实验，为减少程序搜索评估次数和沉淀跨代实验经验提供了可复用架构。
- **ResearchEvolve**：[ADAPT for Science](#adapt-for-science) 可将科学优化拆成“搜索位置”与“搜索方式”的协同演化，而 RIDAR 的轨迹检测与运行时纠正可作为该闭环的研究诚信防线。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-23/  

