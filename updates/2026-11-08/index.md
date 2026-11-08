# 2026-11-08 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 推理时系统自进化取得显著进展：[VISTA：机器人通过自编程实现不动权重的具身自进化](#vista)通过持续修改执行 Harness 将任务成功率从 17.5% 提至 95.0%，[Evolver：将智能体探索转化为持续演化能力](#evolver)则把轨迹沉淀为可检索的 Gene 资产，均表明冻结权重下的经验与脚手架演化潜力。
- 智能体训练进一步转向“合成环境—真实任务—可靠验证”闭环：[Firefly：先探索后出题的可验证工具调用数据合成](#firefly)、[WildAWM：用合成“个人电脑”训练计算机使用智能体](#wildawm)和[Agent-R²：基于真实来源数据合成扩展生产力智能体](#agent-r)分别覆盖工具 API、计算机环境与职业工作流数据。
- 长期记忆同时推进架构、压缩与安全研究：[Anthropic公开Claude离线“做梦”长期记忆架构](#anthropic-claude)展示离线巩固路线，[QRAE：面向深度搜索智能体的查询相关注意力熵上下文压缩](#qrae)降低在线检索成本，而[记忆陷阱：语言智能体从良性交互中过度泛化](#item-44)揭示持久记忆可能跨任务放大不可靠行为。
- 自进化评测开始集中审视“高分是否等于真实进步”：[学习任务还是学习验证器？具身自我改进中的标准暴露](#item-32)发现验证标准暴露会诱发过拟合，[表面之下：智能体演化中被忽视的可靠性、成本与迁移问题](#item-41)提出 EvoAudit，[验证器强化学习相对 SFT 的边际价值评估](#sft)则显示 RLVR 相对 SFT 的额外收益主要是有限的分布外增益。
- 新模型与高效决策架构继续探索低延迟路线：[Drex：迈向基础决策模型](#drex)以非自回归候选分布替代文本解码，[Muir：敏感度分配门控与匹配滤波读出的线性注意力](#muir)兼顾线性注意力吞吐与超长上下文检索。
- 科研与递归改进出现新的能力及治理信号：[SwarmEvolve：潜空间智能体群的进化发现与优化](#swarmevolve)以潜空间群体搜索加速程序发现，[METR 审计：Anthropic 或已触发 AI 研发加速预警阈值](#metr-anthropic-ai)则提示 AI 辅助研发加速已需要更严格的独立测量与预警机制。

## 对当前研究的启发
- **AgentEvolve**：[VISTA](#vista)与[Evolver](#evolver)表明可将自进化载体拆成可验证的 Harness 修改和可复用经验资产，并比较二者在跨任务迁移与长期累积上的收益。
- **SystemEvolve**：[VISTA](#vista)提供了“生成系统修改—自主测试—择优保留”的高增益实例，但[EvoAudit](#item-41)提示系统演化目标必须同时纳入可靠性、成本和迁移指标。
- **AgentTrainEvolve**：[Firefly](#firefly)、[WildAWM](#wildawm)与[Agent-R²](#agent-r)可共同启发一条从真实接口探索、可执行环境合成到职业任务证据对齐的分层训练数据管线。
- **EnvironmentEvolve**：[WildAWM](#wildawm)证明纯合成计算机环境能够产生分布外迁移，而[Firefly](#firefly)说明先探索真实 API 再反向出题有助于保证环境的真实性与可验证性。
- **MemoryEvolve**：[Claude 离线“做梦”架构](#anthropic-claude)可作为记忆巩固基线，但[记忆陷阱](#item-44)要求在写回和迁移时加入任务边界、风险等级与确认策略。
- **CacheEvolve**：[QRAE](#qrae)把查询相关注意力熵用于在线筛选和持久化关键片段，为固定预算下联合优化缓存保留、长期记忆写入与检索成本提供了直接方案。
- **EvalEvolve**：[标准暴露研究](#item-32)与[EvoAudit](#item-41)共同说明自进化评测应隔离优化器可见标准，并独立测量迁移、成本和真实任务构念。
- **GeneralizeEvolve**：[RLVR 与 SFT 的受控比较](#sft)表明应把研究重点从榜内平均增益转向可复现的分布外边际收益，并用[标准暴露研究](#item-32)排除验证器过拟合。
- **JevEvolve**：[Drex](#drex)验证了直接输出候选概率的低延迟决策路线，可进一步用于研究快模型的校准、选项顺序鲁棒性及向慢推理升级的路由边界。
- **SwarmEvolve**：[SwarmEvolve](#swarmevolve)提供了共享 KV 缓存、潜空间推理与新颖性筛选相结合的群体搜索设计，可用于降低大规模多智能体进化的通信和评估成本。
- **Awesome-RSI**：[METR 审计](#metr-anthropic-ai)给出了 AI 研发加速的外部量化信号，而[EvoAudit](#item-41)说明 RSI 清单应同步收录能力增长、成本、迁移和目标作弊的审计方法。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-08/  

