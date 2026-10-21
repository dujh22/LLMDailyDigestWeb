# 2026-10-21 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **固定预算长上下文取得显著进展**：[EdgeRock-4B：固定内存长推理，KV Cache削减99.1%](#edgerock-4b-kv-cache-99-1)以记忆岩锚维持固定容量状态，在 256K 上下文下大幅压缩 KV Cache，并显著提升单卡吞吐。
- **具身自进化形成“部署—训练—群体经验”多线推进**（5 条）：[LoopWAM开源并登顶RoboChallenge Table30](#loopwam-robochallenge-table30)探索部署阶段自进化，[RLinf v0.4 发布：具身强化学习迈向真实物理世界](#rlinf-v0-4)打通真机后训练，而[从车队经验中学习：机器人集体学习范式](#item-15)利用跨机器人成功轨迹与失败上下文持续改进统一策略。
- **Agent 的策略、脚手架与训练环境开始协同演化**：[Self-HPO：框架与策略协同优化的自进化编码智能体](#self-hpo)交替优化交互框架和策略模型，[CoworkEnv：为长时程协作智能体合成可执行训练环境](#coworkenv)则自动构造可执行、可验证且兼容 SFT/RL 的长程环境。
- **生产级 Harness 更重视持久化、恢复与多模态证据管理**：[Pi 1.0 发布 Pi Durable，引入原生 MCP 与 Code Mode](#pi-1-0-pi-durable-mcp-code-mode)提供任务恢复与安全重放，[OpenVLHarness：以多模态记忆增强真实世界视觉智能体工具使用](#openvlharness)通过持久记忆和证据渲染提升工具使用效果并降低成本。
- **真实世界能力的构建与评测进一步端到端化**：[OR-License：现实世界运筹学智能体评测基准](#or-license)以客户模拟和隐藏验证评估专业任务交付，[Holi-World：从人类第一人称经验构建整体世界智能](#holi-world)则整合数据采集、世界表征、训练与独立评测。
- **热点延伸覆盖多模态与轻量化**：低相关性条目集中在脑编码 PEFT、第一人称三维重建、谱空间嵌入压缩和多轮图像编辑；模型发布侧，[MiniMax发布M3.1 Flash，智能体任务成本降低70%](#minimax-m3-1-flash-70)继续强化低成本高频 Agent 路线。

## 对当前研究的启发
- **CacheEvolve**：[EdgeRock-4B](#edgerock-4b-kv-cache-99-1)表明可将长历史压缩为固定容量状态，值得重点分析其锚点选择、状态更新及质量—显存权衡能否转化为可学习的缓存淘汰机制。
- **RobotEvolve**：[LoopWAM](#loopwam-robochallenge-table30)、[RLinf v0.4](#rlinf-v0-4)与[机器人集体学习](#item-15)共同提供了从单机部署反馈、真机后训练到车队经验回灌的完整具身进化闭环。
- **AgentTrainEvolve**：[CoworkEnv](#coworkenv)的可验证环境合成与[RLinf v0.4](#rlinf-v0-4)的全模态真机训练接口，可分别补足长程 Agentic RL 的环境供给和现实交互基础设施。
- **EnvironmentEvolve**：[CoworkEnv](#coworkenv)将工作流约束、程序化验证和反馈修复结合起来，为“环境生成后自动验收并自纠错”提供了直接可复用的实现范式。
- **CodeEvolve**：[Self-HPO](#self-hpo)把编码 Agent 的交互框架与策略模型同时纳入优化，可作为“Agent 修改自身脚手架并用执行结果验证”的训练侧闭环参考。
- **Awesome-RSI**：[Self-HPO](#self-hpo)对框架和策略进行交替递归优化，为研究改进机制自身是否能够持续提升、以及失败模式是否随迭代迁移提供了具体案例。
- **HarnessEvolve**：[Pi Durable](#pi-1-0-pi-durable-mcp-code-mode)的安全重放与[OpenVLHarness](#openvlharness)的证据渲染、持久记忆，提示 Harness 评测应显式覆盖恢复能力、证据可审计性和状态管理成本。
- **MemoryEvolve**：[OpenVLHarness](#openvlharness)展示了将工具所得多模态证据持久化并跨步骤组合的路径，可用于设计面向真实任务的记忆写入、复用和成本评测。
- **EvalEvolve**：[OR-License](#or-license)以真实项目材料、动态客户模拟器和隐藏验证替代静态问答，为抗污染且面向最终交付质量的 Agent 评测提供了模板。
- **SwarmEvolve**：[机器人集体学习范式](#item-15)将车队成功轨迹共享与失败上下文利用结合起来，可用于研究群体经验如何筛选、传播并稳定提升统一策略。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-21/  

