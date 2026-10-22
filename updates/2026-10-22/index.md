# 2026-10-22 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **长程 Agent 与递归自我改进成为主线**：[阶跃星辰开放 Step 5 Preview 权重，面向长程 Agent](#step-5-preview-agent)以百万 token 上下文、上下文压缩和可验证环境强化复杂任务执行，[RSIGame：自主试玩、修复与迭代的游戏开发智能体](#rsigame)则打通作品迭代与底层模型经验学习闭环。
- **系统与脚手架开始和模型协同演化**：[CoEvo-RSI：模型与测试框架协同演化](#coevo-rsi)直面 RSI 中模型与执行框架的“脑—身体”错配，[ScholarEvolve：从科研文献中持续演化 Agent Harness](#scholarevolve-agent-harness)展示了冻结模型参数、依靠文献检索和组合评估持续改进 Harness 的路径。
- **多智能体及工具化 Agent 向复杂生产任务扩展**：[微软发布 Agensh：千智能体自组织协作开发软件](#agensh)将无中心协作扩展至 1024 个软件开发智能体，[S-Agent 2.0：通用编程智能体驱动的空间推理](#s-agent-2-0)则以工具调用和持久化场景记忆构造空间证据闭环。
- **具身世界模型集中推进跨本体、四维表征与控制效率**：[Ropedia W0：利用人类经验扩展跨具身运动操作世界模型](#ropedia-w0)利用人类—机器人数据学习跨具身长程预测，[VPM：通过点轨迹预测学习四维世界](#vpm)联合建模视频与三维点轨迹，[VLA-Rolling：自适应复用动作尾部以加速具身控制](#vla-rolling)则通过动作缓存复用降低实时控制成本。
- **长度泛化与高效生成出现结构性进展**：[PAR：进度对齐循环机制提升状态跟踪长度泛化](#par)将状态跟踪外推到训练长度的 16 倍，[SWIFT：基于目标外推的自引导弱到强扩散模型](#swift)以冻结弱模型构造更强训练目标，[Matrix-Game 4.0：视频模型驱动的实时可玩游戏世界](#matrix-game-4-0)实现单卡 480p、60 FPS 可玩世界；热点延伸则关注 RSI、Agentic RL 与评测人才和合作需求。

## 对当前研究的启发
- **AgentTrainEvolve**：[RSIGame](#rsigame)把自主试玩、缺陷修复和验证经验回灌到底层模型，为从长程执行轨迹构造可验证训练闭环提供了直接范式。
- **TaskEvolve**：[RSIGame](#rsigame)验证了以可运行游戏为进化单位、由局部开发闭环和全局质量控制共同驱动持续迭代的可行性。
- **HarnessEvolve**：[CoEvo-RSI](#coevo-rsi)与[ScholarEvolve](#scholarevolve-agent-harness)分别给出模型—Harness 协同训练和冻结模型下 Harness 搜索两条路线，可用于比较联合演化与纯脚手架演化的收益边界。
- **ResearchEvolve**：[ScholarEvolve](#scholarevolve-agent-harness)将论文检索、算法实现、组合与实验评估闭环化，可直接作为自主科研系统持续吸收文献方法的设计参考。
- **SwarmEvolve**：[Agensh](#agensh)以共享代码仓库、通信系统和上下文看板支撑千级无中心协作，为研究通信拓扑、任务涌现和规模效应提供了可执行样板。
- **MemoryEvolve**：[S-Agent 2.0](#s-agent-2-0)通过持久化场景记忆维持三维证据闭环，提示长期记忆评测应关注证据状态能否在工具操作中持续更新而非仅看检索命中率。
- **RobotEvolve**：[Ropedia W0](#ropedia-w0)、[VPM](#vpm)与[VLA-Rolling](#vla-rolling)分别覆盖跨本体数据、动态世界表征和动作缓存复用，可组合为“世界模型预训练—跨本体迁移—低延迟控制”的技术链。
- **GeneralizeEvolve**：[PAR](#par)通过对齐循环进度实现 16 倍长度外推，为区分真正的算法性长度泛化与训练长度记忆提供了新的结构和实验基线。
- **SystemEvolve**：[CoEvo-RSI](#coevo-rsi)表明模型升级若不与执行框架共同选择、合并和训练会产生能力错配，应把 Harness 检查点纳入系统级演化状态。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-22/  

