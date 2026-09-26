# 2026-09-26 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **长程智能体架构走向状态化与角色解耦**：4 项工作分别从主动式个人操作系统、可编辑任务状态、规划—综合分工及程序合成切入，代表包括 [Today发布：主动式个人Agent操作系统](#today-agent)、[AEWM：面向 LLM 智能体的可编辑世界模型](#aewm-llm) 和 [IterSynth：角色解耦的迭代式深度搜索智能体](#itersynth)。
- **训练、执行与验证开始形成闭环共进化**：[Qwen-Planner-Agent：真实世界移动规划智能体的闭环 AI-for-AI 框架](#qwen-planner-agent-ai-for-ai) 用统一动作—反馈—验证契约贯通数据生产、模型训练与部署，[编码智能体求解广义任务与运动规划](#item-9) 则展示了从环境交互中自动合成可跨实例泛化程序的路径。
- **世界理解与多模态数据基础设施继续补强**：[WROP：在世界模型中训练物体恒存性](#wrop) 以 150 类认知任务训练物体恒存性，[RGBD20K：大规模 RGB-D 语义分割基准](#rgbd20k-rgb-d) 则通过两万组细粒度标注扩展 RGB-D 感知评测。
- **模型测量同时关注内部表征、架构容量与基准可信度**：[SAE 潜在空间中涌现的词性类别](#sae) 揭示词性的分布式潜在编码，[神经谱容量：无需训练的架构测量与设计](#item-8) 提供免训练容量估计，而 [AI在门萨图形推理测试中触及151分理论上限](#ai-151) 再次暴露高分背后的基准污染与测量效度问题。

## 对当前研究的启发
- **DataEvolve**：[Qwen-Planner-Agent：真实世界移动规划智能体的闭环 AI-for-AI 框架](#qwen-planner-agent-ai-for-ai) 表明可将真实执行轨迹及验证结果持续回流为训练数据，形成面向移动规划的数据飞轮。
- **EvolveLLM**：[Qwen-Planner-Agent：真实世界移动规划智能体的闭环 AI-for-AI 框架](#qwen-planner-agent-ai-for-ai) 提供了以统一交互契约连接数据、训练和部署反馈的模型持续迭代范式。
- **HarnessEvolve**：[Qwen-Planner-Agent：真实世界移动规划智能体的闭环 AI-for-AI 框架](#qwen-planner-agent-ai-for-ai) 的动作—反馈—验证契约可作为标准化 Agent harness 接口，并用于研究执行框架与模型协同优化对性能的影响。
- **MemoryEvolve**：[Today发布：主动式个人Agent操作系统](#today-agent) 的长期记忆与 [AEWM：面向 LLM 智能体的可编辑世界模型](#aewm-llm) 的污染状态修订共同提示，记忆系统不仅要支持持久写入和检索，还需具备可验证的纠错与清理机制。
- **ResearchEvolve**：[IterSynth：角色解耦的迭代式深度搜索智能体](#itersynth) 说明将研究规划与证据综合分离、以动态摘要传递状态，可提升长周期文献研究的稳定性与可训练性。
- **EnvironmentEvolve**：[编码智能体求解广义任务与运动规划](#item-9) 展示了从环境交互中自动合成跨实例规划程序的能力，可用于构造“生成任务—执行验证—沉淀求解器”的环境进化闭环。
- **EvalEvolve**：[AI在门萨图形推理测试中触及151分理论上限](#ai-151) 表明静态公开推理卷已接近失效，应转向保密题、动态变体与污染审计相结合的持续评测。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-26/  

