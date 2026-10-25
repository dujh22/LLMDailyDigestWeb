# 2026-10-25 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **推理时自进化从反思走向可迁移技能**：[RoboSkill：具身智能体的技能积累与复用框架](#roboskill)将触觉反馈与文字、代码技能库结合，实现跨任务、跨模型经验复用；[Reflexion 的语言反馈与记忆机制](#rsi-reflexion)与 [RSI，正在重走深度学习的老路](#rsi)则分别提供经典闭环和方法论全景。
- **智能体强化学习聚焦训练稳定性与探索退化**：[ARLArena：稳定智能体强化学习统一框架](#arlarena)以统一平台和 SAMPO 改善多轮训练的稳定性、可复现性，[大模型强化学习中的熵坍塌](#dapo)则从机制层解释探索过早消失及 DAPO 的应对方式。
- **记忆机制深入长程适应与具身操作**：[METTA：面向元强化学习的记忆增强测试时适应](#metta)以因果记忆和回合摘要支持未见任务适应，[WholeBodyMem：面向人形机器人操作的目标前历史记忆](#wholebodymem)通过对象追踪和事件关键帧解决动态、部分可观测操作。
- **AI 同行评审出现值得警惕的相反结论**：[哈佛研究：Claude审稿质量全面超越资深人类专家](#claude)报告模型在受控对照中胜过专家，而[顶刊已发表论文的 LLM 同行评审可靠性评测](#llm)发现模型意见不一致且缺陷检出率低，表明结论高度依赖任务设计与评价标准。
- **模型与系统落地继续向端侧和垂直科学扩展**：[Ember 推理引擎探索自进化](#30b-ember)尝试以预测加载和学习式调度承载手机端 30B 模型，[Carbon-X](#hugging-face-dna-carbon-x)则将 DNA 与自然语言统一建模；热点延伸中的 [VAST](#vast)关注离线强化学习长程信用分配，但与当前主线关联较弱。

## 对当前研究的启发
- **AgentEvolve**：[RoboSkill](#roboskill)表明技能库可同时保存文字、代码与执行反馈，[Reflexion](#rsi-reflexion)则给出了失败反思写回记忆的基础闭环，可共同用于设计“反思生成技能、反馈持续修订”的部署后进化机制。
- **MemoryEvolve**：[METTA](#metta)的因果神经记忆与回合级摘要提供了双时间尺度组织方案，[WholeBodyMem](#wholebodymem)的事件驱动关键帧则可用于研究固定预算下按任务事件写入和淘汰记忆。
- **RobotEvolve**：[RoboSkill](#roboskill)与 [WholeBodyMem](#wholebodymem)分别覆盖跨任务技能沉淀和目标对象历史追踪，可组合为机器人“状态记忆—技能检索—执行反馈—技能更新”闭环。
- **AgentTrainEvolve**：[ARLArena](#arlarena)的序列级裁剪、时序优势估计和动态过滤可直接作为多轮 Agentic RL 稳定训练与统一复现实验的候选基线。
- **EvolveLRM**：[熵坍塌与 DAPO 对策](#dapo)提示应把策略熵轨迹、裁剪方向和低概率 token 更新纳入 RL 后训练监控，以区分早期探索崩溃与后期优化失效。
- **ResearchEvolve**：[Claude 审稿对照实验](#claude)与 [LLM 同行评审可靠性评测](#llm)的矛盾结果说明自动科研评审必须分开测量意见质量、事实错误、一致性和植入缺陷召回率，而不能用单一总体评分判断可替代性。
- **HumanEvolve**：[CoWriter](#cowriter-llm)通过主动提问和专家共创流程提升用户参与、文档所有权与表达质量，为避免写作辅助造成判断外包和去技能化提供了具体交互范式。
- **InfraEvolve**：[Ember](#30b-ember)将预测性部分加载与学习式调度结合，提示可把端侧内存峰值、时延和命中率作为机器可验证反馈，构建持续积累硬件调优经验的推理系统进化闭环。
- **Awesome-RSI**：[RSI 方法论综述](#rsi)将优化、反向传播、元学习、蒸馏和持续学习映射到递归自我改进，可作为资源清单重构分类体系及补充稳定性、泛化与遗忘维度的依据。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-25/  

