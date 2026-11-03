# 2026-11-03 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进出现两条关键路线：[Astra 直接编程神经网络权重](#astra-qwen)探索绕过梯度下降的权重空间读写与修复，[R²Orch](#r-orch)则通过自博弈、任务选择和技能内化持续改进智能体编排器。
- Agent 的持续学习与经验复用进一步系统化：[Meta Routed CL](#meta-routed-cl)以任务聚类和路由记忆提升奖励并显著降低 API 成本，[Trajectory2Gym](#trajectory2gym)通过决策接地的合成交互补强有状态多轮工具任务。
- 具身智能开始强化实时运行时与低延迟控制：[REA](#rea)采用异步“脑—小脑”架构协调慢推理与快速策略，[OSWAM](#oswam)则把世界动作模型压缩到单步扩散，实现约 3 倍加速。
- 数据、评测与持续学习基础环节同步推进：[BHI](#bhi-158-llm)审计 158 个基准的区分度、抗饱和度与影响力，[SimpleLoRIF](#simplelorif)用梯度归因定位导致安全退化的数据，[CaRE](#care-300)将类增量持续学习扩展到 300 余项任务。
- 新模型与热点延伸覆盖统一语音推理、连续潜空间推理、可控游戏世界及视觉生成/跟踪；另有 GPT-6.2 Astra 与 Claude 5.5 的非官方爆料，规格仍待确认。

## 对当前研究的启发
- **Awesome-RSI**：[Astra 权重空间编程](#astra-qwen)把“自我修改”推进到直接读取和重写模型参数，而 [R²Orch](#r-orch)提供了可迭代验证的系统级自博弈闭环，可分别作为激进与渐进 RSI 路线的代表案例。
- **AgentTrainEvolve**：[R²Orch](#r-orch)的自动选题—自博弈—失败内化闭环与 [Trajectory2Gym](#trajectory2gym)的跨步依赖交互合成，可组合成从课程生成到参数更新的工具智能体训练管线。
- **AgentEvolve**：[Meta Routed CL](#meta-routed-cl)表明按任务隔离并路由历史经验能同时改善效果与成本，可用于设计部署期技能库的聚类、检索和复用策略。
- **MemoryEvolve**：[Meta Routed CL](#meta-routed-cl)将任务聚类、记忆路由和经验隔离绑定起来，为抑制长期记忆干扰及量化记忆系统成本收益提供了直接架构参考。
- **JevEvolve**：[REA](#rea)的边界触发判断门与共享预算升级机制，为学习“快策略直接执行还是升级至慢推理”的动态路由边界提供了具身场景原型。
- **DataEvolve**：[SimpleLoRIF](#simplelorif)说明可沿梯度把行为退化追溯到具体训练样本，可将数据筛选从启发式质量打分升级为面向目标行为的因果式归因。
- **EvalEvolve**：[BHI](#bhi-158-llm)的区分度、抗饱和度和影响力三维健康指数，可作为动态决定基准保留、更新或淘汰的元评测信号。
- **EvolveLRM**：[LARC](#larc)用信息增益强化学习将显式思维链迁移到连续隐藏状态，为研究潜在推理的测试时扩展能力及其可验证性提供了新对象。
- **RobotEvolve**：[REA](#rea)与 [OSWAM](#oswam)分别从异步运行时和单步动作生成压缩控制延迟，可共同支撑机器人“慢规划—快执行”的实时闭环。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-03/  

