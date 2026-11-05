# 2026-11-05 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从单点方法走向多层闭环：模型侧的 [801-30B：将 RSI 引入前沿预训练](#801-30b-rsi)、科研群体侧的 [SwarmRSI：共享失败经验驱动科研智能体群递归自我改进](#swarmrsi)，以及系统侧的 [VERSE：面向智能体 Harness 的可验证自进化优化器](#verse-harness) 和 [HarnessPro：兼顾性能与成本的智能体脚手架自进化框架](#harnesspro) 分别探索了记忆继承、失败复用与可验证改写。
- Agent 训练与环境工程进一步体系化：[ToolSpace：面向长程智能体的工具中心环境合成](#toolspace) 将真实 MCP 轨迹转化为可验证长程训练环境，[Axion 1.0：简化训练的开放智能体基础模型](#axion-1-0) 和 [Agentic-RL-Lab：成体系的 Agentic RL 中文教程](#agentic-rl-lab-agentic-rl) 则提供了开放配方与低算力复现路径。
- 新模型继续向原生多模态和长程执行演进，[腾讯发布混元Hy4：原生视觉与长程Agent能力升级](#hy4-agent) 把视觉理解、计算机操作、阶段性自检和执行验证纳入同一模型能力栈。
- Agent 评测开始直面真实规模与真实环境：[LoLBench：大型软件系统长程开发智能体评测](#lolbench) 在百万行级代码库中揭示仅 14% 的最佳完成率，[RoboColosseum：大规模真实场景物理智能评测框架](#robocolosseum) 则以分布式真机网络检验跨机器人和跨场景泛化。
- 效率与具身迁移出现互补进展：[Route Anything：通用人工智能系统的模型与策略路由](#route-anything) 统一优化模型及策略选择，[LoCo：基于本地偏好学习的推理压缩](#loco) 学习状态相关的思考早停，而 [DreamX：视频扩散模型驱动的通用潜在动作学习](#dreamx) 探索跨人类与机器人迁移的统一动作空间。
- 热点延伸集中在多模态表征与连续交互：FactEmbed 以因子化嵌入增强组合式图像检索，YANAMI 则用大规模多轮数据评测多模态状态持续更新能力。

## 对当前研究的启发
- **Awesome-RSI**：[801-30B](#801-30b-rsi) 与 [SwarmRSI](#swarmrsi) 分别给出参数训练闭环和群体经验继承两类 RSI 实例，可用于补充“改进对象、继承载体与闭环粒度”的分类框架。
- **EvolveLLM**：[801-30B](#801-30b-rsi) 的共享生产记忆与多个可闭合小循环，为研究基础模型如何把数据生产、训练和评估组织成持续自改进飞轮提供了直接案例。
- **AgentEvolve**：[VERSE](#verse-harness) 以失败归因、重放和因果扰动验证冻结权重后的 Harness 改动，为部署时自进化增加了防止伪提升与退化的审计机制。
- **HarnessEvolve**：[HarnessPro](#harnesspro) 的性能—成本帕累托搜索与 [VERSE](#verse-harness) 的因果验证可以组合成“候选改写—测试合成—成本筛选—可信验收”的 Harness 演化管线。
- **AgentTrainEvolve**：[ToolSpace](#toolspace) 的可验证跨工具任务与 [Axion 1.0](#axion-1-0) 的精简 SFT/RL 配方，为低成本验证长程工具调用训练闭环提供了可复用起点。
- **EnvironmentEvolve**：[ToolSpace](#toolspace) 展示了从真实 MCP 执行轨迹抽取工具组合、任务与验证器的方法，可直接用于构建随 Agent 能力扩展的工具环境生产线。
- **ResearchEvolve**：[SwarmRSI](#swarmrsi) 将假设、程序、证据和失败记录组织为跨代共享研究图谱，为科研智能体避免重复试错并重组历史发现提供了具体记忆结构。
- **EvalEvolve**：[LoLBench](#lolbench) 与 [RoboColosseum](#robocolosseum) 表明下一阶段动态评测应保留真实系统规模、回归验证和跨实体泛化，而不能仅依赖短任务或静态模拟基准。
- **Groom**：[LoLBench](#lolbench) 的百万行级长轨迹任务和 [HarnessPro](#harnesspro) 的成本目标可分别作为过程级 token 归因的任务载体与性能—成本对照基线。
- **RobotEvolve**：[DreamX](#dreamx) 的跨本体潜在动作空间配合 [RoboColosseum](#robocolosseum) 的真机泛化评测，为验证动作表征能否迁移到不同机器人提供了完整实验路径。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-05/  

