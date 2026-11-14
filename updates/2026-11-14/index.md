# 2026-11-14 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- RSI 从框架走向完整工程闭环（3 条）：[No Second Run](#no-second-run-rsi-801-30b-a3b) 用六智能体协同优化数据、基础设施与训练配置，[openJiuwen RSI 原生 AgentOS](#openjiuwen-rsi-agentos-agent) 则把功能自生成、热插拔、版本化和回退纳入运行时。
- 产业侧开始验证自进化的实际价值：[伐谋 3.0](#3-0-rsi) 将“设计—执行—验证—反馈”闭环用于材料、核聚变、芯片等场景，显示 RSI 正从模型实验进入可验证的生产流程。
- Agent 评测与训练信号进一步细化：[SO-Arena](#so-arena-system-one) 系统评估快决策模型的能力谱系、稳定性与拒答能力，[行动者、评判者还是教师？](#item-11) 则发现弱行动模型仍可通过完整轨迹事后评判提供有效训练信号。
- 效率优化同时深入上下文与模型架构：[CoACT](#coact-coding-agent) 以“保持下一步动作”为准则压缩 Coding Agent 上下文，[SimpleHC](#simplehc) 将超连接训练开销显著压低，[UniSpark](#unispark) 探索全注意力与线性注意力的混合多模态架构。
- 应用与数据基础设施继续扩展：[DeepSeek 应用 API](#deepseek-api-chat-demo) 打包开放搜索、文件解析和语音等产品能力，[Ropedia Xperience 2](#ropedia-xperience-2) 则提供可交互三维环境与人类行为轨迹，支撑具身数据规模化。
- 热点延伸集中在驾驶世界模型、高压缩图像生成与 4D 视频模型评测，包括 BirdDreams、G-STAR 和 WorldDraft，但与当前核心研究方向关联较弱。

## 对当前研究的启发
- **Awesome-RSI**：[No Second Run](#no-second-run-rsi-801-30b-a3b) 与 [openJiuwen RSI 原生 AgentOS](#openjiuwen-rsi-agentos-agent) 分别提供训练流程和部署系统两类 RSI 实例，可据此补充“优化对象—验证机制—版本回退”的分类框架。
- **SystemEvolve**：[openJiuwen RSI 原生 AgentOS](#openjiuwen-rsi-agentos-agent) 的热插拔、版本化与回退机制，为系统自改写建立可控变更与失败恢复层提供了直接设计参考。
- **EvolveLLM**：[No Second Run](#no-second-run-rsi-801-30b-a3b) 表明基础模型自进化可同时作用于数据、训练配置和基础设施，而非仅围绕权重更新或合成数据展开。
- **Groom**：[CoACT](#coact-coding-agent) 将“是否保持下一步动作”定义为上下文压缩目标，可转化为过程级 token 利用评测中的动作充分性指标与压缩基线。
- **AgentTrainEvolve**：[行动者、评判者还是教师？](#item-11) 说明应分离模型的在线行动能力与事后教学能力，并利用完整轨迹评判构造更可靠的长程信用分配信号。
- **EvalEvolve**：[SO-Arena](#so-arena-system-one) 的决策稳定性、交互执行和缺失答案识别维度，可用于设计面向快决策模型的动态可靠性评测。
- **EnvironmentEvolve**：[Ropedia Xperience 2](#ropedia-xperience-2) 将真实三维环境与人类行为共同转化为仿真场景和机器人轨迹，为研究环境—行为协同扩展及自动课程生成提供了数据底座。
- **NewApply**：[伐谋 3.0](#3-0-rsi) 的多产业闭环与 [DeepSeek 应用 API](#deepseek-api-chat-demo) 的能力组件化，分别提供了 RSI 垂直落地和通用 Agent 产品集成的观察样本。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-14/  

