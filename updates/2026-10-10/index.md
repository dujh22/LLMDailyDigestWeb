# 2026-10-10 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进走向可落地闭环**：2 条工作分别从企业 Agent 与人机协同科研切入，[RSI早期产业形态或率先落地企业Agent](#rsi-agent)提出 Reward—Verifier—后训练—安全发布闭环，[Novix 跑通协同进化式 RSI 规模化闭环](#novix-rsi)则展示 AI 探索、专家反馈与能力回流的规模化路径。
- **训练环境从人工搭建转向轨迹生成与持续演化**：[Trace2Env：从交互轨迹构建智能体语言世界模型](#trace2env)可直接把历史轨迹转化为持久状态环境，[AgentGarten：面向持续进化智能体的代码世界](#agentgarten)进一步支持经验继承和少轮交互下的能力迭代。
- **世界模型的数据与奖励闭环向动作忠实性推进**：[DreamTrue：反事实后训练实现动作忠实的机器人世界模型](#dreamtrue)结合几何校准、反事实轨迹扩展和具身视频奖励，改善跨本体预测的物理合理性。
- **智能体评测开始关注经验的获取、保留与迁移**：[Learn2Play Bench：评测智能体在陌生环境中的经验学习能力](#learn2play-bench)以规则新颖或反直觉的交互任务，检验脚手架与记忆机制能否形成可迁移经验。
- **热点延伸集中在具身与视觉生成、推理系统优化及应用工具**：包括多智能体第一人称世界模型、零微调导航、机器人情境学习、Token 级模型路由、动态 3D 影像与 AI 模拟面试等，但与当前核心研究方向关联较弱。

## 对当前研究的启发
- **Awesome-RSI**：[RSI早期产业形态或率先落地企业Agent](#rsi-agent)给出了可验证企业任务承载 RSI 的工程闭环，而 [Novix 跑通协同进化式 RSI 规模化闭环](#novix-rsi)补充了专家反馈和能力回流的规模化机制。
- **ResearchEvolve**：[Novix 跑通协同进化式 RSI 规模化闭环](#novix-rsi)表明可将专家持续反馈嵌入自主探索与复杂科学工程执行，使科研智能体的成果直接回流为下一轮系统能力。
- **EnvironmentEvolve**：[Trace2Env：从交互轨迹构建智能体语言世界模型](#trace2env)提供了无需复刻原系统的环境生成路线，[AgentGarten：面向持续进化智能体的代码世界](#agentgarten)则可作为支持经验继承与环境—智能体协同演化的可扩展载体。
- **DataEvolve**：[DreamTrue：反事实后训练实现动作忠实的机器人世界模型](#dreamtrue)展示了以反事实轨迹扩充训练分布、再用具身视频奖励筛选优化合成数据的具体数据飞轮。
- **EvalEvolve**：[Learn2Play Bench：评测智能体在陌生环境中的经验学习能力](#learn2play-bench)可借鉴其反直觉规则和重复交互设计，构造难以靠静态记忆或模式匹配取巧的动态评测。
- **MemoryEvolve**：[Learn2Play Bench：评测智能体在陌生环境中的经验学习能力](#learn2play-bench)把经验获取、跨轮保留与跨任务迁移拆成可观测能力，为长期记忆写入和复用策略提供了直接评测框架。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-10/  

