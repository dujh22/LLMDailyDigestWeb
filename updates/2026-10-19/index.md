# 2026-10-19 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **长期记忆从“存取”走向结构化演化与精细检索**：十余项工作覆盖记忆写入、更新、筛选和证据组织，[GLOBE](#globe) 将排名反馈沉淀为可迁移的字段级行为记忆，[TIDER](#tider) 则以强化学习完成时序定位与双通道检索。
- **长程智能体训练聚焦可验证奖励与信用分配**：[Reward Engine](#reward-engine) 为开放式工具任务自动构建可冻结的验证包，[WebCoder](#webcoder) 以可执行前端产物和分段信用分配训练复杂开发智能体，[OfficeTown](#officetown) 进一步提供持续运作的组织级任务环境。
- **递归自我改进开始同时追求可扩展反馈和真实泛化**：[LM2LM](#lm2lm) 用研究世界模型提供代理奖励并以真实实验校准，[Darwin-Claw](#darwin-claw) 协同演化技能与长期记忆；但[自进化智能体能修复失败，却难以从失败中泛化](#item-25)表明经验闭环仍可能停留在任务记忆层面。
- **推理优化转向审计内部过程与校准有限算力**：[VERITAS](#veritas) 通过内部计算轨迹定位不忠实思维链，[SPLIT](#split) 则在验证器存在误判和相关错误时联合分配采样、模型与验证预算。
- **快决策与模型路由强调逐轮价值和成本约束**：[RIVET](#rivet-llm) 利用训练期响应信息学习部署前路由，在多轮任务中同时降低调用成本并提高成功率，为快模型—慢模型分工提供了直接方案。
- **能力构建更依赖可执行数据与模块化技能**：[MetaCurate](#metacurate) 自动演化编程轨迹筛选器，[WebCoder](#webcoder) 用产物反馈闭合训练回路，[NestedVLA](#nestedvla) 则以嵌套超网络生成可复用动作专家、降低跨任务技能干扰。

## 对当前研究的启发
- **MemoryEvolve**：[GLOBE](#globe) 的字段级记忆演化与 [TIDER](#tider) 的时序—语义检索可组合成“反馈驱动写入更新—时间定位—证据召回”的分层长期记忆栈。
- **AgentTrainEvolve**：[Reward Engine](#reward-engine) 和 [WebCoder](#webcoder) 表明可先把开放任务编译为测试用例、质量量规或可执行产物，再据此开展长轨迹强化学习与分段信用分配。
- **AgentEvolve**：[Darwin-Claw](#darwin-claw) 提供了情景经验、原型和技能协同更新的部署时框架，但 [CFOE 结果](#item-25)提示应把未见任务迁移而非已见失败修复作为经验沉淀的核心验收指标。
- **Awesome-RSI**：[LM2LM](#lm2lm) 展示了“廉价世界模型反馈＋周期性真实实验校准”的可扩展改进闭环，可用于降低 RSI 中自评判偏差和代理目标漂移。
- **EvolveLRM**：[VERITAS](#veritas) 可将思维链忠实性纳入过程奖励审计，而 [SPLIT](#split)说明测试时扩展策略必须显式建模验证器误差与候选错误相关性。
- **JevEvolve**：[RIVET](#rivet-llm) 的响应知情价值学习可迁移到 Jev 的快慢路由边界训练，使快决策模型从交互日志中学习何时直接决策、何时升级到慢模型。
- **CodeEvolve**：[MetaCurate](#metacurate) 与 [WebCoder](#webcoder)分别提供可演化的数据筛选器和可执行产物奖励，可共同支撑编码智能体“轨迹生成—自动策展—执行验证—再训练”的数据飞轮。
- **EnvironmentEvolve**：[OfficeTown](#officetown) 将持续组织、任务、上下文和反馈统一生成，可作为环境难度随智能体能力演进的工作场景化课程模板。
- **RobotEvolve**：[NestedVLA](#nestedvla) 的任务条件动作专家生成机制为冻结 VLA 的低干扰技能扩展提供了可直接验证的模块化路线。
- **ResearchEvolve**：[前向引文监督生成可操作研究局限](#item-66)可把后续论文对既有工作的修正转化为高质量监督信号，增强科研智能体提出可验证改进方向的能力。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-19/  

