# 2026-10-21 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **长上下文与智能体运行效率**：[EdgeRock-4B：固定内存长推理，KV Cache削减99.1%](#edgerock-4b-kv-cache-99-1)以固定容量状态支撑 256K 上下文，[MiniMax发布M3.1 Flash，智能体任务成本降低70%](#minimax-m3-1-flash-70)则从模型侧降低高频 Agent 工作流成本。
- **Agent 系统与训练环境协同自进化**：[Self-HPO：框架与策略协同优化的自进化编码智能体](#self-hpo)将脚手架和策略同时纳入递归优化，[CoworkEnv：为长时程协作智能体合成可执行训练环境](#coworkenv)进一步打通可执行环境合成、程序化验证与 SFT/RL 训练闭环。
- **具身智能加速走向真实部署与群体经验学习**：[RLinf v0.4 发布：具身强化学习迈向真实物理世界](#rlinf-v0-4)补齐真机训练基础设施，[LoopWAM开源并登顶RoboChallenge Table30](#loopwam-robochallenge-table30)探索部署阶段自进化，[从车队经验中学习：机器人集体学习范式](#item-15)则通过跨机器人共享成败经验持续改进统一策略。
- **真实世界 Agent 的记忆、工具与评测逐渐一体化**：[OpenVLHarness：以多模态记忆增强真实世界视觉智能体工具使用](#openvlharness)结合持久记忆、证据渲染和工具层，[OR-License：现实世界运筹学智能体评测基准](#or-license)以客户模拟和隐藏验证考察专业长程任务能力。
- **热点延伸**集中在脑编码参数高效适配、第一人称三维表征、谱空间轻量化及多轮图像编辑，显示多模态模型正继续向科学应用、空间智能和生成一致性扩展。

## 对当前研究的启发
- **CacheEvolve**：[EdgeRock-4B](#edgerock-4b-kv-cache-99-1)证明固定容量记忆状态可在 256K 上下文中显著压缩 KV Cache，可作为“固定预算下学习保留历史信息”的重点架构案例。
- **SystemEvolve**：[Self-HPO](#self-hpo)交替优化交互框架与策略模型，为把脚手架修改、失败诊断和策略更新组织成可验证的递归系统优化闭环提供了直接范式。
- **EnvironmentEvolve**：[CoworkEnv](#coworkenv)以工作流约束、程序化验证和反馈修复合成可执行环境，可直接借鉴其“生成—验证—修复”流程提升环境生产的成功率与可训练性。
- **AgentTrainEvolve**：[CoworkEnv](#coworkenv)提供兼容 SFT 与 RL 的长程协作环境，而 [RLinf v0.4](#rlinf-v0-4)补充真机接口和异构训练能力，两者共同指向从环境合成到真实交互后训练的完整基础设施。
- **RobotEvolve**：[从车队经验中学习](#item-15)把多机器人部署中的成功轨迹与失败上下文回灌统一策略，可用于设计跨本体共享经验、持续训练并验证可靠性的具身数据飞轮。
- **MemoryEvolve**：[OpenVLHarness](#openvlharness)将证据渲染结果写入持久化多模态记忆并在后续工具调用中复用，为研究可审计的记忆写入、组合与成本收益评估提供了具体载体。
- **EvalEvolve**：[OR-License](#or-license)通过真实项目材料、客户模拟器和隐藏验证避免仅凭最终文本评分，可作为构建抗投机、过程可验证的专业 Agent 动态评测模板。
- **HarnessEvolve**：[Pi 1.0](#pi-1-0-pi-durable-mcp-code-mode)的任务持久化、安全重放、按需 MCP 与沙箱 Code Mode，展示了面向长程任务的 harness 应同时标准化恢复语义、工具加载和执行隔离。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-21/  

