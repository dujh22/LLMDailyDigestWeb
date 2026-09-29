# 2026-09-29 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从单一策略迭代走向系统级闭环：[PhysicalRSI 1.0](#physicalrsi-1-0-robodojo)协同演化规划、执行与 Harness，[RSIAgent](#rsiagent)将环境反馈沉淀为因果记忆，[COEVO](#coevo)和[R² Flow](#r-flow)则分别探索上下文—参数协同演化与可验证技能库更新。
- Harness、环境与评测开始共同演化：[Vestrum](#vestrum)和[Raven](#raven)自动改造智能体脚手架，[Skill2Env](#skill2env)与[CompoWorld](#compoworld)规模化合成可执行环境，[MetaBench-Harness](#metabench-harness)进一步以双循环搜索持续生成高区分度动态基准。
- 智能体安全集中暴露出“提示约束不足、权限与隔离必须系统化”的问题：[ExploitGym](#exploitgym-1200-ai)出现群体串通与越权，[Claude Code 误删文件](#claude-code-4-8)和[残余权限重放攻击](#item-41)揭示长寿命权限风险，而[SPACE 沙箱红队测试](#perplexity-space-vm)表明 VM 隔离仍可能被网络侧旁路。
- 智能体评测正由终局得分转向过程、方差与可攻击性审计：[UC Berkeley 基准审计](#uc-berkeley-ai-agent-13-45)发现 45 种满分作弊方案，[相同运行、不同结果](#item-52)量化运行间波动，[A³Bench](#item-65)和[可靠 LLM-as-a-Judge 系统](#llm-as-a-judge)则加强轨迹归因与持续测量。
- 多智能体研究同时推进协作能力、组织结构与风险治理：[AgentWorld](#agentworld)评测长程非对称协作，[Agent 集群 Scaling Law](#agent-scaling-law)支持分队探索与动态重组，[身份依赖性从众](#item-82)和[LLM 社会群体风险](#llm-6)则显示群体涌现不能由单体安全性简单推出。
- 训练与推理效率继续细化到阶段、词元和决策层：[解耦量化](#llm)分别优化预填充与解码，[PISA](#pisa)实现对数线性块稀疏路由，[TokenProbe](#tokenprobe)压缩低价值思维链词元，而[Intern-Decision](#intern-decision-jev)与[JET](#jet)探索低延迟候选决策及计算复用。

## 对当前研究的启发
- **Awesome-RSI**：[RSIAgent](#rsiagent)、[COEVO](#coevo)与[R² Flow](#r-flow)给出了因果记忆、上下文—参数协同和版本化技能三种可组合闭环，可据此建立“改进对象—验证器—持久状态”统一分类与单调性评测。
- **HarnessEvolve**：[PhysicalRSI 1.0](#physicalrsi-1-0-robodojo)和[Vestrum](#vestrum)表明 Harness 可从失败轨迹中自动演化且直接改变能力—Token 前沿，适合纳入配置版本、改动归因和跨模型迁移性测量。
- **EvalEvolve**：[MetaBench-Harness](#metabench-harness)、[UC Berkeley 基准审计](#uc-berkeley-ai-agent-13-45)与[相同运行、不同结果](#item-52)提示动态评测必须同时演化题目、审计作弊面，并以重复运行报告方差与成本。
- **EnvironmentEvolve**：[Skill2Env](#skill2env)和[CompoWorld](#compoworld)可作为“技能需求生成任务—依赖图组装环境—执行反馈调难—验证轨迹”的环境生产流水线原型。
- **MemoryEvolve**：[RSIAgent](#rsiagent)与[SelfSuite](#selfsuite)展示了验证结果驱动的因果记忆和热启动记忆，而[KV 缓存与记忆错配](#item-59)说明状态更新必须显式解耦事实、对象依赖与位置。
- **SwarmEvolve**：[AgentWorld](#agentworld)可补充交接、通信和共享计划指标，[Agent 集群 Scaling Law](#agent-scaling-law)提供分队重组假设，[ExploitGym](#exploitgym-1200-ai)则要求把隐式通信、串通与奖励作弊纳入群体演化约束。
- **JevEvolve**：[Intern-Decision](#intern-decision-jev)、[Jev 医疗能力基准](#jev-2)和[System One 安全决策评测](#system-one)共同表明快决策模型的核心竞争点应从纯延迟扩展到校准、选择性升级及分布外高置信度漏检控制。
- **LogicEvolve**：[C-HD 及 Lean 验证](#c-hd-lean)展示了多智能体提出算法、形式化证明与工程实测的完整链路，[SIV](#siv-nl-fol)则可用于区分逻辑翻译中的表面匹配与真实语义正确性。
- **DataEvolve**：[程序验证驱动的 VLM 自进化](#item-48)与[上下文训练数据合成](#item-70)说明固定程序验证和受控文档扰动可分别提高合成标签正确率与上下文依赖性，适合作为数据飞轮的双重质量门。
- **ResearchEvolve**：[自主量子相发现](#item-53)与[ALDER](#alder)提供主动实验和机制修正范式，而[EverMine](#evermine-alpha)警示科研能力积累不必然转化为最终成果，应分开评测过程能力与终局效用。
- **EvolveLLM**：[FIRE](#fire-fisher)以 Fisher 信息为正确与错误输出设置不同更新半径，为反馈式自蒸馏中的稳定更新和错误抑制提供了可操作机制。
- **EvolveLRM**：[EAPO](#eapo-llm)和[TGRL](#tgrl-llm)分别利用策略熵及温度组间奖励差改善探索信用分配，可用于减少 RL 推理训练中的重复失败并提高固定 rollout 预算的利用率。
- **Groom**：[TokenProbe](#tokenprobe)的词元价值压缩与[编程智能体运行方差研究](#item-52)提示过程级 Token 评测应同时记录有效证据密度、重复运行方差、任务质量和成本，而不能只比较单次成功率。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-29/  

