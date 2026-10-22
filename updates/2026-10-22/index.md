# 2026-10-22 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **长程 Agent 基座迎来开放权重更新**：[阶跃星辰开放 Step 5 Preview 权重，面向长程 Agent](#step-5-preview-agent)结合稀疏 MoE、百万 token 上下文、上下文压缩与可验证环境训练，体现基础模型开始围绕长期任务执行进行端到端设计。
- **自进化从单点改进转向模型、脚手架与任务闭环协同**：3 项工作分别以[CoEvo-RSI](#coevo-rsi)缓解模型与执行框架的“脑—身体”错配、以[ScholarEvolve](#scholarevolve-agent-harness)从文献持续演化 Agent Harness，并以[RSIGame](#rsigame)打通游戏试玩、修复、验证及经验回灌。
- **Agent 系统向规模化协作和垂直能力拓展**：[Agensh](#agensh)展示最多 1024 个智能体无中心自组织开发软件，[FocusGUI](#focusgui-gui)和[S-Agent 2.0](#s-agent-2-0)则分别用动态证据压缩、持久化场景记忆改善 GUI 操作与三维空间推理。
- **冻结模型下的运行时优化成为效率主线**：[VLA-Rolling](#vla-rolling)通过自适应复用动作尾部同时提高具身控制速度与成功率，[SWIFT](#swift)则用弱去噪器外推目标，以约一半训练算力强化扩散模型。
- **热点延伸**：低相关性条目主要是 [Novix 招募 RSI、Agentic RL 与新架构研究人才](#novix-rsi-agentic-rl)，反映产业界对 RSI、环境和评测基础设施的投入信号，但尚无新的技术结果。

## 对当前研究的启发
- **NewModel**：[Step 5 Preview](#step-5-preview-agent)把百万级上下文、端到端压缩和可验证环境训练统一到长程 Agent 基座中，可作为分析“模型原生 Agent 能力”与外部 harness 增益边界的新样本。
- **HarnessEvolve**：[CoEvo-RSI](#coevo-rsi)与[ScholarEvolve](#scholarevolve-agent-harness)表明 harness 不应固定为评测外壳，而可与模型能力同步继承、组合和实证筛选。
- **TaskEvolve**：[RSIGame](#rsigame)提供了“生成作品—自主试玩—诊断修复—重新验收”的完整实现，可直接借鉴其局部开发闭环与全局质量控制机制。
- **AgentTrainEvolve**：[RSIGame](#rsigame)将开发闭环积累的经验继续用于训练底层模型，为把长程任务执行轨迹转化为参数侧持续改进提供了具体路径。
- **SwarmEvolve**：[Agensh](#agensh)以共享仓库、通信系统和上下文看板支撑千智能体无中心协作，可用于研究协作拓扑、冲突消解与群体规模扩展规律。
- **RobotEvolve**：[VLA-Rolling](#vla-rolling)说明具身系统可依据动作置信度动态决定复用与重新去噪预算，为实时控制中的经验缓存和快慢决策路由提供了可实现方案。
- **MemoryEvolve**：[S-Agent 2.0](#s-agent-2-0)的持久化场景记忆与闭合证据循环，可作为评估长期记忆是否真正支撑空间推理而非仅扩大上下文的案例。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-22/  

