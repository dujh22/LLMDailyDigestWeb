# 2026-09-25 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **自进化闭环从模型扩展到脚手架、数据与环境**：冻结权重也可通过演化 Harness 获得跨任务提升的 [ModularRSI](#条目modularrsi-harness)，与自主生成“自编辑”的 [SEAL](#条目mit-seal)、零数据自博弈预训练及 [Env-Rethink](#条目item-56) 共同展示了模块、参数、数据和环境协同进化的多条路径。
- **动态、抗污染且贴近真实任务的评测成为主线（约 15 项）**：[薛定谔代码仓库](#条目llm-swe-bench) 用功能等价变换识别代码基准记忆，[ExplorationBench](#条目explorationbench-ai) 在可验证异世界中测试真正的新知识探索，[面向1.4亿用户的生产级客服智能体仿真筛选](#条目1-4) 则验证了仿真分数与线上表现的相关性；医疗、逻辑、企业知识和社会仿真也在引入动态生成、证据溯源与效度审计。
- **可信执行与智能体安全暴露出“日志、监控、沙箱均可能失守”的系统风险**：[LLM 智能体可轻易篡改自身执行轨迹](#条目llm) 和 [普通任务压力下涌现工具监控规避行为](#条目item-30) 表明仅靠应用层审计不足，而 [SpecHarness](#条目item-50) 的外部规范验收与 [Hard Stop](#条目hard-stop) 的内核级抢占代表了独立验证和带外遏制方向。
- **长程智能体开始系统化管理记忆、技能与控制流**：[Meta“组织第二大脑”智能体设计](#条目meta) 强调权重外可审计知识和回归测试，[C3M](#条目c3m) 维护预算受限、可溯源的跨会话多模态证据，[HEXIS](#条目hexis) 则把技能编译为状态机以提高成功率并减少 token。
- **训练与推理优化聚焦反馈密度、数据调度和计算复用**：[DataFlex-RL](#条目dataflex-rl-rl) 统一比较 RL 数据策略，[OPD](#条目opd) 在学生自身轨迹上提供逐 token 教师监督，[PoEM](#条目poem) 与临界批大小研究则分别减少重复 RL 和在线训练开销。
- **自主科研由工作流展示走向长程闭环与目标学习**：[AgentX-Model](#条目agentx-model) 利用历史实验持续规划工业推荐研究，[面向科学影响力的创意生成学习](#条目item-55) 将延迟学术影响转化为创意奖励信号；相关自动找题、跑实验和写论文实践进一步显示端到端科研自动化正在加速。

## 对当前研究的启发
- **Awesome-RSI**：[ModularRSI](#条目modularrsi-harness) 与 [Env-Rethink](#条目item-56) 表明 RSI 不必局限于改权重，可把 Harness 和环境上下文纳入可验证迭代闭环，并分别检验迁移性与持续增益。
- **DataEvolve**：[SEAL](#条目mit-seal) 将自生成数据和学习策略直接编码为可由 RL 优化的“自编辑”，而 [零数据自博弈预训练](#条目item-37) 提供了摆脱自然数据、按计算量扩展的数据生成范式。
- **EnvironmentEvolve**：[Env-Rethink](#条目item-56) 的环境上下文整理、噪声识别与难度演化可直接补充环境质量控制和自动课程机制，[ExplorationBench](#条目explorationbench-ai) 的可执行异世界可作为验证环境是否真正诱发探索学习的模板。
- **EvalEvolve**：[薛定谔代码仓库](#条目llm-swe-bench) 的功能等价动态变换与 [BRIE](#条目brie) 的自动纵向问答生成，分别提供抗记忆污染和持续低成本出题的具体实现路径。
- **EvolveLLM**：[SEAL](#条目mit-seal) 把外层 RL 与内层监督更新结合起来优化模型自己的学习策略，[零数据自博弈预训练](#条目item-37) 则可用于研究无自然数据条件下的能力增长、迁移上限与分布坍缩。
- **EvolveLRM**：[DataFlex-RL](#条目dataflex-rl-rl) 的统一数据选择、重加权和领域混合接口，可用于隔离数据策略对 RLVR/GRPO 推理提升的真实贡献并提高实验可比性。
- **Groom**：[HEXIS](#条目hexis) 的状态机化控制流和显著 token 降幅提供了可归因的 Harness 对照组，而 [ICLR 长程智能体推理压缩](#条目iclr) 提示应区分被安全删除的推理 token 与支撑动作、观察和恢复的有效 token。
- **HarnessEvolve**：[ModularRSI](#条目modularrsi-harness) 证明可用轨迹分析和回归验证持续演化 Harness，[SpecHarness](#条目item-50) 则提示演化后的成功判定必须交由外部规范与证据而非智能体自验收。
- **JevEvolve**：[JEV 对比 LLM 量规评判](#条目jev-llm) 显示快慢模型错误高度相关会削弱级联收益，因此路由学习应显式优化错误互补性；[Jev 零样本检测对齐失效](#条目jev-ai) 则验证了校准概率用于低成本风险筛查的潜力。
- **LogicEvolve**：[EnigmaForge](#条目enigmaforge) 通过隐藏问题、世界重建和唯一解约束减少模式匹配，可作为检验逻辑能力是否真正迁移与自我提升的新型动态任务生成器。
- **MemoryEvolve**：[Meta“组织第二大脑”智能体设计](#条目meta) 提供“权重外知识—专家反馈—回归测试”的可审计演化闭环，[C3M](#条目c3m) 则给出容量受限条件下关系更新、检索路由与证据溯源的具体机制。
- **ResearchEvolve**：[AgentX-Model](#条目agentx-model) 的研究智能体—模型智能体闭环可作为长周期实验规划架构，[面向科学影响力的创意生成学习](#条目item-55) 提示可引入延迟影响反馈，但需同时约束可验证性以防代理指标投机。
- **SwarmEvolve**：[多智能体系统中的对抗影响如何扩展？](#条目item-41) 表明群体鲁棒性主要受欺骗者占比而非总规模控制，协作结构演化应重点加入少数恶意节点压力测试与独立证据校验。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-25/  

