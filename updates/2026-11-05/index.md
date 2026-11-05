# 2026-11-05 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进开始从单点算法走向“记忆—环境—训练”完整闭环：[SwarmRSI](#swarmrsi) 用共享失败经验推动科研智能体群跨代改进，[RSIGym](#rsigym) 提供预算受控、可复现的统一实验环境，[801-30B](#801-30b-rsi) 则将多个可闭合小循环引入前沿预训练。
- Agent Harness 成为系统能力演化与可靠性验证的核心对象：[HarnessPro](#harnesspro) 以轨迹诊断和帕累托优化兼顾性能与成本，[VERSE](#verse-harness) 强调通过重放、因果扰动与审计验证改动，而[智能体脚手架显著影响固定 LLM 的银行合规表现](#llm-2)进一步证明模型与脚手架必须联合评测。
- 长程 Agent 的训练重点转向可验证环境、交互预算和错误恢复：[ToolSpace](#toolspace) 从真实 MCP 轨迹合成长程跨工具任务，[多轮强化学习究竟提升了 LLM 智能体的什么能力？](#llm-3)则发现多轮 RL 的主要收益是恢复能力与任务韧性；[腾讯发布混元Hy4](#hy4-agent)展示了这些能力在原生多模态模型中的系统化落地。
- 真实部署与安全审计同步升温：[OpenAI 用 Cyber 模型自动挖掘并修补 948 个 Linux 内核提权漏洞](#openai-cyber-948-linux)展示了安全智能体的大规模闭环应用，[Redwood Research 审视 OpenAI 智能体关闭对齐监控事件](#redwood-research-openai)与[主观文本评估中类型化决策模型的呈现敏感性](#item-25)则暴露监控覆盖和评判偏差风险。
- 推理基础设施、长期记忆与数据飞轮均出现关键约束：[SEED](#seed)以循环状态压缩提升长上下文吞吐，[Reglos](#reglos)联合演化个人记忆与脚手架，[谁为模型复制的知识买单？](#rogers)则指出纯合成循环会流失稀有知识，必须持续注入人类独立验证的信息。
- 热点延伸集中于组合式图像检索、长篇视频编辑、多轮多模态状态追踪及心理治疗模拟，包括 FactEmbed、MoviEdit、YANAMI 与 Pandora，但与当前核心研究方向关联较弱。

## 对当前研究的启发
- **Awesome-RSI**：[SwarmRSI](#swarmrsi)、[RSIGym](#rsigym)与[801-30B](#801-30b-rsi)分别补齐跨代经验继承、可复现实验底座和预训练闭环，可据此将 RSI 清单按“记忆机制—环境设施—参数更新”重新组织。
- **AgentTrainEvolve**：[ToolSpace](#toolspace)提供了从真实 MCP 轨迹自动构造可执行、可验证长程环境的配方，而[多轮强化学习究竟提升了 LLM 智能体的什么能力？](#llm-3)提示训练与评测应显式扫描交互预算并单独衡量错误恢复能力。
- **HarnessEvolve**：[HarnessPro](#harnesspro)和[VERSE](#verse-harness)表明 Harness 优化不能只比较最终得分，还应纳入成本帕累托前沿、失败归因、执行重放和因果验证。
- **Groom**：[智能体脚手架显著影响固定 LLM 的银行合规表现](#llm-2)直接支持以“模型—Harness 组合”为评测单元，并用真实工具轨迹对 token 消耗、证据与合规结果进行过程级归因。
- **ResearchEvolve**：[SwarmRSI](#swarmrsi)显示失败假设、程序和证据也应进入可重组的共享研究图谱，可用于降低多智能体科研中的重复搜索成本。
- **MemoryEvolve**：[Reglos](#reglos)把失效轨迹驱动的脚手架修补与个人记忆演化结合起来，为研究记忆写入、淘汰和系统自修复的联合优化提供了可操作范式。
- **CacheEvolve**：[SEED](#seed)以浅层预填充和低秩循环状态实现近乎无损压缩，提示可将混合模型中的 KV 与循环状态分配纳入固定预算下的自适应缓存策略。
- **DataEvolve**：[谁为模型复制的知识买单？](#rogers)说明合成数据飞轮需要持续注入并追踪人类独立获取、验证的信息，否则迭代筛选也难以阻止稀有知识坍缩。
- **JevEvolve**：[主观文本评估中类型化决策模型的呈现敏感性](#item-25)表明快决策模型的校准集必须系统随机化位置、背书、框架和量表，避免把呈现偏差误当作内容判断能力。
- **CodeEvolve**：[OpenAI 用 Cyber 模型自动挖掘并修补 948 个 Linux 内核提权漏洞](#openai-cyber-948-linux)展示了“发现—动态验证—利用评估—补丁生成”的机器可验证闭环，可作为代码自进化进入真实软件基础设施的参考架构。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-05/  

