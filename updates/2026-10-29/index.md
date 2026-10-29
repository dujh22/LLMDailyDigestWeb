# 2026-10-29 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **模型与个人智能体发布**：OpenAI 推出兼顾桌面操作能力、速度与成本的 [GPT-6.1 Terra](#openai-gpt-6-1-terra-astra)，蚂蚁百灵则开源强化长程任务和工具使用的 [Ling-3.1-flash-1019](#personal-agent-ling-3-1-flash-1019)，智能体竞争进一步从模型指标转向真实任务效费比。
- **递归自我改进走向可执行闭环**：[Apex-35B-V1.0](#35b-apex-35b-v1-0) 将 AI 参与实验、分析与成果回用纳入模型研发，[The Trinity](#the-trinity) 则联合演化可验证环境、能力树和 Harness，体现 RSI 从概念讨论转向系统化实现。
- **工作流与多智能体结构成为主要演化对象**：[Evo²](#evo) 在冻结执行器的条件下协同搜索工作流与演化策略，[DynaFlow](#dynaflow) 学习按任务动态编排子智能体，显示系统级优化正由固定脚手架转向可学习的运行时组织。
- **长期学习与记忆迎来密集检验**（5 条）：[DeepMind：自演化智能体能否持续学习？](#deepmind) 与 [CLE](#cle-llm) 揭示连续任务中的遗忘和跨任务干扰，[Memory Tax](#memory-tax) 质疑复杂记忆系统相对朴素 RAG 的净收益，[TTME](#ttme) 和 [HABIT-Bench](#habit-bench) 分别给出测试时记忆演化与长期用户习惯归纳的新路径。
- **可验证反馈继续推动训练与基础设施自动优化**：[Trajectory2Gym](#trajectory2gym) 以决策依据和依赖覆盖合成工具交互，[ForgeKernel](#forgekernel) 则在华为、英伟达硬件榜单验证跨平台算子自进化，表明数据与系统两端都在形成自动验证闭环。
- **热点延伸集中于主动式与多模态生成**：低相关性条目涵盖 [主动式 AI 的 6A 框架](#ai-6a)、世界一致视频生成、空间音频和长视频取证，反映业界对连续感知、意图预判及复杂时序内容的关注升温。

## 对当前研究的启发
- **Awesome-RSI**：[The Trinity](#the-trinity) 将环境生成、能力刻画和 Harness 演化组成可验证闭环，可作为区分真正递归改进与单轮自优化的系统案例。
- **SystemEvolve**：[Evo²](#evo) 与 [DynaFlow](#dynaflow) 表明可将工作流改写和多智能体编排直接纳入动作空间，并用外部评测或过滤后的轨迹持续优化系统结构。
- **AgentEvolve**：[TTME](#ttme) 证明冻结权重、仅演化外部记忆也能在连续科学任务中超过测试时训练，为部署后免训练自进化提供了高效路线。
- **MemoryEvolve**：[Memory Tax](#memory-tax) 提示记忆研究必须报告相对原始历史检索的净增益及处理成本，而不能只与无记忆基线比较。
- **GeneralizeEvolve**：[DeepMind 的持续学习评估](#deepmind) 与 [CLE](#cle-llm) 可用于系统测量自进化在连续任务流中的可塑性、跨任务迁移和灾难性遗忘。
- **AgentTrainEvolve**：[Trajectory2Gym](#trajectory2gym) 可将“依赖覆盖充分、决策依据明确”作为多轮工具轨迹的生成与筛选准则，改善有状态 Agent 训练数据质量。
- **EnvironmentEvolve**：[The Trinity](#the-trinity) 的 Creator–Explorer–Evolver 分工展示了环境生成器、能力边界探索器与系统优化器协同演化的具体架构。
- **InfraEvolve**：[ForgeKernel](#forgekernel) 在两类硬件评测上的领先结果验证了以正确性和性能为机器反馈、跨后端自动搜索算子的产业可行性。
- **PersonalEvolve**：[HABIT-Bench](#habit-bench) 将个性化能力拆解为从长期弱证据中推断、更新和适时应用习惯，可直接作为个人 Agent 画像演化的评测模板。
- **NewApply**：[GPT-6.1 Terra](#openai-gpt-6-1-terra-astra) 以接近高端模型的电脑操作能力实现数量级成本下降，说明真实桌面 Agent 的落地评估应优先转向单位任务成本、速度与可靠性。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-29/  

