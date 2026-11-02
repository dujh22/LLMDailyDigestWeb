# 2026-11-02 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **Agent Harness 从单会话工具走向可持续、自修复的运行系统**（2 项）：[DeepSeek提出下一代 Super-agent Harness 架构](#deepseek-super-agent-harness)以 Router-Worker、事件驱动和运行时自愈支撑并发长程任务，[HarnessEvolve：基于参考轨迹的可靠智能体自我进化](#harnessevolve)则通过首偏离点定位与双质量门实现可靠的脚手架迭代。
- **自进化对象扩展到记忆架构与奖励准则**（2 项）：[MemEvolve：智能体记忆架构的元进化](#memevolve)联合优化经验和记忆结构，[Self-Evolving Rubrics：自进化准则驱动强化学习](#self-evolving-rubrics)展示动态准则为开放式生成及多步 Agent 提供持续、细粒度奖励的路径。
- **长程协作与持续学习呈现系统化趋势**（2 项）：[LobeHub 的 Super-agent 组织协作实验](#lobehub-super-agent)以分层智能体、持久运行时和自动验收模拟自治组织，[Falcon快速权重注意力实现持续学习](#falcon)则把递归快速权重记忆转化为在线学习机制，兼顾持续适应与长度外推。
- **编码 Agent 的治理开始直接进入系统提示与产品边界**：[Claude Code修改系统提示词，限制复刻现有游戏](#claude-code)体现了通过 Harness 层施加版权与安全约束的现实尝试，也暴露出易绕过和误拒绝问题。

## 对当前研究的启发
- **HarnessEvolve**：[HarnessEvolve](#harnessevolve)的首偏离点信用分配、质量门与性能门可直接用于构建“定位失败—生成修改—防泄漏与防退化—跨框架验证”的脚手架进化闭环。
- **MemoryEvolve**：[MemEvolve](#memevolve)表明不应只优化记忆内容的写入与检索策略，还可把记忆架构本身纳入外层元进化，并以近似固定 API 成本约束搜索。
- **AgentTrainEvolve**：[Self-Evolving Rubrics](#self-evolving-rubrics)提供了将开放式目标动态分解为细粒度、随策略能力演化的奖励准则的方法，可缓解多轮 Agentic RL 的奖励稀疏与信用分配问题。
- **SwarmEvolve**：[LobeHub 的组织协作实验](#lobehub-super-agent)提示可把跨项目交接、分层权限和 Acceptance 自动验收视为群体协作结构的可进化变量，而非固定编排规则。
- **SystemEvolve**：[DeepSeek Super-agent Harness](#deepseek-super-agent-harness)的事件驱动 Router-Worker 与运行时自愈机制，为系统级自进化提供了可持续在线、并发试验和故障恢复的底层载体。
- **CacheEvolve**：[Falcon](#falcon)将固定状态的递归快速权重解释为在线学习，为固定预算下可学习的记忆更新、归一化与遗忘策略提供了模型架构侧参照。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-02/  

