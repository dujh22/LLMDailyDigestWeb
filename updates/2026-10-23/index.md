# 2026-10-23 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **智能体训练转向更精细的长程信用分配与经验闭环**：代表工作包括以同噪声反事实轨迹降低方差的 [TWICE：同噪声孪生世界的智能体强化学习信用分配](#twice)、内化故障恢复策略的 [RIPPLE：面向长程编程智能体的恢复内化与阶段化信用分配](#ripple)，以及协同演化知识与模型的 [SPLICE：基于一致性正则化的智能体知识—模型协同演化](#splice)。
- **环境、脚手架与程序本身成为可持续演化对象**：[WildAWM：面向计算机使用智能体的可控环境与任务合成](#wildawm) 和 [Trace2World：从真实交互轨迹重建应用世界以规模化训练 GUI 智能体](#trace2world-gui)推进可执行、可验证环境生成，[CMAS：非平稳环境下的保守元智能体架构适应](#cmas)与 [AgenticEvolve：持久化智能体驱动的进化程序搜索](#agenticevolve)则探索安全架构迭代和持久化实验搜索。
- **长期记忆研究同时出现“简化架构”与“强化治理”两条信号**：[复杂智能体记忆并非总是必要：朴素 Raw-RAG 基线更强](#raw-rag)表明原始证据覆盖可能比复杂记忆加工更关键，而 [AfterDeleteBench：审计智能体删除后的信息残留](#afterdeletebench)揭示删除后仍可从派生记忆恢复秘密，要求来源感知的级联治理。
- **低延迟决策与固定预算推理加速同步升温**：[OpenAI 发布 Decisions API，面向低延迟低成本决策](#openai-decisions-api)将封闭集评分、路由推向产品化，[OpenAttention：用尾部代理实现 1% 稀疏注意力读取](#openattention-1)则以仅读取 1% KV 缓存保持接近稠密注意力的准确率；[MiniMax 开源 M3.1 Flash：428B 参数与百万 Token 上下文](#minimax-m3-1-flash-428b-token)进一步体现模型、缓存与硬件调度的联合优化趋势。
- **可信执行与评测有效性成为智能体落地的硬约束**：[基于 Petri 网监督控制的智能体认证执行框架](#petri)以形式化控制约束工具动作，[测试评分代码智能体基准中的规格—判定器缺口](#item-49)则指出隐藏测试可能偏离任务规格，直接影响代码智能体排名与训练目标的可信度。
- **热点延伸集中于实时多模态与空间智能评测**：相关性较低但值得关注的 [StreamEval：交互式流式视频生成统一评测基准](#streameval)和 [SpatialScout：VLM 智能体主动探索与三维场景建图基准](#spatialscout-vlm)，分别暴露长期状态一致性和有限预算主动探索的能力缺口。

## 对当前研究的启发
- **AgentTrainEvolve**：[TWICE：同噪声孪生世界的智能体强化学习信用分配](#twice)可用于构造低方差回合级优势信号，[RIPPLE：面向长程编程智能体的恢复内化与阶段化信用分配](#ripple)则提供了把失败反思稳定转化为参数化恢复能力的训练路径。
- **EnvironmentEvolve**：[WildAWM：面向计算机使用智能体的可控环境与任务合成](#wildawm)与 [Trace2World：从真实交互轨迹重建应用世界以规模化训练 GUI 智能体](#trace2world-gui)表明环境生成应以可执行性、可解性和验证器可靠性为联合质量门槛。
- **AgentEvolve**：[SPLICE：基于一致性正则化的智能体知识—模型协同演化](#splice)提示可用多视角一致效用筛选经验，避免推理时知识库写入被单次偶然收益污染。
- **MemoryEvolve**：[复杂智能体记忆并非总是必要：朴素 Raw-RAG 基线更强](#raw-rag)提示先强化原始证据覆盖与重排基线，[AfterDeleteBench：审计智能体删除后的信息残留](#afterdeletebench)则要求记忆系统记录派生关系并支持级联删除。
- **SystemEvolve**：[CMAS：非平稳环境下的保守元智能体架构适应](#cmas)提供了“影子回放—风险约束—保守晋升”的架构更新协议，可用于降低自改工作流上线时的退化风险。
- **CacheEvolve**：[OpenAttention：用尾部代理实现 1% 稀疏注意力读取](#openattention-1)说明固定预算缓存管理可从单纯淘汰转向查询聚类、误差预算与被丢弃尾部信息代理的联合学习。
- **JevEvolve**：[OpenAI 发布 Decisions API，面向低延迟低成本决策](#openai-decisions-api)验证了有限答案空间的直接评分已具备产品形态，可重点研究快模型与慢推理之间的自动升级边界及在线校准。
- **HarnessEvolve**：[测试评分代码智能体基准中的规格—判定器缺口](#item-49)要求 harness 同时披露自然语言规格、隐藏判定器依赖及上游实现假设，避免把复现隐含细节误判为编程能力。
- **CodeEvolve**：[AgenticEvolve：持久化智能体驱动的进化程序搜索](#agenticevolve)表明跨代保留实验上下文和岛屿级自主试验，可在有限评估预算下提升程序搜索效率。
- **ResearchEvolve**：[ADAPT for Science：自进化科学优化多智能体系统](#adapt-for-science)提供了将科研优化拆成“搜索位置”和“搜索方式”并共同演化的闭环设计，适合迁移到昂贵实验预算下的自动科研任务。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-23/  

