# 2026-10-26 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **智能体自进化转向执行框架级优化**：Google 开源的 [Harness²：双层递归优化智能体执行框架](#harness-2)同时迭代任务执行与元级改进机制，无需修改模型权重或真实标签即可跨任务复用经验。
- **具身智能探索参数冻结后的持续成长**：[RAX：在线探索扩展驱动机器人持续自我改进](#rax)通过在线探索、控制程序生成和技能积累，在五大仿真基准上平均领先既有 SOTA 37.4 个百分点。
- **Agent 基础设施的重点从提示技巧延伸至 Harness 与安全环境**：[提示词工程退潮：核心工作转向智能体 Harness](#harness)强调底层执行系统的重要性，而 [OpenAI以断网沙箱重启前沿强化学习训练](#openai)展示了前沿 Agent 训练对隔离、红队和停机机制的新要求。
- **开放模型继续扩展长程 Agent 能力边界**：[月之暗面发布旗舰模型 Kimi K3.1 Pro](#kimi-k3-1-pro)以大规模强化学习、百万上下文和开放权重强化代码、研究及长程任务能力。

## 对当前研究的启发
- **AgentEvolve**：[Harness²](#harness-2)的双层递归优化与 [RAX](#rax)的在线技能积累表明，冻结参数后可将执行轨迹分别沉淀为可迁移的框架经验和可调用技能。
- **HarnessEvolve**：[Harness²](#harness-2)把 Harness 从人工设计的固定脚手架变为可依据轨迹持续递归优化的对象，可直接作为框架版本迭代与跨任务复用机制的参考。
- **RobotEvolve**：[RAX](#rax)验证了“在线探索—程序生成—技能库积累”可以在不更新机器人模型参数的情况下显著提升控制能力，为具身推理时自进化提供了强基线。
- **EnvironmentEvolve**：[OpenAI 的断网沙箱方案](#openai)说明训练环境不仅要可执行、可验证，还需将网络隔离、漏洞红队和紧急停机纳入环境工程的默认组件。
- **Awesome-RSI**：[Harness²](#harness-2)将改进机制自身纳入元级递归优化，是值得收录并重点考察长期稳定性、经验迁移与目标作弊风险的 RSI 实例。
- **NewModel**：[Kimi K3.1 Pro](#kimi-k3-1-pro)提供了“超大规模参数＋百万上下文＋大规模 RL＋开放权重”的新观察样本，可用于分析长程 Agent 能力究竟来自模型规模、上下文还是后训练配方。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-26/  

