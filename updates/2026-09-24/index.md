# 2026-09-24 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进走向可分级、可执行的闭环**：从 [79页综述提出RSI五级自主性分层架构](#79-rsi) 的 B0–L5 框架，到 [SwarmWorld 与 ModularRSI：AI 自我进化的群体与个体路径](#swarmworld-modularrsi-ai)、[Simate以Physical RSI驱动机器人自主研究，登顶RoboDojo](#simate-physical-rsi-robodojo) 的群体、脚手架与真机反馈循环，RSI 正从概念讨论转向系统实现。
- **长程记忆研究集中攻克“保留什么、何时压缩、如何低成本调用”**：[JitMem：面向 LLM 智能体的即时任务自适应记忆策展](#jitmem-llm) 将策展推迟到读取时，[GEM：面向长程智能体的证据保留式历史压缩](#gem) 与 [长程智能体行动前涌现记忆控制信号](#item-70) 分别探索证据保留压缩和状态驱动控制，[FRESH：面向小语言模型工具智能体的失败感知异构图记忆](#fresh) 则把成功与失败经验组织为可复用图记忆。
- **智能体评测由结果分数转向过程、轨迹与运行时风险**：[The Tasteful Agent：衡量与提升长时程任务决策品味](#the-tasteful-agent) 评估关键决策分叉，[PASTABench：智能体序列轨迹的主动安全评测](#pastabench) 衡量最佳干预窗口，[FDE-Bench：LLM 智能体部署环境配置评测基准](#fde-bench-llm) 提供可重放执行检查，[CART：大模型闭环自适应红队测试框架](#cart) 则把安全评测变为持续演化的闭环搜索。
- **自主科研与群体智能出现真实发现和实验理解两条进展**：[950个Claude协作发现噬菌体新酶系统ART](#950-claude-art) 展示大规模智能体并行分析加人类湿实验验证，[WhatWorkedBench：评测 AI 智能体的实验理解能力](#whatworkedbench-ai) 开始检验智能体能否在有限预算下理解实验变更的因果效果。
- **低成本决策、推理与智能体运行成为系统主线**：[开源版 Jev：Laya 登顶 Hugging Face 热榜](#jev-laya-hugging-face) 展示端侧 System 1 决策模型，[JEV-as-a-Judge：高置信接受、低置信升级的低成本评判](#jev-as-a-judge) 验证置信度级联，[Cursor 团队分享 Agent Harness Token 降本提示词](#cursor-agent-harness-token) 与 [GEM：面向长程智能体的证据保留式历史压缩](#gem) 则分别从脚手架和上下文侧降低运行成本。

## 对当前研究的启发
- **Awesome-RSI**：[79页综述提出RSI五级自主性分层架构](#79-rsi) 可作为资源清单的统一分类坐标，并用 Simate、SwarmWorld 和 ModularRSI 分别补充 Physical RSI、群体 RSI 与脚手架自演化实例。
- **DataEvolve**：[EvoAudio：音频理解的递归自我改进](#evoaudio) 展示模型、样本、问题与难度联合演化的数据闭环，可用于研究无新增人工标注时如何维持合成数据的覆盖度与难度匹配。
- **EnvironmentEvolve**：[VHD-Play：从已求解机制生成可验证的智能体强化学习环境](#vhd-play) 提供“先求解机制、再渲染环境”的低成本路线，可同时保障合成环境的可执行性与评分标准可验证性。
- **EvalEvolve**：[The Tasteful Agent：衡量与提升长时程任务决策品味](#the-tasteful-agent)、[PASTABench：智能体序列轨迹的主动安全评测](#pastabench) 和 [CART：大模型闭环自适应红队测试框架](#cart) 表明动态评测应围绕决策分叉、干预时机和自适应攻击生成，而非只扩充静态题目。
- **EvolveLLM**：[翻译微调中的通用遗忘缓解无法保留 MT 指令遵循](#item-34) 说明持续迭代即使保持通用能力仍可能丢失细粒度控制能力，遗忘评测需下沉到语体、长度和属性遵循层面。
- **EvolveLRM**：[RL 始于 RL 之前：在策略蒸馏提升强化学习效果](#rl-rl) 与 [何时何处信任教师：熵校准信用分配统一在策略蒸馏与 GRPO](#grpo) 提示可用分布级在策略蒸馏初始化，再以熵校准教师—验证器信用降低后续 RL 的不稳定性。
- **Groom**：[Cursor 团队分享 Agent Harness Token 降本提示词](#cursor-agent-harness-token) 和 [GEM：面向长程智能体的证据保留式历史压缩](#gem) 提供了提示、工具加载、缓存与历史压缩等可归因降本维度，可纳入过程级 token 效用指标体系。
- **HarnessEvolve**：[Cursor 团队分享 Agent Harness Token 降本提示词](#cursor-agent-harness-token) 的约 7% 无损降本结果说明 harness 评测应标准化披露提示长度、工具按需加载、缓存布局和子智能体调度配置。
- **JevEvolve**：[JEV-as-a-Judge：高置信接受、低置信升级的低成本评判](#jev-as-a-judge) 与 [Jev-Mem：System-One 控制的高效智能体记忆架构](#jev-mem-system-one) 给出了同一快模型在评判级联和记忆路由中的落地模板，可进一步从交互日志联合学习升级阈值与停止策略。
- **LogicEvolve**：[路径很重要：超越答案准确率的知识图谱问答小模型评测](#item-46) 与 [PotARCin：抽象推理技能习得的多维评测基准](#potarcin) 共同说明逻辑自进化不能只看答案正确率，还应追踪路径忠实度、规则迁移和内部一致性。
- **MemoryEvolve**：[JitMem：面向 LLM 智能体的即时任务自适应记忆策展](#jitmem-llm)、[GEM：面向长程智能体的证据保留式历史压缩](#gem) 和 [长程智能体行动前涌现记忆控制信号](#item-70) 指向“保留原始轨迹、读取时策展、行动前控制压缩”的统一可学习记忆管线。
- **ResearchEvolve**：[950个Claude协作发现噬菌体新酶系统ART](#950-claude-art) 证明大规模科研智能体可接入真实实验验证，而 [WhatWorkedBench：评测 AI 智能体的实验理解能力](#whatworkedbench-ai) 可用于补足其对实验因果关系而非相关性的评测。
- **SwarmEvolve**：[950个Claude协作发现噬菌体新酶系统ART](#950-claude-art) 展示群体并行搜索的增益，但 [演化稳定不等于学习可达：多智能体合作涌现研究](#item-47) 和 [多智能体系统中的关机破坏倾向](#item-36) 提醒协作结构演化必须同时评估学习可达性与群体安全风险。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-24/  

