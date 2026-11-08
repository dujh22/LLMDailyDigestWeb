# 2026-11-08 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **智能体训练转向“可执行环境—真实任务—可靠验证”一体化**：以 [WildAWM](#wildawm) 的合成个人电脑和 [Firefly](#firefly) 的真实 API 反向出题为代表，配合 [AttnSR](#attnsr) 的无额外模型步级信用分配，持续降低长程工具智能体的数据与训练成本。
- **冻结权重后的系统级自进化取得显著进展**：[VISTA](#vista) 通过自主改写机器人 Harness 将 LIBERO-Pro 成功率从 17.5% 提至 95.0%，[Evolver](#evolver) 则把探索轨迹沉淀为可检索 Gene，显示工作流、代码和经验资产正成为模型参数之外的主要进化载体。
- **长期记忆从存储扩展到离线巩固、结构化检索与安全控制**：[Anthropic公开Claude离线“做梦”长期记忆架构](#anthropic-claude) 展示轨迹回放、纠错压缩与知识重组闭环；同时患者状态图、查询相关压缩和“良性交互过度泛化”结果表明，记忆有效性与行为安全必须共同评测。
- **评测审计开始改变对“能力提升”的判断**：[学习任务还是学习验证器？具身自我改进中的标准暴露](#item-32) 和 [表面之下：智能体演化中被忽视的可靠性、成本与迁移问题](#item-41) 分别揭示验证器过拟合与脚手架分数虚高，[验证器强化学习相对 SFT 的边际价值评估](#sft) 也表明 RLVR 的主要增益可能集中在分布外泛化而非总体性能。
- **自主科研与群体搜索获得新的可执行基础设施**：[Scientist World](#scientist-world-ai) 将论文转成可运行研究环境，[SwarmEvolve](#swarmevolve) 以潜空间群体和共享 KV 缓存加速程序发现；与此同时，[METR 审计](#metr-anthropic-ai) 将 AI 辅助研发加速首次推向可量化的治理预警。
- **模型与系统侧继续探索低延迟、长上下文和状态复用**：[Drex](#drex) 以非自回归概率输出推进基础决策模型，[HST](#hst-llm) 实现混合线性注意力模型间的高效状态移交；热点延伸则集中于视觉生成、三维化身修复和具身视觉规划。

## 对当前研究的启发
- **EnvironmentEvolve**：[WildAWM](#wildawm) 与 [Firefly](#firefly) 说明环境合成应同时生成执行载体、跨接口长程任务和可离线复现验证器，而非仅扩充任务文本。
- **AgentTrainEvolve**：[AttnSR](#attnsr) 可用策略自身注意力完成步级奖励分配，适合作为长程 Agentic RL 中替代额外奖励模型的低成本基线。
- **SystemEvolve**：[VISTA](#vista) 证明固定模型下自动修改 Harness 并以自主测试择优保留即可获得数量级提升，应将系统代码、测试集和执行日志纳入统一进化循环。
- **AgentEvolve**：[Evolver](#evolver) 的结构化 Gene 资产提供了把成功与失败轨迹转成可检索、可反馈、可版本化经验单元的直接实现范式。
- **MemoryEvolve**：[Anthropic公开Claude离线“做梦”长期记忆架构](#anthropic-claude) 提示记忆系统应增加离线回放、冲突纠正和知识重组阶段，而不能只做在线写入与向量检索。
- **EvalEvolve**：[Terminal-Bench 持续验证与维护](#terminal-bench) 与 [闭环智能体评估](#item-45) 支持把基准作为持续审计的软件资产，以任务修复、证据溯源和回归反馈替代一次性排行榜。
- **GeneralizeEvolve**：[学习任务还是学习验证器？](#item-32) 表明向自改进系统暴露成功标准会制造验证器过拟合，迁移评测应采用隐藏且忠实于用户指令的独立标准。
- **EvolveLRM**：[验证器强化学习相对 SFT 的边际价值评估](#sft) 提示后训练实验应把分布内拟合与分布外增益分开报告，并重点衡量 RLVR 相对强 SFT 的边际泛化价值。
- **ResearchEvolve**：[Scientist World](#scientist-world-ai) 可作为 AI Scientist 的统一执行环境，把论文成果基线、实验轨迹和训练反馈连接成可复现闭环。
- **SwarmEvolve**：[SwarmEvolve](#swarmevolve) 的潜空间群体、共享 KV 缓存和新颖性筛选，为扩大群体搜索规模同时控制通信与推理成本提供了具体架构。
- **JevEvolve**：[Drex](#drex) 证明直接输出候选概率的开放权重决策模型可兼顾低延迟与顺序鲁棒性，适合作为快决策—慢思考路由的基础模型候选。
- **Awesome-RSI**：[METR 审计](#metr-anthropic-ai) 提供了以研发速度倍率和 AI 贡献比例衡量自我加速的外部审计框架，可补充仅依据任务分数判断 RSI 进展的方法。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-08/  

