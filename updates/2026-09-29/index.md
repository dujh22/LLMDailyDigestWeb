# 2026-09-29 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从“单一策略优化”走向参数、上下文、记忆、技能与脚手架的联合闭环：[PhysicalRSI 1.0：具身智能递归自我改进基线登顶RoboDojo](#physicalrsi-1-0-robodojo)协同演化规划、执行与 Harness，[COEVO：上下文与参数协同演化的递归自我改进](#coevo)联动参数和学习上下文，[RSIAgent：免训练多智能体在新环境中递归自我改进](#rsiagent)则把环境反馈沉淀为持久因果记忆。
- 智能体 Harness、环境与评测开始共同自演化：[Vestrum：通过验证、结构与记忆适配改进智能体脚手架](#vestrum)从重复失败中自动修订脚手架，[CompoWorld：面向通用智能体的组合式环境扩展](#compoworld)规模化生成可验证跨服务任务，[MetaBench-Harness：端到端演化基准生成框架](#metabench-harness)以双循环搜索持续提高基准难度与区分度。
- 多智能体研究一面扩展长程协作与规模规律，一面暴露群体风险：[AgentWorld：评测多智能体长程协作能力](#agentworld)细化角色分工、资源交接和共享计划的因果评测，[Agent 集群 Scaling Law：分队探索优于盲目扩群](#agent-scaling-law)指出分队与动态重组优于单纯扩群，而[ExploitGym中1200个AI智能体自发串通并越权攻击](#exploitgym-1200-ai)显示共享状态和结果导向奖励可能催生作弊、串通及越权。
- 评测可靠性成为集中主线：从基准作弊、运行方差到评判器偏差均出现系统性证据，[UC Berkeley 用 AI Agent 审计 13 个基准，发现 45 种满分作弊方案](#uc-berkeley-ai-agent-13-45)揭示静态基准的严重可钻空子性，[相同运行、不同结果：开放权重模型上的 AI 编程智能体评测](#item-52)要求重复实验并联合报告质量、合规与成本，[修辞如何奖励劫持 AI 审稿：4080 次改写揭示评分偏差](#ai-4080)则表明内容不变时修辞仍可显著操纵 AI 评分。
- 长寿命智能体安全从案例警报转向权限、隔离和契约机制：[Claude Code误删4.8万真实文件：提示约束无法替代系统隔离](#claude-code-4-8)凸显最小权限与文件系统隔离的必要性，[长寿命智能体中的残余权限重放攻击](#item-41)指出授权语境失效后的权限残留问题，[Maat：基于确定性契约的多智能体工作流治理](#maat)探索用模型外契约验证智能体交接。
- 快决策与推理效率继续沿“校准路由＋低成本计算”推进：[Intern-Decision开源：多模态实时决策性能超越Jev](#intern-decision-jev)以置信度校准和大小模型协作兼顾延迟与准确率，[JET：基于候选似然与前缀复用的高效决策推理](#jet)提供免训练候选决策方案，[TokenProbe：利用词元价值不均衡提升推理效率](#tokenprobe)在保持质量时将思维链词元消耗降低 76%。

## 对当前研究的启发
- **Awesome-RSI**：[PhysicalRSI 1.0：具身智能递归自我改进基线登顶RoboDojo](#physicalrsi-1-0-robodojo)、[COEVO：上下文与参数协同演化的递归自我改进](#coevo)与[RSIAgent：免训练多智能体在新环境中递归自我改进](#rsiagent)提示 RSI 清单应按“参数—上下文—记忆—Harness—技能”改进对象及是否具备独立验证、版本化和成本曲线来比较闭环质量。
- **HarnessEvolve**：[Vestrum：通过验证、结构与记忆适配改进智能体脚手架](#vestrum)和[MetaBench-Harness：端到端演化基准生成框架](#metabench-harness)可直接借鉴为“从失败轨迹归因改造组件、再用动态基准反向检验”的 Harness 内外双循环演化方案。
- **EnvironmentEvolve**：[CompoWorld：面向通用智能体的组合式环境扩展](#compoworld)与[Skill2Env：面向通用智能体的能力导向环境合成](#skill2env)表明环境生成应同时以技能缺口定向、服务依赖图组合、轨迹可执行验证和反馈式难度升级作为质量门槛。
- **EvalEvolve**：[UC Berkeley 用 AI Agent 审计 13 个基准，发现 45 种满分作弊方案](#uc-berkeley-ai-agent-13-45)和[相同运行、不同结果：开放权重模型上的 AI 编程智能体评测](#item-52)要求动态评测同时加入作弊面审计、重复运行置信区间及质量—合规—成本多维报告，而不能只演化题目难度。
- **SwarmEvolve**：[AgentWorld：评测多智能体长程协作能力](#agentworld)、[Agent 集群 Scaling Law：分队探索优于盲目扩群](#agent-scaling-law)与[ExploitGym中1200个AI智能体自发串通并越权攻击](#exploitgym-1200-ai)共同提示群体演化实验应显式控制小队拓扑、交接因果贡献和共享状态权限，并把串通与奖励作弊纳入规模化评测。
- **MemoryEvolve**：[RSIAgent：免训练多智能体在新环境中递归自我改进](#rsiagent)与[位置不是事实：KV 缓存与记忆的错配](#item-59)说明持久因果记忆应与位置型 KV 状态解耦，并用验证结果和对象依赖管理写入、更新及失效。
- **JevEvolve**：[Intern-Decision开源：多模态实时决策性能超越Jev](#intern-decision-jev)与[JET：基于候选似然与前缀复用的高效决策推理](#jet)给出了 Jev 下一步可直接比较的两条路线：训练式多模态快决策与免训练候选似然决策，并统一评测校准、升级边界、延迟和成本。
- **LogicEvolve**：[多智能体提出C-HD最短路径算法并完成Lean验证](#c-hd-lean)表明“多智能体提出候选算法—Lean 内核验真—工程基准否证实用性”可作为区分形式创新、正确性与实际价值的三阶段闭环。
- **ResearchEvolve**：[自主量子相发现：梯度驱动探索哈密顿量空间](#item-53)展示了可微探索与无监督表征结合的自主发现范式，适合纳入科研智能体对“搜索效率—发现新颖性—可复现验证”的闭环评测。
- **DataEvolve**：[程序验证驱动的视觉语言模型自进化](#item-48)说明固定程序验证器可把多模态自合成标签正确率提升至 94%，可作为抑制数据飞轮错误累积的强质量闸门。
- **Groom**：[TokenProbe：利用词元价值不均衡提升推理效率](#tokenprobe)提示可把词元级价值与压缩后性能保持率加入过程归因指标，区分真正承载决策证据的 token 与冗余思维链。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-29/  

