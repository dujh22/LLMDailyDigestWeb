# 2026-10-25 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 具身智能的经验复用与长期记忆成为主线（3 条）：[RoboSkill](#roboskill) 将触觉反馈与文字、代码技能库结合以支持跨任务复用，[WholeBodyMem](#wholebodymem) 则以对象追踪和事件关键帧应对动态、部分可观测操作。
- 测试时适应与反思记忆继续推动免参数自进化：[METTA](#metta) 通过因果神经记忆和回合摘要实现双时间尺度适应，[Reflexion 机制解读](#rsi-reflexion) 展示了“执行—评估—反思—写回”的经典闭环。
- Agent 与推理模型的强化学习重点转向训练稳定性：[ARLArena](#arlarena) 以统一平台和 SAMPO 改善多轮 Agentic RL 的稳定性与复现性，[DAPO 对策](#dapo) 则从熵坍塌机制解释策略训练为何过早失去探索能力。
- RSI 方法论进一步体系化：[RSI，正在重走深度学习的老路](#rsi) 将递归自我改进与优化、反向传播、元学习、蒸馏及持续学习逐一对应，为分析长期迭代的稳定性与泛化提供统一视角。
- AI 同行评审出现值得警惕的相反证据：[Claude 审稿对照实验](#claude) 报告其全面优于资深专家，而[顶刊论文 LLM 评审可靠性评测](#llm) 发现模型意见不一致且缺陷检出率偏低，说明结论高度依赖评测设计与任务分布。
- 系统与应用侧呈现端侧部署、人机共创和技能生态三条落地路径：[Ember](#30b-ember) 探索学习式调度驱动的端侧推理自进化，[CoWriter](#cowriter-llm) 强调保持用户认知参与；热点延伸方面，[VAST](#vast) 关注离线强化学习的长程信用分配。

## 对当前研究的启发
- **AgentEvolve**：[RoboSkill](#roboskill) 与 [Reflexion](#rsi-reflexion) 分别给出成功技能沉淀和失败反思写回的实现，可组合成同时积累正反经验的部署时进化闭环。
- **MemoryEvolve**：[METTA](#metta) 的因果神经记忆与回合摘要、[WholeBodyMem](#wholebodymem) 的事件驱动关键帧共同表明，记忆系统应按不同时间尺度和事件价值选择性写入，而非完整保存轨迹。
- **RobotEvolve**：[RoboSkill](#roboskill) 的跨模型技能复用和 [WholeBodyMem](#wholebodymem) 的目标前历史压缩，可用于构建兼顾操作经验迁移与动态状态追踪的具身记忆层。
- **AgentTrainEvolve**：[ARLArena](#arlarena) 的序列级裁剪、时序优势估计和动态样本过滤可直接作为多轮工具调用强化学习的稳定训练基线。
- **Awesome-RSI**：[RSI 方法论梳理](#rsi) 提供了按优化、元学习、蒸馏和持续学习组织 RSI 文献的分类框架，也提示清单应单列长期退化与泛化验证。
- **EvolveLRM**：[DAPO 分析](#dapo) 表明应把策略熵轨迹和裁剪两侧的更新比例纳入 RL 后训练监控，以提前识别探索坍塌及后期无效更新。
- **ResearchEvolve**：[Claude 审稿实验](#claude) 与 [LLM 可靠性评测](#llm) 的冲突说明 AI 科研评审必须同时测试真实意见质量、植入缺陷召回率和跨模型一致性，不能仅以人类偏好判定替代能力。
- **InfraEvolve**：[Ember](#30b-ember) 的预测性部分加载与学习式调度提供了可由真实内存、时延反馈驱动自动迭代的端侧推理优化对象。
- **HumanEvolve**：[CoWriter](#cowriter-llm) 表明协作式写作 Agent 应优化用户观点表达、参与度和所有权，而非只追求成文速度与文本质量。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-25/  

