# 2026-11-14 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **RSI 从框架走向完整工程闭环与产业落地**：3 项代表进展分别覆盖可热插拔自扩展的 [openJiuwen RSI 原生 AgentOS](#openjiuwen-rsi-agentos-agent)、自主优化数据与训练基础设施并产出 MoE 模型的 [No Second Run](#no-second-run-rsi-801-30b-a3b)，以及进入材料、核聚变和芯片设计等场景的 [伐谋 3.0](#3-0-rsi)。
- **智能体评测与训练信号进一步转向过程可靠性**：[SO-Arena](#so-arena-system-one)从交互执行、决策稳定性和拒答识别等维度刻画快决策模型，而[行动者、评判者还是教师？](#item-11)表明弱行动模型仍可借助完整轨迹的事后判断提供有效强化学习信号。
- **效率优化覆盖上下文、网络结构与注意力机制**：[CoACT](#coact-coding-agent)以“保持下一步动作”为目标压缩 Coding Agent 上下文并降低 33% Token 消耗，[SimpleHC](#simplehc)以较低训练开销简化超连接，[UniSpark](#unispark)则探索全注意力与线性注意力混合的统一多模态架构。
- **物理与具身方向开始形成“环境—数据—模型改进”链条**：[Ropedia Xperience 2](#ropedia-xperience-2)规模化构建可交互三维环境和机器人轨迹，[PhysLoop](#physloop-llm)则让 LLM 以物理知识参与视频生成、筛选和纠错，形成数据驱动的递归改进闭环。
- **应用能力继续产品化，热点延伸集中于世界模型与视觉生成**：[DeepSeek 开放应用 API](#deepseek-api-chat-demo)降低完整对话应用的集成门槛；低相关性热点则包括驾驶世界模型、4D 世界评测、图像 Token 深度压缩和视图合成加速。

## 对当前研究的启发
- **Awesome-RSI**：[No Second Run](#no-second-run-rsi-801-30b-a3b)与 [openJiuwen AgentOS](#openjiuwen-rsi-agentos-agent)分别提供训练流程和运行时系统两种 RSI 实例，可用于补充“改进对象、验证机制与回退能力”的工程化分类。
- **SystemEvolve**：[openJiuwen AgentOS](#openjiuwen-rsi-agentos-agent)将扩展做成可热插拔、版本化和可回退单元，为系统自改写后的安全验证与保留机制提供了直接设计参考。
- **EvolveLLM**：[No Second Run](#no-second-run-rsi-801-30b-a3b)把数据、基础设施和训练配置纳入统一多智能体闭环，展示了基础模型自进化可从单一数据迭代扩展为全栈联合优化。
- **InfraEvolve**：[No Second Run](#no-second-run-rsi-801-30b-a3b)证明训练基础设施可以成为 Agent 持续实验和优化的对象，其自动验证与配置沉淀机制可迁移到推理引擎进化。
- **RSI创业**：[伐谋 3.0](#3-0-rsi)将“设计—执行—验证—反馈”闭环部署到多个高价值产业场景，为判断 RSI 商业化应优先落在可验证研发流程提供了案例。
- **Groom**：[CoACT](#coact-coding-agent)以“压缩后能否保持下一步动作”为评价准则，可直接转化为过程级 Token 价值归因和上下文冗余测量指标。
- **JevEvolve**：[SO-Arena](#so-arena-system-one)提供快决策模型的能力谱系、稳定性与缺失答案识别评测，而[事后教师研究](#item-11)提示应将行动能力和轨迹评判能力分开校准。
- **AgentTrainEvolve**：[行动者、评判者还是教师？](#item-11)表明完整轨迹上的事后评判可从弱行动模型中提取高质量强化学习信号，为长时程信用分配提供了具体路径。
- **PhysicalEvolve**：[PhysLoop](#physloop-llm)展示了把物理知识转化为视频筛选与修复信号的闭环，可借鉴为“模型预测—物理检查—数据回灌”的自进化模板。
- **EnvironmentEvolve**：[Ropedia Xperience 2](#ropedia-xperience-2)同时规模化环境资产与人类行为轨迹，为研究环境复杂度、行为数据量和具身能力之间的协同缩放提供了数据基础。
- **CacheEvolve**：[UniSpark](#unispark)的全注意力与 GatedDeltaNet 混合结构为固定预算下兼顾全局交互和线性状态记忆提供了可跟踪的架构样本。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-14/  

