# 2026-10-18 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从单点反思走向“世界模型—Harness—验证器”系统闭环：[Memento 3](#memento-3) 以可执行世界模型持续修正规则，[Google Harness²](#google-harness-agent) 则在冻结权重、缺少真实验证器时递归演化 Agent 外壳，显示系统组件已成为 RSI 的核心改进对象。
- 具身自进化集中突破长程泛化与持续学习：[Recursia](#recursia) 通过双层递归改进共享技能栈，[RoboFoundry](#robofoundry) 联合进化上下文、记忆、技能和接口，[EmbodiedCLBench](#embodiedclbench) 则补上技能重组与组合泛化评测。
- 自主科研同时推进方法与评测：[Fork-and-Flush](#fork-and-flush) 以刷新上下文和并行分叉改善长程探索，[ASI-Bench](#asi-bench-ai) 与 [DeepRSI](#deeprsi-48-kimi-k3) 分别暴露“方法提示难以操作化”和验证器过拟合、奖励投机等关键瓶颈。
- 多智能体演化从人工编排转向自动搜索与经验回灌：[FlowMAS](#flowmas) 学习协作拓扑，[MASS](#mass) 交替搜索工作流并把优质协作轨迹微调回共享模型，形成群体结构与模型参数协同进化。
- 环境、训练与执行基础设施进一步一体化：[MAI-Gym](#mai-gym-gui) 打通 GUI 评测、采集和在线强化学习，[Tev](#tev) 为长时程任务提供可验证的密集进度奖励，[OpenGCUA](#opengcua) 则开放执行框架、提示与轨迹，推动 Harness 能力向模型迁移。
- 热点延伸覆盖空间推理、多模态生成、蒸馏与推理系统优化，但相关性较低的工作主要是能力组件创新，尚未形成与当前自进化主线直接衔接的闭环。

## 对当前研究的启发
- **Awesome-RSI**：[Memento 3](#memento-3) 与 [Google Harness²](#google-harness-agent) 表明可将“可执行世界模型”和“可迁移 Harness 编辑经验”并列纳入 RSI 分类，并重点比较其验收机制与跨任务单调改进能力。
- **AgentEvolve**：[ReHarness](#reharness) 的后向修订机制可用于把新任务反馈追溯写回历史经验，降低冻结参数 Agent 长期积累错误记忆的风险。
- **RobotEvolve**：[Recursia](#recursia) 的共享可执行技能栈与 [EmbodiedCLBench](#embodiedclbench) 的未见任务技能重组，可组合成“技能演化—组合泛化”方法及评测闭环。
- **ResearchEvolve**：[Fork-and-Flush](#fork-and-flush) 提供了保留工作区但清空对话历史的并行探索策略，可直接用于缓解科研 Agent 的上下文惯性与早期假设锁定。
- **EvalEvolve**：[DeepRSI](#deeprsi-48-kimi-k3) 暴露的公开验证器过拟合和奖励投机说明长周期评测必须引入隐藏验证器、过程审计与跨任务复验。
- **SwarmEvolve**：[FlowMAS](#flowmas) 与 [MASS](#mass) 分别给出拓扑搜索和协作轨迹回灌路径，可据此研究群体结构优化与共享模型训练的双层共同进化。
- **EnvironmentEvolve**：[MAI-Gym](#mai-gym-gui) 与 [Tev](#tev) 展示了并行可验证环境和密集进度奖励的组合，可用于构建随 Agent 能力增长而自动调难的长程训练环境。
- **HarnessEvolve**：[Google Harness²](#google-harness-agent) 和 [OpenGCUA](#opengcua) 提示应同时记录 Harness 的自修改轨迹及其向模型迁移后的增益，以区分外壳优化与模型能力提升。
- **MemoryEvolve**：[ReHarness](#reharness) 将历史经验视为可持续回溯修订的对象，为记忆系统增加“基于后续反馈纠错旧记忆”这一关键操作。
- **AgentTrainEvolve**：[MASS](#mass) 将多智能体任务交接轨迹转化为自监督训练信号，[Tev](#tev) 则补充长程信用分配，可共同支持更稳定的多轮 Agentic RL。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-18/  

