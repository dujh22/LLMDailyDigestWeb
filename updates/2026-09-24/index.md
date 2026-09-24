# 2026-09-24 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从概念分层走向多路径实现：综述提出 [RSI 五级自主性分层架构](#79-rsi)，[SwarmWorld 与 ModularRSI](#swarmworld-modularrsi-ai) 分别验证群体协作与脚手架演化路径，[Mint Recursive](#mind-lab-mint-recursive) 则将闭环落到企业模型后训练。
- 智能体闭环开始连接组织知识与真实物理环境：[Meta“组织第二大脑”智能体](#meta) 以结构化知识、自动评估和专家反馈实现免重训改进，[Simate Physical RSI](#simate-physical-rsi-robodojo) 则闭合假设、真机实验与评测反馈并登顶 RoboDojo。
- Jev 式 System 1 快决策形成完整应用栈（4 项）：从 [Jev 与 Decitron 的范式对比](#jev-vs-decitron-ai)、开源端侧模型 [Laya](#jev-laya-hugging-face)，延伸到置信度级联的 [JEV-as-a-Judge](#jev-as-a-judge) 和记忆控制架构 [Jev-Mem](#jev-mem-system-one)。
- 智能体与生成模型评测进一步细化到过程决策和实例级奖励：[Taste-Bench](#the-tasteful-agent) 自动构造长时程轨迹决策分叉，[RULER](#ruler-svg) 则把实例感知多维量规转化为 SVG 强化学习奖励。
- 模型底层能力同步推进：[Ovis-Embedding](#ovis-embedding) 统一全模态表征，[HyperQ](#hyperq) 探索量子残差适配，[Flash-dLLM](#flash-dllm-io-kv) 与 [StableVQ](#stablevq) 分别改善扩散语言模型推理效率和视觉分词器训练稳定性。

## 对当前研究的启发
- **Awesome-RSI**：[RSI 五级自主性分层架构](#79-rsi) 可作为资源库统一标注自主性和改进环路的主轴，并用 [SwarmWorld 与 ModularRSI](#swarmworld-modularrsi-ai) 补充群体、脚手架两类实现案例。
- **MemoryEvolve**：[Meta“组织第二大脑”智能体](#meta) 展示了“结构化外部记忆—自动评估—专家纠偏”的可审计演化闭环，而 [Jev-Mem](#jev-mem-system-one) 提供了用快模型学习记忆写入、关联、路由和停止策略的低成本架构。
- **ResearchEvolve**：[Simate Physical RSI](#simate-physical-rsi-robodojo) 表明自主科研闭环可扩展至真机实验，值得重点研究人机共驾下假设生成、执行验证和真实数据回流的接口设计。
- **JevEvolve**：[JEV-as-a-Judge](#jev-as-a-judge) 的高置信接受、低置信升级机制可直接用于学习快慢模型路由边界，[Laya](#jev-laya-hugging-face) 与 [Jev-Mem](#jev-mem-system-one) 则分别验证端侧部署和高频记忆控制场景。
- **EvalEvolve**：[Tasteful Agent](#the-tasteful-agent) 的轨迹决策分叉自动出题方法，为构建随真实工程与科研轨迹持续更新、且关注长程决策质量的动态评测提供了具体方案。
- **SwarmEvolve**：[SwarmWorld 与 ModularRSI](#swarmworld-modularrsi-ai) 中共享环境驱动的群体经验学习，可用于研究协作结构、知识传播与群体改进信号是否真正超越单体自迭代。
- **HarnessEvolve**：[ModularRSI](#swarmworld-modularrsi-ai) 将执行框架本身纳入演化对象，提示应把工具接口、模块组合和验证流程作为可搜索、可比较的 harness 配置。
- **EvolveLRM**：[Mint Recursive](#mind-lab-mint-recursive) 将评测、数据、LoRA 后训练、部署和生产反馈串成低成本循环，可作为持续 RL 后训练平台化与防退化监控的工程参照。
- **Groom**：[Taste-Bench](#the-tasteful-agent) 的轨迹分叉与结果感知教师机制可用于定位关键决策 token，并区分有效规划投入与冗余搜索消耗。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-24/  

