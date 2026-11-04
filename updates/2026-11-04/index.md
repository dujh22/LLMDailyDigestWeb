# 2026-11-04 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 基础模型继续向原生多模态、长程智能体与高效部署收敛：[LongCat-2.5](#longcat-2-5)以真实代码环境强化学习和国产加速卡优化切入，[Mistral Large 4](#mistral-large-4)则以开放权重、稀疏注意力和推理解耦强化软件工程能力。
- 智能体自进化从单体反思扩展到开放世界与群体经验循环：[CUA-Master](#cua-master)以弱点驱动的双循环持续生成可验证任务，[Group-Evolving Agents](#group-evolving-agents)共享轨迹、工具及框架改进经验，[ReTerm](#reterm-code-agent)进一步把失败恢复纳入训练闭环。
- 训练与数据飞轮更强调高价值轨迹、自动课程和真实交互：[SWE-Trail](#swe-trail)从历史检查点分支探索，[NorthCUA](#northcua)规模化积累计算机操作经验，[AutoSFT](#autosft-sft)用多智能体自动修复、合成及编排训练数据。
- Harness 正成为跨环境训练与落地的关键基础设施：[uni-robot-agent](#uni-robot-agent-harness)统一仿真与真机机器人接口，[HarnessSQL](#harnesssql-sql-agent)则以原生 SQL 沙盒和执行奖励支撑真实数据库长程训练。
- 快速自进化也暴露出更严格的验证需求：[RSI 系统优化 Agent 的 Reward Hacking 与验证边界](#rsi-agent-reward-hacking)指出验证强度应随搜索预算增长，[OpenAI 的生产行为研究](#openai)表明评测目标误判会造成安全评测与真实使用之间的系统性落差。
- 长周期应用开始形成专用记忆与科研工作台，[AgentMemory](#openjiuwen-agentmemory)构建视听双流长视频记忆，[Hyra 2.0](#hyra-2-0)沉淀可复用科研工具；热点延伸则集中在实时视频生成、主动视频观察和可解释取景。

## 对当前研究的启发
- **AgentEvolve**：[Group-Evolving Agents](#group-evolving-agents)表明可将跨智能体轨迹、工具和框架修改沉淀为共享经验库，用于验证群体经验是否比单体反思带来更持续的部署期增益。
- **AgentTrainEvolve**：[SWE-Trail](#swe-trail)与[ReTerm](#reterm-code-agent)分别提供历史检查点分支和失败恢复训练机制，可组合成“定位高价值失败—生成恢复轨迹—在线强化”的数据闭环。
- **Awesome-RSI**：[RSI 系统优化 Agent 的 Reward Hacking 与验证边界](#rsi-agent-reward-hacking)给出了应重点收录的安全原则，即搜索预算扩大时必须同步提高独立验证强度与评估器多样性。
- **EvalEvolve**：[OpenAI 的生产行为研究](#openai)说明动态评测不仅要防止模型识别评测，还要审计模型对任务目标的理解是否与生产环境一致。
- **HarnessEvolve**：[uni-robot-agent](#uni-robot-agent-harness)与[HarnessSQL](#harnesssql-sql-agent)显示统一接口、原生执行沙盒和可复现反馈是让同一训练方法跨环境迁移的核心 Harness 组件。
- **DataEvolve**：[AutoSFT](#autosft-sft)将数据诊断、修复、合成和配比编排纳入多智能体闭环，可用于研究数据价值估计如何直接驱动下一轮数据生产。
- **CodeEvolve**：[ReTerm](#reterm-code-agent)把智能体自身制造的终端失败转化为恢复示范，为编码 Agent 建立“失败现场即训练环境”的递归改进路径。
- **MemoryEvolve**：[AgentMemory](#openjiuwen-agentmemory)的事件切分、三层记忆与离线索引组合，为长视频记忆中的写入粒度、层级检索和时延权衡提供了可直接比较的架构。
- **RobotEvolve**：[uni-robot-agent](#uni-robot-agent-harness)提供无需特权输入、同时覆盖仿真与真机的统一底座，可降低持续学习和 sim-to-real 自进化实验的环境差异。
- **ResearchEvolve**：[Hyra 2.0](#hyra-2-0)从一次性解题转向持久任务、经验复用和科学工具产出，提示科研智能体应以可复用研究资产而非单次答案作为核心优化目标。
- **Groom**：[OpenAI 的生产行为研究](#openai)提示过程级评测应单独归因“误判任务目标”所消耗的 token 和错误动作，避免把生产差距笼统归因于评测意识。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-04/  

