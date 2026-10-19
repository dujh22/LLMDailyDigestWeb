# 2026-10-19 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 长期记忆成为今日最密集主线：从 [TIDER：强化学习引导的长程智能体记忆时序定位与双通道检索](#tider) 的时序检索、[GLOBE：面向生成式搜索商品优化的结构化智能体记忆演化](#globe) 的反馈闭环，到查询条件化证据编译、记忆选择与个性化门控，研究重点正由“存得更多”转向可学习的写入、定位、压缩和演化。
- 长程智能体训练集中攻克奖励与信用分配：[Reward Engine：面向开放式工具智能体的奖励中心自进化](#reward-engine) 为开放任务构造可验证奖励，[TreeOPSD：面向长程智能体强化学习的树感知后验蒸馏](#treeopsd) 改善终局奖励回传，[WebCoder：基于可执行产物反馈的通用前端开发智能体](#webcoder) 则展示了执行反馈驱动复杂编码能力的实效。
- 递归自我改进进一步延伸至科研闭环：[LM2LM：语言模型学习改进语言模型](#lm2lm) 以研究世界模型和真实实验校准学习模型改进方案，[DiscoveryRSI：递归学习发现高价值科学假设](#discoveryrsi) 递归优化假设价值，[Self-Building Labs：自主构建科学实验室](#self-building-labs) 更将自主演化推进到实验室设计与运行。
- 推理可靠性与成本控制开始联合优化：[VERITAS：通过计算言语化检测思维链忠实性](#veritas) 从内部计算轨迹定位不忠实推理，[RIVET：面向成本感知多轮 LLM 路由的响应知情价值估计](#rivet-llm) 学习逐轮调用价值；[Jev成Vercel平台采用最快的轻量级决策模型](#jev-vercel) 的快速普及也验证了受限输出快决策模型的产业需求。
- 数据、环境与脚手架正共同成为能力演化对象：[MetaCurate：演化高质量编程智能体数据筛选器](#metacurate) 自动演化轨迹筛选标准，[OfficeTown：生成式组织仿真促进智能体持续演进](#officetown) 合成持续运作的工作环境，[DrugHarness：面向计算药物发现的可演化智能体脚手架](#drugharness) 则把技能归纳、工具组合和独立验证接入科学工作流。

## 对当前研究的启发
- **MemoryEvolve**：[TIDER](#tider) 的时序定位、[GLOBE](#globe) 的字段级行为记忆与 MemCompile 的证据编译可组合成“学习写入—时序寻址—按查询压缩”的长期记忆流水线。
- **AgentTrainEvolve**：[Reward Engine](#reward-engine)、[TreeOPSD](#treeopsd) 与 [WebCoder](#webcoder) 表明，长程 Agent RL 可围绕自动生成验证器、分支级回报传播和可执行产物反馈统一设计信用分配。
- **AgentEvolve**：[Darwin-Claw：环境自适应的递归自进化智能体经验整合框架](#darwin-claw) 与 CDSE 提示应将情景经验、原型、元认知和脚本技能分层更新，而非把所有经验压入单一记忆库。
- **Awesome-RSI**：[LM2LM](#lm2lm) 用可扩展代理奖励配合周期性真实实验校准，为评估 RSI 是否持续产生真实改进而非代理目标过拟合提供了可复用范式。
- **ResearchEvolve**：[DiscoveryRSI](#discoveryrsi)、[Self-Building Labs](#self-building-labs) 与 [DrugHarness](#drugharness) 展示了从假设搜索到实验基础设施和独立验证的端到端科研自进化链路。
- **CodeEvolve**：[WebCoder](#webcoder) 将可执行前端产物转化为训练反馈，[MetaCurate](#metacurate) 自动演化轨迹筛选器，可共同降低仓库级编码 Agent 的环境与高质量数据构建成本。
- **DataEvolve**：[MetaCurate](#metacurate) 说明数据策展器本身可以作为可执行程序被演化，并以成对评判替代大量人工编写的任务专用筛选规则。
- **EnvironmentEvolve**：[OfficeTown](#officetown) 将组织、任务、上下文和反馈持续生成化，可作为工作场景 Agent 自动课程与长期演进环境的原型。
- **JevEvolve**：[RIVET](#rivet-llm) 的多轮价值估计与 Jev 的产业采用共同支持“高频步骤用快决策、低置信度步骤升级慢模型”的在线路由架构。
- **EvolveLRM**：[VERITAS](#veritas) 对内部计算偏移的定位可与不完美验证器下的预算分配结合，用于避免把相关错误产生的额外测试时计算误判为有效证据。
- **HarnessEvolve**：[DrugHarness](#drugharness) 将工具、轨迹归纳和独立验证模块化，提供了让科研 Agent harness 自身参与技能演化与质量控制的具体实现路径。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-19/  

