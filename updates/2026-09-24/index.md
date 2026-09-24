# 2026-09-24 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进走向分层、可执行的闭环体系**：从提出 B0–L5 自主性框架的 [79页综述提出RSI五级自主性分层架构](#条目79-rsi)，到群体协作与脚手架演化并行的 [SwarmWorld 与 ModularRSI：AI 自我进化的群体与个体路径](#条目swarmworld-modularrsi-ai)，RSI 研究正从概念讨论转向可比较的实现路径。
- **真实反馈成为自进化的关键驱动力**：[Simate以Physical RSI驱动机器人自主研究，登顶RoboDojo](#条目simate-physical-rsi-robodojo)将假设、真机实验和评测闭合，[Meta“组织第二大脑”智能体：结构化知识与自改进闭环](#条目meta)与 [Mind Lab推出自迭代后训练平台Mint Recursive](#条目mind-lab-mint-recursive)则分别以专家反馈和生产反馈持续更新知识或模型。
- **Jev 式快决策形成从模型到系统的完整路线**：4 项工作覆盖范式比较、端侧模型、分级评判和记忆控制，包括 [开源版 Jev：Laya 登顶 Hugging Face 热榜](#条目jev-laya-hugging-face)、[JEV-as-a-Judge：高置信接受、低置信升级的低成本评判](#条目jev-as-a-judge)与 [Jev-Mem：System-One 控制的高效智能体记忆架构](#条目jev-mem-system-one)。
- **评测与奖励开始刻画开放任务中的细粒度质量**：[The Tasteful Agent：衡量与提升长时程任务决策品味](#条目the-tasteful-agent)从真实轨迹自动构造决策分叉题，[RULER：面向 SVG 生成的实例感知量规奖励](#条目ruler-svg)则把实例级多维量规转化为可用于强化学习的评分信号。
- **基础模型与系统侧继续拓展效率和模态边界**：[Ovis-Embedding：统一文本、图像、视频与音频的全模态嵌入](#条目ovis-embedding)统一四类模态检索，[Flash-dLLM：IO 感知 KV 缓存与并行解码加速扩散语言模型](#条目flash-dllm-io-kv)提升扩散语言模型推理效率，[HyperQ：量子增强扩散语言模型的电路超网络](#条目hyperq)探索量子残差分支的参数高效适配。

## 对当前研究的启发
- **Awesome-RSI**：[79页综述提出RSI五级自主性分层架构](#条目79-rsi)的 B0–L5 分级可作为资源清单的统一标注轴，而 SwarmWorld、ModularRSI 与 Physical RSI 可补充群体、脚手架和物理闭环三类代表路线。
- **MemoryEvolve**：[Meta“组织第二大脑”智能体：结构化知识与自改进闭环](#条目meta)与 [Jev-Mem：System-One 控制的高效智能体记忆架构](#条目jev-mem-system-one)分别提供“专家反馈驱动知识演化”和“快模型控制写入、检索与停止”的两种可审计长期记忆方案。
- **ResearchEvolve**：[Simate以Physical RSI驱动机器人自主研究，登顶RoboDojo](#条目simate-physical-rsi-robodojo)表明可将真机实验结果直接纳入假设生成与研究策略更新，构造具身科研智能体的可验证自进化闭环。
- **SwarmEvolve**：[SwarmWorld 与 ModularRSI：AI 自我进化的群体与个体路径](#条目swarmworld-modularrsi-ai)可用于比较共享环境中的群体经验传播与单体模块演化，进而识别群体协作带来的独立增益。
- **HarnessEvolve**：[SwarmWorld 与 ModularRSI：AI 自我进化的群体与个体路径](#条目swarmworld-modularrsi-ai)中的 ModularRSI 将执行框架本身纳入演化对象，为量化 harness 改动对能力提升和排名变化的贡献提供了直接案例。
- **JevEvolve**：[JEV-as-a-Judge：高置信接受、低置信升级的低成本评判](#条目jev-as-a-judge)与 [Jev-Mem：System-One 控制的高效智能体记忆架构](#条目jev-mem-system-one)展示了可从评判置信度和记忆操作日志中持续学习快模型与慢模型的升级边界。
- **EvalEvolve**：[The Tasteful Agent：衡量与提升长时程任务决策品味](#条目the-tasteful-agent)以智能体轨迹中的真实决策分叉自动生成题目，可用于构建随新轨迹持续更新、且更贴近长程任务质量的动态评测。
- **EvolveLRM**：[Mind Lab推出自迭代后训练平台Mint Recursive](#条目mind-lab-mint-recursive)提供了以评测、数据、LoRA 后训练和生产反馈组成低成本迭代闭环的工程模板，而 [RULER](#条目ruler-svg)说明实例感知量规可进一步转化为开放任务的细粒度强化学习奖励。
- **LogicEvolve**：未打标签的 [Lean Pool：AI 维护的形式化数学档案库](#条目lean-pool-ai)可作为持续扩充且机器可验证的训练与评测来源，为逻辑自进化提供低歧义反馈和错误修复基础。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-24/  

