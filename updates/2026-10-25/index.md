# 2026-10-25 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **推理时经验积累与复用**：两项工作聚焦无需频繁改参的持续改进，[RoboSkill：具身智能体的技能积累与复用框架](#roboskill)将触觉反馈、文字与代码技能库结合，[RSI 代表论文解读：Reflexion 的语言反馈与记忆机制](#rsi-reflexion)则以语言反思写回记忆，形成“执行—评估—改进”闭环。
- **RSI 方法论梳理**：[RSI，正在重走深度学习的老路](#rsi)将递归自我改进与优化、反向传播、元学习、蒸馏及持续学习等成熟机制对应起来，为构建统一的 RSI 技术谱系提供视角。
- **强化学习稳定性与长程决策**：[大模型强化学习中的熵坍塌：机制、推导与 DAPO 对策](#dapo)解析熵坍塌及非对称裁剪对策；热点延伸 [VAST：自适应时间尺度的离线价值缝合](#vast)则通过联合选择子目标与时间跨度改善长程信用分配。

## 对当前研究的启发
- **AgentEvolve**：[RoboSkill：具身智能体的技能积累与复用框架](#roboskill)与 [RSI 代表论文解读：Reflexion 的语言反馈与记忆机制](#rsi-reflexion)表明，可将成功技能代码化、失败经验语言化，并统一纳入部署期可持续更新的经验闭环。
- **MemoryEvolve**：[RoboSkill：具身智能体的技能积累与复用框架](#roboskill)提供了从多模态执行反馈抽取技能记忆并持续更新的具身案例，而 Reflexion 可作为失败记忆写入与检索的基线机制。
- **RobotEvolve**：[RoboSkill：具身智能体的技能积累与复用框架](#roboskill)说明触觉反馈可参与技能抽取和复用，有望减少机器人面对新任务时的真实环境探索成本。
- **Awesome-RSI**：[RSI，正在重走深度学习的老路](#rsi)可用于按优化、元学习、蒸馏与持续学习重构 RSI 资源分类，而 Reflexion 则提供了参数冻结型 RSI 的代表闭环。
- **EvolveLRM**：[大模型强化学习中的熵坍塌：机制、推导与 DAPO 对策](#dapo)提示应把训练熵轨迹与裁剪两侧的更新比例纳入诊断，以区分探索过早消失和后期有效梯度不足。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-25/  

