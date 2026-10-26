# 2026-10-26 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **智能体优化重心上移至系统层**：Google 开源 [Harness²：双层递归优化智能体执行框架](#harness-2)，以任务级和元级递归优化执行框架，在冻结模型权重的前提下利用轨迹反馈持续提升表现。
- **具身智能探索出推理时技能演化路径**：[RAX：在线探索扩展驱动机器人持续自我改进](#rax) 通过在线探索生成控制程序并沉淀可复用技能，在五类仿真基准上平均领先既有 SOTA 37.4 个百分点。
- **提示工程正在向 Harness 工程转型**：[提示词工程退潮：核心工作转向智能体 Harness](#harness) 指出能力释放的关键正从面向用户的提示“咒语”，转向底层提示、工具调用、执行框架与系统工程的协同设计。

## 对当前研究的启发
- **AgentEvolve**：[RAX](#rax) 与 [Harness²](#harness-2) 分别验证了技能库积累和执行轨迹驱动的框架优化，可作为参数冻结 Agent 持续进化的两类互补机制。
- **RobotEvolve**：[RAX](#rax) 表明机器人可在部署时将在线探索转化为控制程序和可复用技能，为具身自进化补充了无需更新模型参数的实践路线。
- **HarnessEvolve**：[Harness²](#harness-2) 将 Harness 从人工配置对象变成可递归优化的系统组件，可直接启发执行轨迹反馈、框架变异与择优保留机制的设计。
- **SystemEvolve**：[Harness²](#harness-2) 的任务级—元级双层闭环提供了系统自指改进的具体实现，可用于研究工作流与改进机制本身的联合演化。
- **PromptEvolve**：[提示词工程退潮](#harness) 提示应将优化单条提示扩展为联合优化系统提示、工具约定和执行脚手架的多组件 LM 程序。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-26/  

