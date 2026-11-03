# 2026-11-03 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从“优化输出”推进到“改写模型与系统”： [Astra 直接编程神经网络权重](#astra-qwen)探索无需梯度下降的权重空间编程，[R²Orch](#r-orch)则以自博弈和技能内化形成智能体编排器的参数化改进闭环。
- 智能体持续学习聚焦经验组织与训练数据构造：[Meta Routed CL](#meta-routed-cl)以任务路由和隔离记忆兼顾收益、遗忘与成本，[Trajectory2Gym](#trajectory2gym)合成跨步依赖的决策接地交互，[CaRE](#care-300)则将类增量学习扩展至300多个任务。
- 具身智能加速融合快慢控制与世界模型：[REA](#rea)用异步脑—小脑架构协调高层推理和快速策略，[OSWAM](#oswam)将动作生成压缩至单步扩散，[HiFOR](#hifor)通过分层未来预测为机器人动作提供针对性前瞻。
- 评测与数据治理开始面向长期有效性：[BHI](#bhi-158-llm)系统审计158个基准的区分度、抗饱和度与影响力，[SimpleLoRIF](#simplelorif)则用梯度归因追溯导致安全退化的微调样本。
- 新模型方向出现语音工具调用与连续潜空间推理等进展；热点延伸还包括尚待官方确认的GPT-6.2 Astra/Claude 5.5爆料、视频先验图像生成和稠密三维跟踪。

## 对当前研究的启发
- **Awesome-RSI**：[Astra 权重空间编程](#astra-qwen)与[R²Orch](#r-orch)分别把递归改进对象推进到模型权重和智能体编排器，可作为“改进机制自身被改进”的两类关键案例。
- **AgentTrainEvolve**：[R²Orch](#r-orch)的双层自博弈课程与[Trajectory2Gym](#trajectory2gym)的跨步决策接地合成，可组合成“自动选题—生成长程交互—失败内化”的训练闭环。
- **AgentEvolve**：[Meta Routed CL](#meta-routed-cl)表明按任务聚类、路由并隔离经验能够同时提升复用收益和降低调用成本，为冻结参数下的技能与工作流记忆管理提供直接设计依据。
- **DataEvolve**：[Trajectory2Gym](#trajectory2gym)将数据分配落实到逐决策接地认证，而[SimpleLoRIF](#simplelorif)可反向定位有害样本，两者共同支持“合成—归因—过滤”的数据飞轮。
- **EvalEvolve**：[BHI](#bhi-158-llm)提供了区分度、抗饱和度和影响力三维健康指标，可用于决定哪些静态基准应更新、降权或退出进化式评测集合。
- **GeneralizeEvolve**：[CaRE](#care-300)和[Meta Routed CL](#meta-routed-cl)分别从专家路由与经验隔离切入大规模持续学习，可用于研究跨任务扩展时如何控制灾难性遗忘。
- **JevEvolve**：[REA](#rea)的边界触发判断门与共享预算升级机制，为学习“何时走快速策略、何时升级基础模型慢思考”的动态路由边界提供了具身实现。
- **RobotEvolve**：[OSWAM](#oswam)的单步实时动作生成与[HiFOR](#hifor)的分层未来预测形成互补，可用于兼顾机器人闭环控制的低延迟和长时规划能力。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-03/  

