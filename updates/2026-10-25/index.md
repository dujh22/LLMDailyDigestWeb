# 2026-10-25 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **推理时经验积累与复用成为主线（2 条）**：[RoboSkill：具身智能体的技能积累与复用框架](#roboskill)将触觉反馈、文字经验与代码技能结合，[RSI 代表论文解读：Reflexion 的语言反馈与记忆机制](#rsi-reflexion)则以“执行—评估—反思—记忆更新”闭环展示冻结参数下的持续改进。
- **RSI 方法论进一步体系化**：[RSI，正在重走深度学习的老路](#rsi)将递归自我改进与优化、反向传播、强化学习、元学习及持续学习逐一对应，为分析 RSI 的更新机制、泛化与退化风险提供统一视角。
- **强化学习关注训练稳定性与长程信用分配**：[大模型强化学习中的熵坍塌：机制、推导与 DAPO 对策](#dapo)解析熵坍塌及非对称裁剪对策；热点延伸 [VAST：自适应时间尺度的离线价值缝合](#vast)则通过联合选择子目标和时间跨度改善多阶段决策。

## 对当前研究的启发
- **AgentEvolve**：[RoboSkill](#roboskill)与 [Reflexion](#rsi-reflexion)共同表明，可将成功轨迹代码化为技能、失败轨迹语言化为反思，并由执行反馈统一驱动技能库和工作流记忆更新。
- **MemoryEvolve**：[RoboSkill](#roboskill)提供了把多模态反馈沉淀为可复用技能记忆的具身案例，而 [Reflexion](#rsi-reflexion)可作为失败经验写入与检索策略的基础闭环。
- **RobotEvolve**：[RoboSkill](#roboskill)说明触觉反馈不仅能用于即时控制，还可作为技能更新和跨任务复用的经验信号，从而降低真实机器人探索成本。
- **Awesome-RSI**：[RSI，正在重走深度学习的老路](#rsi)给出了组织 RSI 文献的新框架，可按优化、元学习、蒸馏、正则化和持续学习机制重构资源分类并补充稳定性问题。
- **EvolveLRM**：[DAPO 熵坍塌分析](#dapo)提示应把训练早期探索保持与后期有效更新分开诊断，并将熵曲线及裁剪两侧的梯度贡献纳入 RL 后训练监控。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-25/  

