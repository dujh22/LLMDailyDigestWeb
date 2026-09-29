# 2026-09-29 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进向具身执行与免训练适应两条路线推进：[PhysicalRSI 1.0：具身智能递归自我改进基线登顶RoboDojo](#条目physicalrsi-1-0-robodojo)协同演化规划、执行与 Harness，[RSIAgent：免训练多智能体在新环境中递归自我改进](#条目rsiagent)则以环境反馈和持久因果记忆形成递归闭环。
- 多智能体研究同时强化长程评测与可验证科研：[AgentWorld：评测多智能体长程协作能力](#条目agentworld)考察角色分工、资源交接和共享计划维护，[多智能体提出C-HD最短路径算法并完成Lean验证](#条目c-hd-lean)展示了“协作发现—形式化证明”的潜力，也暴露理论复杂度与工程性能脱节的问题。
- 具身与空间智能补齐世界模型、触觉和长时程跟踪能力：[InternW0-Δ：基于 2 万小时开放数据的世界动作模型](#条目internw0-2)统一多类运动与动作先验，[Tactile-JEPA：拓扑感知的触觉自监督表征学习](#条目tactile-jepa)学习非规则触觉表征，[TrackEverything：去重 3D 场景表征实现长时程密集跟踪](#条目trackeverything-3d)将密集跟踪扩展至千帧级视频。
- 模型与数据基础设施围绕效率持续优化：[解耦量化：分别优化 LLM 预填充与解码](#条目llm)分阶段配置量化策略，[PISA：对数线性复杂度的块稀疏注意力](#条目pisa)降低长上下文路由复杂度，[RayOrch：血缘可控的多粒度基础模型数据流引擎](#条目rayorch)则以显式血缘和动态批处理支撑异构数据流水线。
- 生成视觉研究覆盖表征融合、条件修复和无标注评测：[FuseReg：正则化层融合缩小表征自编码器的重建—生成差距](#条目fusereg)缓解跨层特征差异，[预训练扩散模型与多模态条件增强摄影测量DSM](#条目dsm)改善城市高程图，[FoMo：以扩散轨迹分岔时刻度量图像感知距离](#条目fomo)利用扩散轨迹自动生成感知距离标签。
- 智能体决策与评判可靠性受到进一步审视：[SLCA-GRPO：纠正工具调用强化学习的跨片段信用归因](#条目slca-grpo)细化工具调用奖励路由，[修辞如何奖励劫持 AI 审稿：4080 次改写揭示评分偏差](#条目ai-4080)揭示内容不变时修辞仍可显著操纵 AI 评分，[Jev 模型功能、应用与生态系统的数据驱动分析](#条目jev)则量化了低成本决策组件的真实应用生态。

## 对当前研究的启发
- **Awesome-RSI**：[PhysicalRSI 1.0](#条目physicalrsi-1-0-robodojo)与[RSIAgent](#条目rsiagent)表明 RSI 可分别通过脚手架协同演化和环境反馈沉淀因果记忆实现，适合纳入具身型与免训练型 RSI 的对照谱系。
- **HarnessEvolve**：[PhysicalRSI 1.0](#条目physicalrsi-1-0-robodojo)将 Harness 明确列为与规划、执行共同演化的对象，为研究 Harness 设计对性能排名及 Token 成本的因果影响提供了直接案例。
- **MemoryEvolve**：[RSIAgent](#条目rsiagent)把执行反馈蒸馏为可持久复用的因果记忆，可用于研究记忆写入、验证和跨任务迁移如何支撑无参数更新的持续适应。
- **SwarmEvolve**：[AgentWorld](#条目agentworld)提供长程协作与因果贡献指标，而[C-HD 工作](#条目c-hd-lean)展示十智能体科研协作实例，两者可分别支撑群体协作机制的标准评测与真实任务验证。
- **LogicEvolve**：[C-HD 工作](#条目c-hd-lean)以 Lean 验证多智能体提出的新算法，为“神经协作生成候选—符号系统验证正确性”的逻辑自进化闭环提供了范例。
- **EvalEvolve**：[AgentWorld](#条目agentworld)的过程与因果协作指标可扩展动态多智能体评测，而[AI 审稿偏差研究](#条目ai-4080)提示演化式评测必须加入语义等价改写下的评分稳定性审计。
- **EvolveLRM**：[SLCA-GRPO](#条目slca-grpo)将执行优势与偏好优势路由到不同片段，为工具增强推理模型设计更精确、低污染的过程奖励与信用分配机制提供了方案。
- **ResearchEvolve**：[C-HD 工作](#条目c-hd-lean)说明形式化验证可作为自主科研的硬反馈，但理论改进未转化为工程加速也提示科研智能体必须同时验证正确性、新颖性和实用价值。
- **JevEvolve**：[Jev 生态分析](#条目jev)从 2170 个公开项目提炼真实功能组合与应用分布，可据此选择高频场景并设计快决策模型的路由边界和持续校准任务。
- **DataEvolve**：[FoMo](#条目fomo)用扩散轨迹分岔自动生成感知距离监督，为无需人工标注的数据合成提供了可计算的质量信号与样本筛选依据。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-29/  

