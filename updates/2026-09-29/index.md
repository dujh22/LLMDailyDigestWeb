# 2026-09-29 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进向真实环境与具身任务推进：[PhysicalRSI 1.0](#physicalrsi-1-0-robodojo)协同演化规划、执行与 Harness，以较低 Token 成本登顶 RoboDojo；[RSIAgent](#rsiagent)则用多智能体循环将环境反馈沉淀为因果记忆，实现免训练持续适应。
- 多智能体研究同时强化长程协作评测与可验证科研：[AgentWorld](#agentworld)以 MMORPG 任务和因果指标检验角色分工、资源交接与共享计划，[C-HD](#c-hd-lean)展示了多智能体提出新算法并完成 Lean 验证的潜力，也暴露理论复杂度优势未必转化为工程收益。
- 具身与空间智能补齐世界建模、触觉和长期跟踪能力：[InternW0-Δ](#internw0-2)基于逾 2 万小时开放数据统一视觉动力学、几何先验与动作生成，[Tactile-JEPA](#tactile-jepa)学习拓扑感知触觉表征，[TrackEverything](#trackeverything-3d)实现千帧级去重 3D 密集跟踪。
- 长上下文系统优化聚焦阶段解耦与稀疏路由：[解耦量化](#llm)分别优化预填充和解码的格式与存储，[PISA](#pisa)以金字塔式 Top-K 路由和 Triton 内核将块选择降至对数线性复杂度。
- 训练与评测中的“信号是否可信”成为共同问题：[SLCA-GRPO](#slca-grpo)纠正工具调用强化学习的跨片段信用污染，[修辞如何奖励劫持 AI 审稿](#ai-4080)表明内容不变时修辞仍可显著操纵评分，[FoMo](#fomo)则利用扩散轨迹分岔自动生成感知距离监督。
- 视觉生成及应用生态继续扩展：[FuseReg](#fusereg)缓解表征自编码器的重建—生成差距，扩散模型被用于[摄影测量 DSM 修复](#dsm)，而[Jev 生态分析](#jev)从 2170 个项目刻画了低成本决策组件的功能与应用分布。

## 对当前研究的启发
- **Awesome-RSI**：[PhysicalRSI 1.0](#physicalrsi-1-0-robodojo)与[RSIAgent](#rsiagent)分别给出“协同演化 Harness”和“反馈蒸馏为持久因果记忆”两条非参数更新式 RSI 路径，可作为具身与开放环境基线纳入清单。
- **HarnessEvolve**：[PhysicalRSI 1.0](#physicalrsi-1-0-robodojo)说明 Harness 可与规划、执行模块共同成为演化对象，适合用于研究 Harness 改动对性能排名和 Token 成本的独立贡献。
- **MemoryEvolve**：[RSIAgent](#rsiagent)将执行反馈持续蒸馏为可复用因果记忆，为评测记忆写入、验证和跨任务迁移是否真正驱动长期改进提供了具体范式。
- **SwarmEvolve**：[AgentWorld](#agentworld)提供覆盖非对称分工、持续沟通和共享计划维护的长程群体基准，可用于衡量协作结构演化是否产生真实因果增益。
- **LogicEvolve**：[C-HD](#c-hd-lean)展示“多智能体提出算法—形式化验证”的闭环，同时其工程性能落差提示研究中必须把证明正确性、渐近优势和实际效率分层评估。
- **ResearchEvolve**：[C-HD](#c-hd-lean)可作为自主算法发现案例，而[AI 审稿偏差研究](#ai-4080)表明科研闭环中的评审器易被修辞劫持，需引入内容保持改写等对抗审计。
- **EvalEvolve**：[AgentWorld](#agentworld)的因果协作指标与[AI 审稿偏差研究](#ai-4080)的受控改写方法，分别为动态评测群体过程和审计评判器提示敏感性提供了可复用设计。
- **Groom**：[PhysicalRSI 1.0](#physicalrsi-1-0-robodojo)同时报告任务成绩与 Token 成本，结合[AgentWorld](#agentworld)的过程级协作指标，可推动从总成本比较进一步细化到规划、通信、执行和恢复阶段的 Token 归因。
- **JevEvolve**：[Jev 生态分析](#jev)给出的 2170 个公开项目数据可用于识别高频决策场景，并据此确定快模型路由、工具选择和风险检查的优先演化方向。
- **EvolveLRM**：[SLCA-GRPO](#slca-grpo)通过片段锁定和分层奖励隔离工具执行优势与文本偏好优势，为复杂轨迹 RL 中减少错误信用传播提供了直接可用的奖励设计。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-29/  

