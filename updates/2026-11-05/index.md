# 2026-11-05 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进形成“模型—环境—群体”三层实践：[801-30B](#801-30b-rsi) 将共享生产记忆和闭合小循环引入前沿预训练，[RSIGym](#rsigym) 提供预算约束、可复现的训练环境，[SwarmRSI](#swarmrsi) 则探索科研智能体群跨代继承成功与失败经验。
- Agent Harness 自进化转向可验证、成本敏感的工程闭环：[HarnessPro](#harnesspro) 以轨迹诊断、测试合成和帕累托优化兼顾通过率与成本，[VERSE](#verse-harness) 用重放、因果扰动和审计验证每次改动，[LoLBench](#lolbench) 则显示大型软件系统中的最佳完成率仍仅为 14%。
- 长程 Agent 的模型与训练条件同步升级：[ToolSpace](#toolspace) 从真实 MCP 轨迹合成可验证的跨工具环境，[Axion 1.0](#axion-1-0) 开放精简的 SFT+RL 训练配方，[混元Hy4](#hy4-agent) 则以原生视觉、计算机操作和阶段性自检强化长程交付。
- 系统效率优化覆盖路由与推理预算：[Route Anything](#route-anything) 统一模型和策略路由并报告平均 8.82 倍效率增益，[LoCo](#loco) 通过本地偏好学习让模型按状态决定何时停止思考。
- 具身智能同时推进动作表征与真实评测：[DreamX](#dreamx) 从视频扩散模型中学习可跨人类、机器人和环境迁移的潜在动作空间，[RoboColosseum](#robocolosseum) 以分布式真机网络检验 VLA 的跨本体泛化。
- 热点延伸集中于组合式图像检索、多轮多模态状态追踪、心理治疗模拟及长篇视频编辑，代表工作包括 [FactEmbed](#factembed-mllm)、[YANAMI](#yanami)、[Pandora](#pandora) 与 [MoviEdit](#moviedit)。

## 对当前研究的启发
- **Awesome-RSI**：[801-30B](#801-30b-rsi)、[RSIGym](#rsigym) 与 [SwarmRSI](#swarmrsi) 分别补齐模型更新、实验基础设施和跨代经验继承，可据此整理一套 RSI 闭环的分层分类框架。
- **AgentEvolve**：[VERSE](#verse-harness) 的失败归因、执行重放与因果扰动，为冻结权重 Agent 判断“某次自改是否真实有效”提供了可直接复用的验证流程。
- **HarnessEvolve**：[HarnessPro](#harnesspro) 将通过率与执行成本纳入帕累托优化，而 [LoLBench](#lolbench) 提供超大型代码库压力测试，可组合成面向真实软件工程的 Harness 演化基线。
- **Groom**：[HarnessPro](#harnesspro) 的性能—成本双目标和 [VERSE](#verse-harness) 的轨迹审计，可用于把 token 利用评测进一步落到具体失败环节及 Harness 改动收益归因。
- **AgentTrainEvolve**：[ToolSpace](#toolspace) 展示了由真实 MCP 执行轨迹生成长程任务并以可验证反馈开展 RL 的完整数据—环境—训练链路。
- **EnvironmentEvolve**：[ToolSpace](#toolspace) 的工具组合环境合成与 [RSIGym](#rsigym) 的 Everything-as-a-Service 架构，为可执行、可验证且受预算约束的环境工厂提供了两种互补实现。
- **EvolveLLM**：[801-30B](#801-30b-rsi) 将共享生产记忆和多个可闭合小循环用于基座预训练，为研究自生成数据如何跨训练轮次沉淀和复用提供了前沿案例。
- **EvalEvolve**：[LoLBench](#lolbench) 与 [RoboColosseum](#robocolosseum) 分别把评测推进到百万行真实代码库和分布式真机网络，说明动态评测应优先扩展真实环境覆盖而非继续堆叠静态题目。
- **JevEvolve**：[Route Anything](#route-anything) 的全模态轨迹矩阵可用于学习快模型与慢模型之间的动态升级边界，并以质量—时延—成本联合指标持续校准路由器。
- **EvolveLRM**：[LoCo](#loco) 从自生成轨迹构造状态条件偏好对，为学习式推理早停提供了无需固定 token 阈值的训练方案。
- **RobotEvolve**：[DreamX](#dreamx) 的跨本体潜在动作空间可作为数据共享层，[RoboColosseum](#robocolosseum) 则可充当其 sim-to-real 与跨机器人迁移的真实验证设施。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-05/  

