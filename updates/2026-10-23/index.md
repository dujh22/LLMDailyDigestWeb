# 2026-10-23 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **环境与训练闭环加速成形**：从可执行环境合成到经验回灌，[WildAWM：面向计算机使用智能体的可控环境与任务合成](#wildawm)负责规模化生成长程任务，[苏格拉底式技能学习：教学与实践交替培养可迁移智能体技能](#item-8)与[SPLICE：基于一致性正则化的智能体知识—模型协同演化](#splice)则探索技能沉淀和知识—参数协同演化。
- **长程智能体训练聚焦精确信用分配**：[TWICE：同噪声孪生世界的智能体强化学习信用分配](#twice)以共享采样噪声隔离决策影响，为反事实评估和低方差回合级强化学习提供了新路径。
- **记忆研究转向“简单基线与治理优先”**：[复杂智能体记忆并非总是必要：朴素 Raw-RAG 基线更强](#raw-rag)显示原始证据检索可胜过复杂记忆架构，而[AfterDeleteBench：审计智能体删除后的信息残留](#afterdeletebench)进一步揭示派生记忆残留及级联删除的必要性。
- **推理系统围绕固定预算下的缓存取舍持续突破**：[OpenAttention：用尾部代理实现 1% 稀疏注意力读取](#openattention-1)实现极低 KV 读取比例下的高保真加速，[BeNice! 通过 KV 共享弥合循环架构的推理内存差距](#benice-kv)则改善循环模型的长上下文内存效率；同时[MiniMax 开源 M3.1 Flash：428B 参数与百万 Token 上下文](#minimax-m3-1-flash-428b-token)将稀疏注意力、量化训练与硬件调度整合进大规模开放模型。
- **系统自进化与可信执行同步推进**：[CMAS：非平稳环境下的保守元智能体架构适应](#cmas)和[AgenticEvolve：持久化智能体驱动的进化程序搜索](#agenticevolve)分别探索安全架构迭代与持久化实验搜索，[基于 Petri 网监督控制的智能体认证执行框架](#petri)及[测试评分代码智能体基准中的规格—判定器缺口](#item-49)则补上执行约束与评测有效性问题。
- **快决策模型开始形成产品与持续学习链路**：[OpenAI 发布 Decisions API，面向低延迟低成本决策](#openai-decisions-api)推动有限答案空间的实时决策服务化，[Jev-DLC：基于类型化反馈的决策级持续学习](#jev-dlc)进一步展示冻结评分器下的跨请求个性化；热点延伸则集中在流式视频、三维主动探索和多光谱归因评测。

## 对当前研究的启发
- **AgentTrainEvolve**：[TWICE](#twice)的同噪声反事实轨迹可用于降低多轮工具调用强化学习的信用分配方差，而[SPLICE](#splice)提供了把高一致性经验同时写入外部知识与模型参数的训练闭环。
- **AgentEvolve**：[苏格拉底式技能学习](#item-8)可借鉴为“专家建议—自主实践—技能修订—跨任务复用”的冻结参数技能演化流程。
- **EnvironmentEvolve**：[WildAWM](#wildawm)把环境生成、任务生成和执行质量门控统一起来，可直接补强自动合成环境的可解性、难度标定与验证可靠性。
- **MemoryEvolve**：[Raw-RAG](#raw-rag)提示应先以原始证据覆盖率和重排质量作为强基线，[AfterDeleteBench](#afterdeletebench)则要求记忆写入时同步维护来源依赖图以支持级联遗忘。
- **CacheEvolve**：[OpenAttention](#openattention-1)的误差感知读取预算与[BeNice!](#benice-kv)的跨递归 KV 共享，为固定显存预算下联合学习“读哪些缓存、哪些状态复用”提供了两条互补路线。
- **SystemEvolve**：[CMAS](#cmas)的影子回放与保守晋升机制可用于约束 Agent 架构自动修改，避免非平稳任务中一次高分实验直接替换稳定系统。
- **CodeEvolve**：[AgenticEvolve](#agenticevolve)表明持久化实验智能体能以更少评估完成程序搜索，可用于增强代码进化中的跨代假设积累和实验复用。
- **HarnessEvolve**：[Petri 网监督控制框架](#petri)可将工具调用约束编译为可认证执行规则，而[规格—判定器缺口研究](#item-49)提示 harness 必须显式审计任务描述与隐藏测试的一致性。
- **JevEvolve**：[OpenAI Decisions API](#openai-decisions-api)验证了封闭集低延迟决策的产品需求，[Jev-DLC](#jev-dlc)则给出了利用接受与撤销反馈持续更新个性化状态、无需重训评分器的具体机制。
- **ResearchEvolve**：[ADAPT for Science：自进化科学优化多智能体系统](#adapt-for-science)将搜索位置与搜索方式共同纳入闭环优化，可用于设计能依据历史实验和执行反馈自适应调整科研策略的多智能体系统。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-23/  

