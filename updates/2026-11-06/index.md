# 2026-11-06 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进与自主科研转向“实验闭环是否真实有效”：从用实验反馈直接更新预测器的 [WeightLoop：基于实验反馈的权重空间编程](#weightloop)，到端到端能力基准 [FrontierPhysics：端到端物理研究智能体评测基准](#frontierphysics)，而 [验证器更强不等于发现质量更高：提议池构成才是关键](#item-66) 表明候选探索可能比继续增强评判器更重要。
- Agent 训练集中攻克长程信用分配与能力泛化：[TurnWise：回合级信用分配推进流式视频强化学习](#turnwise) 将奖励对齐到逐回合决策；[在策略蒸馏用于强化学习后能力巩固的泛化局限](#item-14) 与 [RLVR只优化解题路径选择，未提升内在推理能力](#rlvr-4) 则共同警示，分布内保持或分数提升不等于能力边界扩展。
- 长期记忆从“保存更多内容”走向状态化、依赖感知与模型—Harness 协同：[StateGraph：面向长期智能体记忆的依赖感知状态修订](#stategraph) 用反事实验证处理事实变更，[千问 Personal Agent：模型、记忆与生态的协同架构](#personal-agent) 则将需求驱动记忆、上下文压缩和失败重规划整合进产品级架构。
- 智能体评测进一步强调可执行证据与真正的能力迁移：[长程智能体失败归因需执行反事实：迈向报告标准](#item-46) 要求用状态回放而非轨迹文本验证归因，[SelfImprove-Bench：自改进智能体泛化能力评测](#selfimprove-bench) 则以分级未见场景检验“自改进”是否只是局部过拟合。
- 系统与物理智能均在形成自主优化闭环：[递归稀疏注意力：以对数成本外推至百万词元](#item-22) 和 [SpecPilot：面向投机解码的自主算法发现与系统优化](#specpilot) 推进长上下文及推理基础设施；[PyRUA-DataFarm：LLM 远程操作者驱动的真实场景机器人数据采集](#pyrua-datafarm-llm) 与 [CUE：通过自主机器人交互弥合动力学鸿沟](#cue) 分别打通数据生成和真机参数辨识。
- 模型发布方面，[OpenAI 发布 GPT-6 Cyber 网络安全模型](#openai-gpt-6-cyber) 将专用安全模型推进到受控实战访问；低相关热点延伸则集中在分钟级游戏世界建模、三维多视图求解、光网络控制和未知游戏实时解说。

## 对当前研究的启发
- **Awesome-RSI**：[SelfImprove-Bench：自改进智能体泛化能力评测](#selfimprove-bench) 可作为 RSI 是否产生可迁移增益的分级测试，而 [验证器更强不等于发现质量更高：提议池构成才是关键](#item-66) 提示改进闭环应优先扩大高质量候选池而非单纯堆强评判器。
- **ResearchEvolve**：[FrontierPhysics：端到端物理研究智能体评测基准](#frontierphysics) 暴露推理严谨性与专家直觉仍是端到端科研瓶颈，[WeightLoop：基于实验反馈的权重空间编程](#weightloop) 则提供了把持续实验结果直接转成可复用模型更新程序的路径。
- **AgentTrainEvolve**：[TurnWise：回合级信用分配推进流式视频强化学习](#turnwise) 表明可在无需价值模型和额外采样的条件下，把长程策略学习信号细化到每次响应或等待决策。
- **GeneralizeEvolve**：[在策略蒸馏用于强化学习后能力巩固的泛化局限](#item-14) 与 [RLVR只优化解题路径选择，未提升内在推理能力](#rlvr-4) 提供了区分“分布内能力保存、路径重加权与真实能力扩展”的三层诊断框架。
- **MemoryEvolve**：[StateGraph：面向长期智能体记忆的依赖感知状态修订](#stategraph) 可用于在上游事实变化时选择性失效下游记忆，[千问 Personal Agent：模型、记忆与生态的协同架构](#personal-agent) 则验证了记忆策略需与模型和 Harness 联合训练。
- **EvalEvolve**：[长程智能体失败归因需执行反事实：迈向报告标准](#item-46) 提示长程评测应保存可恢复环境状态，并以干预回放证书替代仅凭文本轨迹作出的失败归因。
- **SystemEvolve**：[SpecPilot：面向投机解码的自主算法发现与系统优化](#specpilot) 展示了以成本模型、真实部署验证和结构化记忆构成系统优化闭环，可迁移到其他推理算法的自动发现。
- **CacheEvolve**：[递归稀疏注意力：以对数成本外推至百万词元](#item-22) 的递归树状 KV 缓存与分层候选选择，为固定预算下兼顾超长上下文外推和检索效率提供了新结构。
- **RobotEvolve**：[PyRUA-DataFarm：LLM 远程操作者驱动的真实场景机器人数据采集](#pyrua-datafarm-llm) 可将一次真机标定扩展为大规模精确动作数据，而 [CUE：通过自主机器人交互弥合动力学鸿沟](#cue) 可进一步用信息增益驱动的真机交互持续校准数字孪生。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-06/  

