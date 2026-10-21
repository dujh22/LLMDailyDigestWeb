# 2026-10-21 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 智能体自进化集中转向“接口—脚手架—模型”协同优化：[Agent S4](#agent-s4)从无成功标签轨迹中演化接口，[Self-HPO](#self-hpo)交替优化交互框架与策略，[MaD-RSI](#mad-rsi)则利用异构模型失败轨迹改进跨模型共享脚手架。
- 长程 Agent 训练的关键环节进一步补齐：[CoworkEnv](#coworkenv)自动合成可执行、可验证的协作环境，[Self-Credit](#self-credit)与[TrajEvolve](#trajevolve)分别以证据引用和反事实验证改善稀疏奖励下的步骤级信用分配。
- 具身自进化从仿真训练走向真机与群体经验闭环：[RLinf v0.4](#rlinf-v0-4)提供模块化真机强化学习基础设施，[从车队经验中学习](#item-15)则让多机器人共享成功轨迹并利用失败上下文持续提升统一策略。
- 自主科研出现经过真实实验验证和符号规律发现的代表性进展：[Claude Science](#claude-science)完成抗蝎毒蛋白设计及湿实验验证，[OptScientist](#optscientist)从数据与文献先验中自动发现可解释的优化定律。
- 评测与安全研究开始追问指标背后的真实能力和可监督性：[DecisionPivot](#decisionpivot-llm)细分诊断决策可靠性，[智能体脚手架优化：能力唤起还是能力扩展？](#item-32)区分已有能力释放与能力边界扩张，而[奖励错设会削弱思维链可监控性](#item-27)揭示奖励作弊可能同步破坏监督信号。
- 系统效率方面，[EdgeRock-4B](#edgerock-4b-kv-cache-99-1)以固定容量状态在256K上下文削减99.1% KV Cache；热点延伸则覆盖 BrainLoRA 脑编码、第一人称三维表征、谱空间轻量化与多轮图像编辑等方向，但与核心研究主线关联较弱。

## 对当前研究的启发
- **CacheEvolve**：[EdgeRock-4B](#edgerock-4b-kv-cache-99-1)证明固定容量“记忆锚点”可同时实现超长上下文、极高缓存压缩与吞吐提升，可作为学习式缓存取舍机制的重要架构参照。
- **AgentEvolve**：[Agent S4](#agent-s4)表明无需成功标签也能从历史轨迹中演化接口及其使用知识，为部署期冻结参数的经验驱动能力增长提供了直接方案。
- **HarnessEvolve**：[智能体脚手架优化：能力唤起还是能力扩展？](#item-32)提示脚手架评测应同时报告可达任务覆盖率与 pass@k，避免把重复采样或既有能力唤起误判为能力扩展。
- **SystemEvolve**：[Self-HPO](#self-hpo)与[MaD-RSI](#mad-rsi)说明系统演化不应孤立搜索工作流，而应把策略模型、失败轨迹和跨模型共享脚手架纳入同一迭代闭环。
- **AgentTrainEvolve**：[Self-Credit](#self-credit)和[TrajEvolve](#trajevolve)可分别提供证据引用式稠密监督与反事实步骤修复，适合组合成面向长程轨迹的信用分配管线。
- **EnvironmentEvolve**：[CoworkEnv](#coworkenv)以能力约束、工作流约束、程序化验证和反馈修复保障环境可执行性，可直接借鉴为长程协作任务的自动环境质检流程。
- **RobotEvolve**：[从车队经验中学习](#item-15)与[RLinf v0.4](#rlinf-v0-4)共同给出“多机器人部署经验汇聚—统一策略更新—真机复现”的具身数据飞轮实现路径。
- **ResearchEvolve**：[Claude Science](#claude-science)和[OptScientist](#optscientist)显示自主科研评测应优先采用湿实验命中率或规律恢复精度等外部可验证结果，而非仅评价生成文本。
- **EvalEvolve**：[DecisionPivot](#decisionpivot-llm)与[奖励错设会削弱思维链可监控性](#item-27)提示评测需把正确率拆解为排序、校准和监督可见性，防止总体分数掩盖不可靠决策或奖励作弊。
- **Awesome-RSI**：[MaD-RSI](#mad-rsi)提供了以异构模型失败为数据的递归改进路线，而[奖励错设会削弱思维链可监控性](#item-27)说明每轮自改进还必须独立审计目标错设与监控信号退化。
- **HumanEvolve**：[人机何时真正互补](#item-31)与[辩论可纠正人类判断，却难以改善弱模型监督](#item-72)共同说明协同增益取决于监督者类型和互补错误结构，不能把对人类有效的辩论机制直接迁移给弱模型裁判。
- **MemoryEvolve**：[WorldMemArena](#worldmemarena)与[ClawMMU](#clawmmu-llm)分别提供记忆生命周期分阶段评测和带来源、权限的访问控制，可用于同时衡量长期记忆效用与安全隔离能力。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-21/  

