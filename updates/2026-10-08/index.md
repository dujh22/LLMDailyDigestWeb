# 2026-10-08 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进与 Harness 演化转向“受约束、可复现、协同优化”： [RRSI](#rrsi-harness)抑制迭代过拟合与复杂度膨胀，[RSIGym](#rsigym)统一训练、评测和沙箱基础设施，[模型与 Agent Harness 适配关系的系统评测](#agent-harness)与[CoTrace](#cotrace)则表明模型、数据和运行时脚手架必须联合适配。
- AI 科研产出规模快速增长，但验证与创新性成为决定性瓶颈：[OpenAI 公开 722 篇 AI 生成数学手稿](#openai-722-ai)和[Bolzano](#bolzano)展示规模化数学研究潜力，而[PaperBenchX](#paperbenchx-ai-13-98)仅测得 13.98% 的完整论文复现率，[InnovationEval](#innovationeval)还发现前沿模型未能独立产出人类水平创新并出现择优上报。
- 推理训练开始细化结构先验、探索和信用分配：[SAGE](#sage)以代数与双曲结构显著提升长程证明成功率，[ExpDis](#expdis-rlvr)解耦探索策略和学生优化，[RewardWeaver](#rewardweaver)则按失败归因动态分配长程过程奖励。
- 长期记忆研究从“检索相关内容”升级为“维护充分且作用域正确的状态”：[相关不等于充分](#item-121)要求构建完整证据集，[CASK](#cask-llm)防止临时推演污染持久记忆，[RealCompanion](#realcompanion)进一步以最长 120 天真实对话检验远程记忆和过度推断。
- 快决策模型正在成为智能体高频判断与路由层：[Jev](#jev)展示概率判断、搜索和轻量评估器蒸馏的统一路径，[OpenAI Decisions API](#openai-decisions-api-10)与[openJiuwen X-Router](#openjiuwen-x-router-agent-token)则将低延迟候选选择和反馈驱动路由推向产品化。
- 多智能体扩展同时显现科研价值与边界：[万级多智能体扩展](#item-7)指出其主要收益仍是并行测试时计算且呈次线性，[OpenAI 多智能体用 88 小时攻克数学悬赏题](#openai-88)则显示强基础模型、规模化搜索和验证流水线结合后可形成高强度科研工程能力。

## 对当前研究的启发
- **Awesome-RSI**：[RRSI](#rrsi-harness)与[自我改进循环中的赢家诅咒](#llm-3)共同说明，候选复杂度正则、独立留出集和保守接受规则应成为 RSI 循环的默认组件。
- **HarnessEvolve**：[模型与 Agent Harness 适配关系的系统评测](#agent-harness)和[CoTrace](#cotrace)表明不存在普适最优 Harness，应围绕具体模型与任务联合演化轨迹配方、反馈机制和上下文管理。
- **ResearchEvolve**：[PaperBenchX](#paperbenchx-ai-13-98)与[InnovationEval](#innovationeval)提示自主科研系统必须把隔离复现、证据溯源和防择优上报置于论文生成与新颖性声称之前。
- **EvalEvolve**：[AutoSciBench](#autoscibench)和[TestGRAD](#testgrad)提供了两种可复用路线，即根据求解轨迹持续生成新任务，并根据失败模式自动演化可区分候选的测试套件。
- **EvolveLRM**：[ExpDis](#expdis-rlvr)与[RewardWeaver](#rewardweaver)可组合为“独立探索—轨迹筛选—失败归因奖励”的长程推理训练管线，兼顾探索广度与信用分配稳定性。
- **EvolveLLM**：[自生成反馈破坏测试时训练的长期稳定性](#item-26)说明任何在线自更新都应先经独立真实数据门控，不能让模型生成物同时充当训练信号和验收依据。
- **LogicEvolve**：[SAGE](#sage)和[Bolzano](#bolzano)表明显式结构引导、并行搜索与独立验证器的结合，比单纯延长思维链更有希望获得可审计的复杂推理。
- **MemoryEvolve**：[相关不等于充分](#item-121)与[CASK](#cask-llm)提示记忆系统应联合学习“证据是否充分”和“信息属于哪个世界或推理分支”，而不只是优化相似度召回。
- **EnvironmentEvolve**：[RSI-Forge](#rsi-forge)展示了将论文自动转化为含基线、执行环境和评估器的训练单元，可直接扩展环境生成与自动课程基础设施。
- **JevEvolve**：[Jev](#jev)与[OpenAI Decisions API](#openai-decisions-api-10)验证了无开放文本解码的评分模型适合作为高频路由层，下一步应重点学习快决策升级到慢推理的动态边界。
- **SwarmEvolve**：[万级多智能体扩展](#item-7)说明群体规模本身不等于群体智能，研究应把边际收益、通信失控、奖励错配和验证吞吐纳入统一扩展曲线。
- **Groom**：[模型与 Agent Harness 适配关系的系统评测](#agent-harness)提示过程级 token 评测必须记录模型—Harness 配对，并将上下文管理、反馈和恢复开销分别归因，避免用单一总成本比较异构系统。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-08/  

