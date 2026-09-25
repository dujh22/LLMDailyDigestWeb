# 2026-09-25 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 自我改进从“更新模型”扩展到“演化系统组件”： [ModularRSI：冻结模型权重实现 Harness 持续自我改进](#条目modularrsi-harness)通过迭代修改并验证 Harness 获得跨任务、跨模型增益，[Meta“组织第二大脑”智能体设计：可审计知识与自改进闭环](#条目meta)则将机构知识、推理程序和反馈回归置于权重之外。
- 后训练开始细化数据与监督信号的控制：[北大开源 DataFlex-RL：统一接入与公平比较 RL 数据策略](#条目dataflex-rl-rl)统一比较动态数据选择、重加权和领域混合策略，[OPD：模型如何从自身生成轨迹学习](#条目opd)以在策略轨迹上的逐 token 教师监督兼顾分布匹配与稠密反馈。
- 动态、抗记忆评测成为代码智能体能力辨析的关键：[薛定谔代码仓库：LLM 学会还是记住了 SWE-bench？](#条目llm-swe-bench)利用功能等价的仓库变换揭示 SWE-bench 成绩中存在仓库线索记忆成分，凸显静态基准的污染与推理失真风险。
- 多模态长程任务围绕“状态记忆—交互学习—闭环决策”推进：[Spatial-Interactor：通过物理交互学习空间推理](#条目spatial-interactor)从真实与模拟轨迹学习物理状态转移，[过去塑造未来：自回归视频生成中的记忆机制综述](#条目item-7)系统梳理时序记忆机制，[PackLab：机器人料箱装箱多模态模型综合框架](#条目packlab)则打通仿真、训练和标准化评测。
- 科研与创作自动化继续走向端到端执行：[AI Skill 自动发现科研 Idea 并运行实验](#条目ai-skill-idea)和[AI自主跑实验并生成论文](#条目item-14)展示从创意、实验到写作的无人值守工作流，而[Claude Opus 5.5 纯代码生成视频、3D 与游戏应用](#条目claude-opus-5-5-3d)体现代码智能体向视觉应用快速交付的扩展。

## 对当前研究的启发
- **HarnessEvolve**：[ModularRSI：冻结模型权重实现 Harness 持续自我改进](#条目modularrsi-harness)表明可把执行轨迹分析、模块修改和回归验证直接做成 Harness 的自动演化闭环，并以跨模型迁移检验改进是否独立于底座。
- **Awesome-RSI**：[从 AI Build AI 到真正 RSI：自进化闭环的实践路径](#条目ai-build-ai-rsi)与 ModularRSI 共同提示资源清单应区分局部组件优化和改进机制自身可迭代的真正 RSI，并重点记录闭环层级与持续增益证据。
- **MemoryEvolve**：[Meta“组织第二大脑”智能体设计：可审计知识与自改进闭环](#条目meta)提供了以权重外知识、显式推理程序、专家反馈和回归测试共同驱动记忆演化的可审计架构范式。
- **EvolveLRM**：[北大开源 DataFlex-RL：统一接入与公平比较 RL 数据策略](#条目dataflex-rl-rl)和[OPD：模型如何从自身生成轨迹学习](#条目opd)可分别用于研究 RL 推理训练中的数据配比演化与在策略稠密监督，从而联合改善探索效率和训练稳定性。
- **EvalEvolve**：[薛定谔代码仓库：LLM 学会还是记住了 SWE-bench？](#条目llm-swe-bench)证明功能等价的动态仓库变换可作为抗污染评测原语，用于分离仓库记忆、表面线索利用与真实仓库级推理。
- **JevEvolve**：[Jev掀起类型安全决策模型研究热潮](#条目jev)提示应优先评测候选选项扰动下的概率校准与稳定性，并探索其在模型评判、动作路由和记忆管理中的低延迟闭环学习。
- **ResearchEvolve**：[AI Skill 自动发现科研 Idea 并运行实验](#条目ai-skill-idea)和[AI自主跑实验并生成论文](#条目item-14)为端到端科研智能体提供了工作流样例，但应进一步纳入创意新颖性、实验可复现性和论文结论可追溯性验证。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-25/  

