# 2026-09-26 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 长程智能体开始围绕“可维护状态＋角色分工＋程序合成”提升执行可靠性：[AEWM：面向 LLM 智能体的可编辑世界模型](#aewm-llm)主动修订受污染状态，[IterSynth：角色解耦的迭代式深度搜索智能体](#itersynth)拆分规划与证据综合，[编码智能体求解广义任务与运动规划](#item-8)则从交互中合成可跨实例泛化的规划程序。
- 数据、训练与执行框架的一体化闭环成为智能体自进化主线：[Qwen-Planner-Agent：真实世界移动规划智能体的闭环 AI-for-AI 框架](#qwen-planner-agent-ai-for-ai)以统一动作—反馈—验证契约贯通数据生产、模型训练和部署，[Skild AI以140年虚拟自博弈训练人形足球机器人](#skild-ai-140)则展示了稀疏奖励、自博弈与仿真到现实迁移的规模化路径。
- 世界理解向对象认知和多感官空间建模推进：[WROP：在世界模型中训练物体恒存性](#wrop)用150类认知任务强化物体恒存性，[OmniEcho：面向具身智能体的空间音频理解](#omniecho)引入空间音频定位与导航，[RGBD20K：大规模 RGB-D 语义分割基准](#rgbd20k-rgb-d)补充大规模深度视觉数据基础。
- 模型内部机制与高效设计出现多条探索：[Transformer 可同时生成双重思路：LLM 线性叠加证据](#transformer-llm)揭示单次前向生成双候选的可能，[SAE 潜在空间中涌现的词性类别](#sae)刻画分布式语言表征，[神经谱容量：无需训练的架构测量与设计](#item-8)尝试以权重谱实现免训练容量评估和架构搜索。
- AI 原生应用与生成体验继续向主动化、长周期化发展：[Today发布：主动式个人Agent操作系统](#today-agent)整合长期记忆、主动提醒和云端执行，[WanPE：面向文本生成视频的电影级提示词增强](#wanpe)通过跨镜头规划提升长视频质量；与此同时，[AI在门萨图形推理测试中触及151分理论上限](#ai-151)再次暴露静态基准饱和、污染与效度问题。

## 对当前研究的启发
- **DataEvolve**：[Qwen-Planner-Agent：真实世界移动规划智能体的闭环 AI-for-AI 框架](#qwen-planner-agent-ai-for-ai)表明可将真实执行轨迹经反馈与验证直接转化为下一轮训练数据，为数据飞轮提供统一且可审计的生产契约。
- **EvolveLLM**：[Qwen-Planner-Agent：真实世界移动规划智能体的闭环 AI-for-AI 框架](#qwen-planner-agent-ai-for-ai)提供了模型与执行框架协同迭代的实例，可用于研究模型能力提升是否来自数据、训练策略还是 harness 演进。
- **HarnessEvolve**：[Qwen-Planner-Agent：真实世界移动规划智能体的闭环 AI-for-AI 框架](#qwen-planner-agent-ai-for-ai)的动作—反馈—验证契约可沉淀为移动智能体 harness 的标准接口，并支持跨模型复现和归因比较。
- **MemoryEvolve**：[Today发布：主动式个人Agent操作系统](#today-agent)与[IterSynth：角色解耦的迭代式深度搜索智能体](#itersynth)分别提供产品级长期记忆和任务级动态摘要案例，可用于研究记忆写入、压缩与主动调用如何共同支撑长周期任务。
- **ResearchEvolve**：[IterSynth：角色解耦的迭代式深度搜索智能体](#itersynth)说明将规划与证据综合解耦、同时维护动态研究摘要，可能提升自主科研中长程文献搜索与结论整合的稳定性。
- **EnvironmentEvolve**：[编码智能体求解广义任务与运动规划](#item-8)展示了从环境交互中自动合成跨实例规划程序的路径，可进一步扩展为任务生成、执行验证与求解器共同演化的环境闭环。
- **EvalEvolve**：[AI在门萨图形推理测试中触及151分理论上限](#ai-151)凸显静态公开题在能力饱和后难以区分模型，支持引入保密题、动态等价变体和污染审计来维持评测效度。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-26/  

