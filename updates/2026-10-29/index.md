# 2026-10-29 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **新模型竞逐长程智能体与成本效率**：OpenAI 的 [GPT-6.1 Terra](#openai-gpt-6-1-terra-astra) 以约十分之一成本逼近旗舰电脑操作能力，[Gemini 4 Carbon](#gemini-4-carbon) 强化长程编程与安全防御，开源的 [Ling-3.1-flash-1019](#personal-agent-ling-3-1-flash-1019) 则面向个人智能体优化多步骤执行。
- **递归自我改进从模型扩展到完整系统闭环**：[The Trinity](#the-trinity) 协同演化环境、能力树与 Harness，[RuHarness](#ruharness) 让评判准则和脚手架共同迭代，[ForgeKernel](#forgekernel) 则以跨硬件算子榜首展示了可验证反馈驱动的基础设施自进化。
- **Agent 训练转向可控环境、交互合成与动态编排**：[Trajectory2Gym](#trajectory2gym) 合成决策驱动的有状态交互，[可控环境合成揭示工具使用智能体缩放定律](#item-58) 建立环境多样性与泛化能力的量化关系，[DynaFlow](#dynaflow) 进一步让主智能体自主学习多智能体工作流。
- **长期学习的重点从“添加记忆”转向净收益与可靠评测**：[Memory Tax](#memory-tax) 发现复杂记忆系统常不及朴素 RAG，[CLE](#cle-llm) 揭示前沿 Agent 仍难跨长程工作流积累经验，[TTME](#ttme) 则表明演化外部记忆可低成本支持科学发现；[TraceTrial-Bench](#tracetrial-bench) 补充了运行框架故障归因能力。
- **AI 科研取得超大规模成果，但验证与评审成为核心瓶颈**：[数十个 AI Agent 24 天形式化有限单群分类定理](#ai-agent-24) 展示群体形式化能力，而 [Ai2 新颖性评判基准](#ai2-llm) 证明 LLM 对研究创新性的判断高度不稳定，提示重大科研主张仍需独立审验。
- **热点延伸**：低相关性条目主要集中在主动式 AI 框架、视频与空间音频生成、长视频取证及空间 VLM，反映多模态系统正向连续交互和长时序处理扩张。

## 对当前研究的启发
- **Awesome-RSI**：[The Trinity](#the-trinity) 与 [RuHarness](#ruharness) 表明，可持续 RSI 应把环境生成、评判准则和 Harness 一并纳入递归改进闭环，而非只优化模型或提示。
- **AgentTrainEvolve**：[Trajectory2Gym](#trajectory2gym) 和 [可控环境合成揭示工具使用智能体缩放定律](#item-58) 提供了从交互覆盖设计到环境多样性配比的可操作训练路线，可用于构建可预测扩展的工具 Agent 课程。
- **HarnessEvolve**：[智能体接口的决策几何](#harness) 与 [TraceTrial-Bench](#tracetrial-bench) 提示 Harness 评测必须同时披露策略适配程度，并以执行证据区分模型故障、接口偏置和运行时故障。
- **Groom**：[TraceTrial-Bench](#tracetrial-bench) 的多源证据与机制链归因可直接借鉴为过程级 token 归因框架，将冗余消耗关联到具体决策和故障传播环节。
- **MemoryEvolve**：[Memory Tax](#memory-tax) 要求记忆方案以朴素历史检索为强基线核算净收益，而 [HABIT-Bench](#habit-bench) 可补充对跨会话弱证据归纳能力的专项测量。
- **ResearchEvolve**：[Ai2 新颖性评判基准](#ai2-llm) 与 [OpenAI 邀外部专家及 Lean 核查证明](#openai-lean-ai) 共同说明，科研智能体需要把新颖性评审的不确定性估计和外部形式化复核设为默认流程。
- **InfraEvolve**：[ForgeKernel](#forgekernel) 的跨 CANN/CUDA 榜单结果证明，基于真实硬件执行反馈的生成—验证—保留闭环能够跨平台沉淀算子优化能力。
- **HumanEvolve**：[Anthropic 专家决策实验](#anthropic-ai) 显示专业用户也会受 AI 预设立场显著影响且难以自知，因而人机协同界面应显式呈现建议来源、反方证据与影响校准。
- **PersonalEvolve**：[Ling-3.1-flash-1019](#personal-agent-ling-3-1-flash-1019) 与 [HABIT-Bench](#habit-bench) 分别提供个人 Agent 长程执行底座和习惯归纳评测，可组合验证真实反馈能否转化为稳定个性化能力。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-29/  

