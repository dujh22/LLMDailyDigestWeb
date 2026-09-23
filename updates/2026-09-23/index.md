# 2026-09-23 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从概念框架走向可运行闭环：共 6 项工作覆盖运行经验回流、模型与脚手架联合演化及自主科研，[基元律动](#agent)提出由多模型调度迈向 RSI 反馈闭环，[MiMo-V2.6](#mimo-v2-6-rl-rsi)以 75 万条智能体轨迹开展大规模 RL，[AIDE²](#item-42)则通过改写、评测和筛选自身代码实现连续改进。
- 智能体基础设施同步向规模化、低成本与可靠执行演进：[DSec](#deepseek-dsec-5000-agent)实现每秒创建 5000 多个训练沙盒，[Agensh](#agensh-1-024)扩展至 1,024 个自组织智能体，[FIRE](#fire)和[Growing Harness](#growing-harness)分别利用历史失败干预与失败驱动代码修复提升成功率、沉淀可复用能力。
- 前沿模型竞争进一步转向长程 Agent 的单位任务成本：[Grok 4.7](#grok-4-7-coding-agent)扩展至 50 万 Token 并强化编程与复杂任务，[GPT-6 Sol、Luna 与 Claude Opus 5.5](#gpt-6-sol-luna-claude-opus-5-5)强调推理效率和性价比，而[CliffCompaction](#cliffcompaction)展示了百万词元任务中最高 50% 的上下文成本降幅。
- 智能体评测的主线是从结果分数转向生产真实性与测量有效性：[SWE-Serve](#swe-serve)以真实推理服务变更检验生产正确性，[代码漏洞修复评测审计](#llm)揭示编译率等代理指标失效，[本地工具调用评测研究](#item-35)则指出服务栈、解码和统计口径足以扭曲模型能力结论。
- 多模态智能体正在打通生成、世界建模与具身控制：[VideoGen-Agent](#videogen-agent)以多任务 RL 编排视频工具，[WorldCrafter](#worldcrafter)引入可查询的隐式三维记忆，[RoboDawn](#robodawn)与[Grounded Action Model](#grounded-action-model-3d)分别探索免任务训练闭环控制和对象中心 3D 对齐。
- 推理训练与可解释性出现新的效率—可信度张力：[超越重复采样](#item-34)学习语义多样化搜索策略，[面向低比特推理的在策略蒸馏](#item-33)恢复亚 3 比特模型的长程能力，而[无意义填充词实验](#gpt-6-astra)和[隐藏思维链提取](#item-37)提示额外 Token、内部计算与过程监控之间仍存在明显盲区。

## 对当前研究的启发
- **Awesome-RSI**：[基元律动](#agent)、[MiMo-V2.6](#mimo-v2-6-rl-rsi)与[AIDE²](#item-42)分别提供“经验回流—大规模轨迹 RL—自改写评测筛选”三类闭环实例，可用于细化 RSI 自主性层级及持续增益证据标准。
- **EvolveLLM**：[MiMo-V2.6](#mimo-v2-6-rl-rsi)表明多任务智能体轨迹可同时改善长程执行、软件工程和多模态能力，适合作为研究通用能力自进化及跨任务迁移的规模化案例。
- **EvolveLRM**：[超越重复采样](#item-34)以小型策略模型引导冻结大模型进行语义级搜索，提供了比盲目增加采样次数更高效的测试时自进化路径。
- **DataEvolve**：[TransBERT](#transbert)证明纯合成翻译语料可支撑低资源专业领域预训练，而[onPanda](#onpanda)提供保留模型在策略分布的低成本纠错数据生成机制，可共同启发合成数据价值与分布匹配研究。
- **EvalEvolve**：[代码漏洞修复评测审计](#llm)与[本地工具调用评测研究](#item-35)说明动态基准不仅要更新题目，还必须审计指标构念效度并完整披露服务栈等测量条件。
- **HarnessEvolve**：[Growing Harness](#growing-harness)展示了将失败轨迹自动编译为可回滚专家脚手架的方法，[FIRE](#fire)则表明无需改权重即可把历史失败转化为运行时可靠性策略。
- **Groom**：[CliffCompaction](#cliffcompaction)的低损上下文删减与[Brood War Bench](#brood-war-bench-19)揭示的观察—决策—执行时效瓶颈，可用于扩展过程级 Token 归因中的压缩收益和闭环延迟指标。
- **MemoryEvolve**：[SpeakerMem-R1](#speakermem-r1)的说话者中心双轨状态与[Zeva-Ego](#zeva-ego)的因果记忆分别提供长期对话归因和部署中经验复用的具体记忆演化机制。
- **ResearchEvolve**：[AIDE²](#item-42)通过迭代改写、执行评测和择优保留科研代码获得跨领域泛化，为自主科研系统建立“可执行产物驱动”的自改进闭环提供了直接方案。
- **SwarmEvolve**：[Agensh](#agensh-1-024)与[MAGIC](#magic)分别从无中心异步协作和奖励驱动动态图编排展示群体结构扩展路径，而[社会规范机制评测](#llm-3)提示应同时测量行为、经验预期和规范预期以辨别真实涌现机制。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-23/  

