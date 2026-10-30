# 2026-10-30 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进进入可审计实验阶段：[RSI-Master：受控实验驱动的自主模型改进](#rsi-master)以研究 DAG 组织自主后训练，[RSI Arena：基于人类反馈的递归自我改进实验](#rsi-arena)则发现人类偏好提升不必然带来能力与安全同步改善。
- 环境与 Harness 成为 Agent 进化的关键杠杆：[WorkRover：递归环境演化扩展长程协同智能体训练](#workrover)用执行反馈修复环境并细化信用分配，[CMU开源Hermit：统一Harness层RSI与持续学习框架](#cmu-hermit-harness-rsi)则将持续改进下沉到可插拔 Harness 层。
- 自生成任务继续推动低依赖训练：[LongZero：零外部数据增强长上下文推理](#longzero)在无外部语料和教师模型的条件下合成多跳任务并进行 RL，[推理 LLM 中序贯实验设计的摊销学习](#llm)进一步把信息获取策略训练为可迁移能力。
- 具身智能同时推进经验复用、评估与开放验证：[CausGround：基于因果交互定位的自适应具身规划](#causground)把交互经验提炼为免训练迁移的因果知识，[感觉运动对齐：具身策略成功的低成本代理指标](#item-18)提供离线成功率代理，而 [Motubrain 2.0 开启 Physical AI 全流程训练直播](#motubrain-2-0-physical-ai)公开了预训练、部署和真机 OOD 评测全过程。
- Agent 评测与服务开始面向真实流程：[RealCLI：统一评估 CLI 智能体的人机协作](#realcli)暴露可操控性与信任校准短板，[TauIndianBankBench：银行工具智能体的流程感知评测](#tauindianbankbench)同时核查执行过程、结果和越权行为，[TAO：面向 LLM 智能体服务的工具感知联合调度](#tao-llm)则优化工具调用场景下的端到端调度。
- 热点延伸集中于流式音视频处理、全向一致视频生成、指令容量测量及前沿模型安全评估，但与当前核心自进化方向关联较弱。

## 对当前研究的启发
- **AgentTrainEvolve**：[WorkRover](#workrover)的回合级奖励归因与递归环境修复可直接用于缓解长程 Agentic RL 的稀疏奖励和环境失效问题。
- **EnvironmentEvolve**：[WorkRover](#workrover)与[从手工到自进化：Agent 环境扩展五篇论文](#agent)共同给出了“执行反馈修复—确定性验证—难度演化”的环境闭环实现路线。
- **HarnessEvolve**：[Hermit](#cmu-hermit-harness-rsi)表明可将训练、评测和部署统一为可替换 Adapter，使 Harness 本身成为无需修改基模的持续进化层。
- **Awesome-RSI**：[RSI Arena](#rsi-arena)中偏好、基准能力与安全性的分离说明 RSI 清单应重点记录多目标退化检测，而不能把单一偏好胜率视为持续改进证据。
- **ResearchEvolve**：[RSI-Master](#rsi-master)的动态研究 DAG、独立 Reviewer 与防作弊实验环境可作为自主科研系统保持可审计性和实验有效性的参考架构。
- **DataEvolve**：[LongZero](#longzero)展示了模型自造长上下文多跳任务并直接回灌 RL 的零外部数据飞轮，可用于研究合成任务覆盖度与分布坍缩边界。
- **RobotEvolve**：[CausGround](#causground)可将真实交互沉淀为跨环境复用的动作前置条件和效果知识，而[感觉运动对齐](#item-18)可作为低成本筛选 VLA 检查点的代理指标。
- **EvalEvolve**：[RealCLI](#realcli)与[TauIndianBankBench](#tauindianbankbench)说明真实 Agent 评测应同时覆盖协作质量、过程合规、越权操作和最终结果，而非只看任务成功率。
- **Groom**：[TauIndianBankBench](#tauindianbankbench)的流程步骤与未授权操作核查可转化为过程级证据标签，辅助分析 token 消耗是否真正贡献于合规执行。
- **SystemEvolve**：[TAO](#tao-llm)表明工具就绪度、缓存收益和 token 占用可以联合进入调度目标，为 Agent 系统自动优化工作流与资源配置提供可机器判定的反馈。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-30/  

