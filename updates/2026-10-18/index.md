# 2026-10-18 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进成为今日主线：从可执行世界模型驱动的 [Memento 3](#memento-3)、跨代码/GUI/科研任务的 [RSI-Anything](#rsi-anything)，扩展到冻结权重后递归优化外壳的 [Google Harness²](#google-harness-agent) 与权重—脚手架协同演化的 [Evo²](#evo)，改进对象正由单一提示或记忆走向完整系统。
- 具身自进化集中验证“经验沉淀—技能修订—跨任务泛化”闭环：[Recursia](#recursia) 与 [RoboFoundry](#robofoundry) 分别演化共享技能栈和整套执行系统，[EmbodiedCLBench](#embodiedclbench) 则开始系统衡量持续学习与组合泛化。
- 长程 Agent 训练同步推进环境、奖励与基础设施：[Tev](#tev) 提供可验证的密集进度奖励，[QwenGyre](#qwengyre-agent) 显著压缩超长轨迹 RL 时间；与此同时，[智能体强化学习自蒸馏方法的现实检验](#item-98) 发现十种方法均未稳定超越 GRPO，提示额外自蒸馏计算不等于有效进化。
- 自主科研从系统设计进一步转向真实长周期评测：[DeepRSI](#deeprsi-48-kimi-k3) 暴露验证器过拟合和奖励投机，[ASI-Bench](#asi-bench-ai) 指出方法提示落地为完整研究流程仍是瓶颈，[Fork-and-Flush](#fork-and-flush) 则以刷新上下文和并行分叉改善长程探索。
- 记忆与长程可靠性开始强调“可修订”而非只追加：[ReHarness](#reharness) 利用在线反馈后向校正历史经验，并与显式信念校验、按情境激活经验等工作共同指向动态维护的可执行记忆。
- 热点延伸主要覆盖多模态空间推理、视频与三维生成、模型架构及推理加速；这些方向当日热度较高，但与团队核心自进化研究的直接关联有限。

## 对当前研究的启发
- **Awesome-RSI**：Memento 3 与 RSI-Anything 表明，可执行世界模型、真实反馈和兼容性检查可以构成跨领域 RSI 的统一闭环，而 DeepRSI 的奖励投机结果说明验收机制必须与改进器隔离。
- **SystemEvolve**：Google Harness² 与 Evo² 可直接参考为“双层递归搜索+权重/脚手架协同优化”方案，并应把跨任务、跨模型迁移作为系统改进是否真实的核心验收项。
- **HarnessEvolve**：Harness²、Evo² 和 ReHarness 共同提示，Harness 的提示、工具、记忆与代码应模块化版本管理，并通过独立验证决定修订的保留、回滚和迁移。
- **RobotEvolve**：Recursia 与 RoboFoundry 给出了冻结基座模型、持续修订技能和执行接口的两种具身进化路径，EmbodiedCLBench 可用于检验所得能力是否能重组到未见高级任务。
- **AgentTrainEvolve**：Tev 的密集进度势能奖励和 QwenGyre 的分支轨迹训练可分别缓解长程信用分配与吞吐瓶颈，而十种自蒸馏方法的负结果要求新增训练机制必须对 GRPO 做严格等算力比较。
- **ResearchEvolve**：DeepRSI 与 ASI-Bench 显示科研智能体评测应同时覆盖长时持续优化、隐蔽测试和完整流程操作化，Fork-and-Flush 则提供了避免长对话惯性并保持实验资产的搜索策略。
- **MemoryEvolve**：ReHarness 的后向修订机制说明记忆系统不应只做增量写入，而应利用新任务反馈追溯校正旧经验并保留可审计的版本关系。
- **SwarmEvolve**：MASS 将协作轨迹回灌共享模型、FlowMAS 自动搜索通信拓扑，提示可把“群体结构搜索”和“群体经验参数化”组合成双层演化闭环。
- **EvalEvolve**：DeepRSI 暴露的公开验证器过拟合与 ASI-Bench 的分级指导设计，为构建抗奖励投机、可区分自主程度的动态长周期评测提供了直接依据。
- **GeneralizeEvolve**：Recursia 的零样本长程迁移与 EmbodiedCLBench 的技能重组评测可形成“实际迁移结果+组合泛化基准”的双重证据，避免把场景内熟练误判为自进化。
- **JevEvolve**：Jeva 的决策原生结构与 StartLux-Decision 的置信度引导 AutoThink 可结合，用于学习高频动作直接决策与升级慢思考之间的动态路由边界。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-18/  

