# 2026-10-21 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- Agent 系统开始同时演化脚手架与策略：[Self-HPO](#self-hpo) 以交替优化应对持续变化的失败模式；[Pi 1.0](#pi-1-0-pi-durable-mcp-code-mode) 则补齐任务持久化、恢复、安全重放及原生 MCP 等生产级能力。
- 长程 Agent 的训练基础设施进一步完善：[CoworkEnv](#coworkenv) 自动合成可执行、可验证的协作环境，[RLinf v0.4](#rlinf-v0-4) 将多模态强化学习与异构训练推进至真实机器人部署。
- 具身智能围绕“经验—世界模型—部署自进化”形成主线：[LoopWAM](#loopwam-robochallenge-table30) 展示部署阶段自进化效果，[Holi-World](#holi-world) 则打通第一人称数据采集、世界表征、训练与评测。
- 固定预算长上下文取得显著系统收益：[EdgeRock-4B](#edgerock-4b-kv-cache-99-1) 在 256K 上下文下削减 99.1% KV Cache，并将单卡吞吐最高提升 6.42 倍。
- 真实世界智能体的记忆与评测继续走向可审计执行：[OpenVLHarness](#openvlharness) 以持久化多模态记忆组合证据，[OR-License](#or-license) 通过客户模拟与隐藏验证评估专业运筹任务。
- 热点延伸覆盖脑编码、第一人称三维重建、轻量表征和多轮图像编辑，代表性工作包括 [BrainLoRA](#brainlora)、[EgoXperience](#egoxperience) 与 [MT Forcing](#mt-forcing)。

## 对当前研究的启发
- **CacheEvolve**：[EdgeRock-4B](#edgerock-4b-kv-cache-99-1) 的固定容量“记忆岩锚”可作为学习式缓存淘汰机制的强基线，重点验证其在 Agent 多轮交互中的信息保真与吞吐收益。
- **SystemEvolve**：[Self-HPO](#self-hpo) 将交互框架和策略模型纳入同一交替优化闭环，为系统组件与参数协同进化提供了可复用范式。
- **CodeEvolve**：[Self-HPO](#self-hpo) 针对动态失败模式递归改造编码 Agent，可用于研究脚手架修改是否带来跨任务、持续且可验证的提升。
- **AgentTrainEvolve**：[CoworkEnv](#coworkenv) 的可执行环境合成与 [RLinf v0.4](#rlinf-v0-4) 的真机 RL 基础设施，可分别补足长程训练数据生产和物理部署闭环。
- **EnvironmentEvolve**：[CoworkEnv](#coworkenv) 以工作流约束、程序化验证和反馈修复保证合成环境质量，为“生成—执行—纠错”的环境自进化管线提供了直接实现。
- **RobotEvolve**：[LoopWAM](#loopwam-robochallenge-table30)、[RLinf v0.4](#rlinf-v0-4) 与 [Holi-World](#holi-world) 分别覆盖部署自进化、真机训练和第一人称世界建模，可拼接为具身数据回灌闭环。
- **HarnessEvolve**：[Pi 1.0](#pi-1-0-pi-durable-mcp-code-mode) 的可恢复执行与 [OpenVLHarness](#openvlharness) 的证据渲染层提示评测 harness 应显式记录重放状态、工具证据和记忆读写。
- **MemoryEvolve**：[OpenVLHarness](#openvlharness) 证明持久化多模态记忆能够降低推理成本并改善工具使用，适合作为证据级记忆写入、组合与淘汰策略的实验载体。
- **EvalEvolve**：[OR-License](#or-license) 的真实项目材料、客户模拟器与隐藏验证机制，为构建抗捷径、重过程且贴近业务结果的动态 Agent 评测提供了模板。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-21/  

