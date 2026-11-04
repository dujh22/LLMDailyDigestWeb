# 2026-11-04 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进走向开放式、群体化演化**：除以双循环自动合成可验证任务的 [CUA-Master](#cua-master) 外，[Group-Evolving Agents](#group-evolving-agents) 将经验共享扩展至智能体群组，[Awesome RSI](#awesome-rsi-ai) 则给出覆盖方法、基准与开源系统的领域全景。
- **长程 Agent 的训练与运行底座加速成熟**：[HarnessSQL](#harnesssql-sql-agent) 以真实执行沙盒和执行奖励让 8B Agent 超越多个 32B 专用模型，[CoworkOS](#coworkos) 则通过策略—执行分离、子智能体委派和持久工作区支撑真实生产力任务。
- **评测重点从最终成功转向轨迹、恢复与安全边界**：[Storage Agent Family](#storage-agent-family) 建立可追溯的持续评测闭环，[ReTrace](#retrace) 专门测量错误后的状态恢复能力，而 [RSI 系统优化 Agent 的 Reward Hacking](#rsi-agent-reward-hacking) 指出验证强度必须随自改进搜索预算同步增长。
- **模型与具身系统均出现重要工程发布**：美团 [LongCat-2.5](#longcat-2-5) 将原生多模态、真实代码环境 RL 与国产加速卡优化结合，[uni-robot-agent](#uni-robot-agent-harness) 则提供跨仿真和真机、可继续训练的开放机器人 Harness。
- **热点延伸集中于高速视频生成与主动视觉观察**：[Wave Forcing](#wave-forcing) 展示 134.8 FPS 的流式长视频生成，[Reviso](#reviso) 以主动感知和验证引导 RL 改进视频字幕，但二者与当前自进化主线关联较弱。

## 对当前研究的启发
- **AgentEvolve**：[Group-Evolving Agents](#group-evolving-agents) 表明可将成功轨迹、工具和 Harness 改进经验作为群体共享的推理时资产，突破单 Agent 独立积累经验的上限。
- **AgentTrainEvolve**：[HarnessSQL](#harnesssql-sql-agent) 证明原生执行沙盒、全轨迹 SFT 与执行奖励 RL 的组合可让小模型获得强长程工具交互能力，可直接参考其训练闭环设计。
- **Awesome-RSI**：[Awesome RSI](#awesome-rsi-ai) 可作为现有清单的结构化补全来源，而 [RSI 系统优化 Agent 的 Reward Hacking](#rsi-agent-reward-hacking) 提供了“验证预算随搜索预算扩张”的关键安全收录原则。
- **SwarmEvolve**：[Group-Evolving Agents](#group-evolving-agents) 将进化单位由个体提升为群组，为研究知识传播、工具共享和群体持续演化提供了直接范式。
- **HarnessEvolve**：[uni-robot-agent](#uni-robot-agent-harness)、[Storage Agent Family](#storage-agent-family) 与 [ReTrace](#retrace) 分别补足跨环境统一接口、可追溯持续评测和错误恢复测试，可组合成更完整的 Agent Harness 评测栈。
- **Groom**：[Storage Agent Family](#storage-agent-family) 的 Trace 归因与双评估器机制可用于把 token 消耗映射到具体任务行为和失败环节，增强过程级利用效率审计。
- **RobotEvolve**：[uni-robot-agent](#uni-robot-agent-harness) 提供无需特权输入、贯通仿真与真机且支持后续训练的统一底座，可降低具身数据回流与持续学习实验成本。
- **SystemEvolve**：[RSI 系统优化 Agent 的 Reward Hacking](#rsi-agent-reward-hacking) 警示系统搜索越强越会放大代理指标偏差，因此每轮架构或代码变异都应配套独立验证器与递增审计预算。
- **NewModel**：[LongCat-2.5](#longcat-2-5) 展示了原生多模态、长程 Agent RL 和国产硬件全栈协同的新模型发布路线，[O³PD](#o-pd) 则提供无需教师概率校准的轻量在策略蒸馏方案。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-04/  

