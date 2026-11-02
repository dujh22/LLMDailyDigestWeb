# 2026-11-02 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- Agent 系统开始从单会话脚手架走向可持续运行与自我改进：[DeepSeek 提出下一代 Super-agent Harness 架构](#deepseek-super-agent-harness)以分层并发、状态持久化和 Watchdog 支撑长期在线，[HarnessEvolve](#harnessevolve)则用参考轨迹与双质量门约束脚手架进化，LobeHub 进一步探索多智能体组织的自动交接与验收。
- 记忆自进化同时向架构搜索、结构化经验和参数化在线学习推进：[MemEvolve](#memevolve)联合优化经验与记忆架构，[MEMIG](#memig)展示可索引干预记忆在抗体优化中的价值，[Falcon](#falcon)则把快速权重记忆建模为在线学习过程。
- 奖励与信用分配成为长程 Agent 训练的关键主线：[Self-Evolving Rubrics](#self-evolving-rubrics)汇总动态准则生成路线，[CivHarness](#civharness-freeciv)通过分支回放和局面评判器缓解长程博弈中的记分板陷阱。
- 具身智能出现覆盖部署后学习的完整闭环：[智元发布具身智能模型 GO-3 Preview](#go-3-preview)串联预训练、虚实后训练和真机持续学习，体现机器人基础模型由一次性交付转向真实环境中的持续进化。
- 安全治理开始直接介入编码 Agent 的系统提示，但 Claude Code 限制复刻现有游戏的做法也暴露出规则易绕过、误拒原创需求以及仅靠提示层约束可靠性不足的问题。

## 对当前研究的启发
- **HarnessEvolve**：[HarnessEvolve](#harnessevolve)的首偏离点定位、质量门与性能门可直接用于构建既防泄漏又防提示膨胀和能力退化的脚手架进化流程。
- **SystemEvolve**：[DeepSeek Super-agent Harness](#deepseek-super-agent-harness)表明 Router-Worker、事件驱动、存算分离与自愈监控可作为长期在线自进化系统的基础运行时。
- **MemoryEvolve**：[MemEvolve](#memevolve)提示记忆研究不应只优化写入和检索策略，还可把记忆架构本身纳入外层元进化闭环。
- **AgentTrainEvolve**：[CivHarness](#civharness-freeciv)的分支未来回放可将延迟后果转化为可训练的局面价值信号，为长程交互中的信用分配提供具体方案。
- **EvolveLLM**：[Self-Evolving Rubrics](#self-evolving-rubrics)展示了让评价准则随策略能力共同演化的路径，可为开放式生成任务持续提供比固定奖励更细粒度的训练信号。
- **RobotEvolve**：[GO-3 Preview](#go-3-preview)将虚实后训练与部署后持续学习串成闭环，可作为检验机器人自进化是否真正跨越 sim-to-real 的系统范式。
- **ResearchEvolve**：[MEMIG](#memig)说明科研 Agent 的经验应保存为可定量检索的“干预—效果—交互关系”，而非难以验证和复用的自由文本反思。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-02/  

