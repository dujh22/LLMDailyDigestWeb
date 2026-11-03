# 2026-11-03 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从系统闭环推进到权重空间：[Astra 直接编程神经网络权重](#astra-qwen)展示无梯度读写模型参数，[R²Orch](#r-orch)则以自博弈和技能内化持续改进智能体编排；与此同时，[Anthropic 对 RSI 阈值的警示](#anthropic-rsi)凸显验证与治理可能落后于能力增长。
- Agent 训练与环境工程进一步围绕“更深任务、可验证环境、自动课程”收敛：[终端长程任务的真实深度测量与合成](#item-30)提出模型无关的交互深度指标，[LegoEnv](#legoenv)以原子模块重组自演化环境，[Thinker-Sim](#thinker-sim)则打通具身场景、数据、评测与 Sim2Real。
- 部署期 Agent 的主线转向经验复用和可信执行：[Meta Routed CL](#meta-routed-cl)通过路由隔离经验兼顾持续学习与成本，[MemUse](#memuse)把评测落到记忆是否真正影响行动，[RECEIPT](#receipt)则修复工具交互中的假成功与超时。
- 评测可靠性暴露出基础缺口：[不可能代码，评分几乎不变](#item-39)发现强代码评判器对语法无效输出仍可能给出近似评分，而 BHI、RubricWorld 与科研报告治理工作分别从基准健康度、评分规约和确定性门控补强评测链路。
- 模型与系统侧兼顾新架构和推理效率：[SenseNova Loop-9B-Preview](#sensenova-loop-9b-preview)以参数共享循环计算换取有效深度，[CacheWeave](#cacheweave-kv)学习选择性重计算以复用位置无关 KV 缓存；具身运行时方面，[REA](#rea)用异步快慢控制避免高层推理阻塞执行。
- 热点延伸主要包括尚待官方确认的 GPT-6.2 Astra、Claude 5.5 爆料，以及 FrameForge 图像生成和 ReLift 三维跟踪等视觉方向进展，当前证据或方向相关性有限。

## 对当前研究的启发
- **Awesome-RSI**：[Astra 权重空间编程](#astra-qwen)把自我修改推进到参数层，而[代码评判器复现实验](#item-39)表明其闭环必须依赖可执行验证而非模型自评。
- **AgentEvolve**：[SeaFlow](#seaflow)证明可将执行反馈沉淀为可审计的代码优先工作流，为冻结参数下持续修订 Agent 脚手架提供了直接方案。
- **AgentTrainEvolve**：[R²Orch](#r-orch)的任务自选、自博弈与失败内化可作为自动课程闭环，而[DEPTH](#item-30)提供了避免课程难度被模型轮数误导的度量。
- **EnvironmentEvolve**：[LegoEnv](#legoenv)的意图、规则、数据和服务器原子化设计，为环境组件独立验证、重组和持续演化提供了可复用抽象。
- **MemoryEvolve**：[MemUse](#memuse)提示记忆系统不能只测检索命中率，应沿交付后的行动轨迹评估记忆是否被采用以及是否真正改善结果。
- **HarnessEvolve**：[RECEIPT](#receipt)表明工具返回协议本身会制造假成功，适合纳入 harness 的标准化交互检查与执行验收层。
- **EvalEvolve**：[不可能代码，评分几乎不变](#item-39)揭示 LLM 评判器存在严重有效性风险，应把语法检查、执行测试和对抗性无效答案纳入动态评测。
- **CacheEvolve**：[CacheWeave](#cacheweave-kv)把缓存复用转化为可学习的块选择与重计算决策，可用于探索固定计算预算下的自适应缓存管理。
- **ResearchEvolve**：[Hyra 2.0](#hyra-2-0-agent)的状态持久化、证据复核与技能沉淀展示了科研智能体从一次性任务执行走向可持续升级工具链的工程路径。
- **RobotEvolve**：[Thinker-Sim](#thinker-sim)将场景重建、仿真数据、能力评测和任务编排置于同一闭环，可作为机器人环境—数据—策略协同进化的基础设施参考。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-03/  

