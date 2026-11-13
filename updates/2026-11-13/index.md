# 2026-11-13 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **冻结参数的智能体自进化形成多条可落地路径**：[VbD](#vbd) 协同演化执行器与评估器，[HyperSkill](#hyperskill-grpo) 以超图组织可审计技能，[MIGRO](#migro) 则让经验作为持久状态跨模型迁移。
- **评测开始深入真实过程而非只看最终成功率**：[TestPrism](#testprism-coding-agent) 揭示单参考实现会把测试生成成绩高估一倍以上，[RSI-PDEbench](#rsi-pdebench) 检验自改进的泛化与效率，[终止滞后研究](#item-32) 则定位编程智能体解题后的冗余消耗。
- **训练研究同时推进长程信用分配、有效探索与泛化辨析**：[TreeOPSD](#treeopsd) 用树式信用估计改善深度研究智能体，[有效熵与 VEPO](#llm) 将探索约束到有效推理空间，而 [SFT 与 RL 再比较](#rl-sft-sft) 表明数据来源、规模和解法多样性足以逆转既有泛化结论。
- **可验证闭环正从数学证明延伸到算法与系统优化**：[Claude Code 形式化哥德巴赫证明](#claude-code) 在大型 Lean 工程中发现原证明错误，[AutoAssumption](#autoassumption-ml) 通过放宽可证明假设自动发现新算法，[TraceKV](#tracekv-kv) 则提供免训练的策略保持缓存压缩。
- **Google 集中发布快决策与通用智能体模型**：[Gemini Decision 1](#google-gemini-decision-1) 将多模态选择、评分和置信度压缩到单次前向传播，[Gemini 4 Hydrogen](#google-deepmind-gemini-4-hydrogen) 则面向长上下文编码、搜索和多模型智能体工作流全面开放。
- **热点延伸共 4 项**，集中在跨模态表征对齐、按不确定性动态切换精度、智能体推理服务资源调度和 GPU 科学计算求解器，暂未进入今日重点。

## 对当前研究的启发
- **AgentEvolve**：[VbD](#vbd) 与 [HyperSkill](#hyperskill-grpo) 表明冻结权重后仍可通过验证器协同演化和可审计技能图持续增益，可作为“执行—验证—技能沉淀”统一闭环的两类实现。
- **AgentTrainEvolve**：[TreeOPSD](#treeopsd) 的树式轮次信用估计可直接用于长程工具调用训练，减少单一轨迹级奖励对中间关键决策的信号稀释。
- **Awesome-RSI**：[RSI 持续进步评测](#rsi-rsibench-data-s-gym) 与 [RSI-PDEbench](#rsi-pdebench) 共同提示清单应明确记录版本轨迹、计算预算、历史峰值和未见任务表现，而不能仅收录最终分数。
- **EvalEvolve**：[TestPrism](#testprism-coding-agent) 证明基于单一参考答案的代码评测存在系统性高估，因此动态基准应同时纳入多个正确实现与错误实现来测量测试辨别力。
- **CodeEvolve**：[终止滞后研究](#item-32) 显示正确补丁往往早于智能体停止出现，可据此训练或搜索基于执行证据的早停策略，避免冗余探索甚至答案回退。
- **EvolveLRM**：[有效熵与 VEPO](#llm) 提供了比原始输出熵更可靠的探索目标，可用于区分“有效推理多样性”与仅增加无效轨迹的表面多样性。
- **GeneralizeEvolve**：[SFT 与 RL 再比较](#rl-sft-sft) 说明比较自进化方法时必须对齐 rollout 预算、数据来源和解法多样性，否则容易把数据优势误判为算法泛化优势。
- **MemoryEvolve**：[MIGRO](#migro) 的跨模型持久状态接口与“历史必须匹配真实世界状态”的发现共同表明，记忆迁移应绑定可核验环境状态，而非只清洗文本记录。
- **SystemEvolve**：[AutoAssumption](#autoassumption-ml) 展示了以形式化假设为搜索空间、以证明和实测为双重验证器的系统算法进化路线，可迁移到缓存、剪枝和调度优化。
- **JevEvolve**：[Gemini Decision 1](#google-gemini-decision-1) 与 CAPS 日志反馈决策头说明快决策模型可同时输出候选评分和校准置信度，并借部署日志持续学习“直接决定还是升级慢思考”的边界。
- **PersonalEvolve**：[Personal Agent 北极星指标](#personal-agent) 将评价中心从 DAU 转向事务托管量、完成率、长期留存与人工接管率，为个性化智能体的长期价值评测提供了可操作指标组。
- **LogicEvolve**：[Claude Code 形式化哥德巴赫证明](#claude-code) 表明大规模形式化工程不仅能验证既有结论，还能主动暴露论文中的数值和不等式错误，可作为逻辑自进化的高质量反馈源。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-13/  

