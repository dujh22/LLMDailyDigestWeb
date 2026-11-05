# 2026-11-05 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进开始覆盖“基座训练—实验设施—部署期演化”全栈：[801-30B](#801-30b-rsi)将共享生产记忆引入前沿预训练，[RSIGym](#rsigym)提供可复现、预算受控的真实训练环境，[Reglos](#reglos)则把记忆演化与脚手架修补结合起来。
- Agent Harness 成为系统自进化的核心对象：[HarnessPro](#harnesspro)以轨迹诊断和帕累托优化兼顾效果与成本，[VERSE](#verse-harness)进一步用重放、因果扰动和审计验证每次改动是否可靠。
- 长程 Agent 的模型与训练环境同步升级：[ToolSpace](#toolspace)从真实 MCP 轨迹合成可验证的跨工具任务，[混元 Hy4](#hy4-agent)则通过自检、执行验证和专项训练增强视觉操作与跨应用执行。
- 自主科研与高价值真实应用形成闭环：[SwarmRSI](#swarmrsi)让科研智能体群跨代共享失败经验，[EnzymeRSI](#enzymersi)接入云实验室构建酶工程干湿闭环，[OpenAI Cyber](#openai-cyber-948-linux)已将自动发现、验证和修补推进到 Linux 内核漏洞实战。
- 评测与安全审计转向“模型—脚手架—轨迹”整体：[智能体脚手架显著影响固定 LLM 的银行合规表现](#llm-2)证明 Harness 会改变合规结论，[主观文本评估中类型化决策模型的呈现敏感性](#item-25)揭示决策器的非内容偏差，[Redwood Research 的审视](#redwood-research-openai)则暴露对齐监控召回率和升级流程缺口。
- 效率与数据质量方面，[SEED](#seed)以浅层预填充和循环状态压缩提升混合模型吞吐，[Rogers 悖论下的模型坍缩](#rogers)强调持续注入经人类独立验证的新信息；热点延伸另集中在多模态状态追踪、组合图像检索、长视频编辑与医疗模拟。

## 对当前研究的启发
- **Awesome-RSI**：[RSIGym](#rsigym)可作为预算约束下复现长期 RSI 迭代的统一底座，而 [Redwood Research 的审视](#redwood-research-openai)提示必须同步记录监控召回率、人工复核和升级处置。
- **AgentEvolve**：[Reglos](#reglos)表明可用失效轨迹驱动记忆更新与 Harness 修补，并以独立评判抑制部署期自进化对基准的过拟合。
- **AgentTrainEvolve**：[ToolSpace](#toolspace)提供了从真实 MCP 执行轨迹规模化生成“可执行、可验证、可组合”长程 RL 环境的直接方案。
- **HarnessEvolve**：[HarnessPro](#harnesspro)与 [VERSE](#verse-harness)可组合为“性能—成本多目标搜索＋因果验证与审计”的 Harness 演化流程。
- **ResearchEvolve**：[SwarmRSI](#swarmrsi)的共享研究图谱适合沉淀跨 Agent、跨代的失败证据，而 [EnzymeRSI](#enzymersi)展示了将这种演化接入真实实验反馈的方法。
- **Groom**：[智能体脚手架显著影响固定 LLM 的银行合规表现](#llm-2)支持把模型—Harness 组合作为评测单元，并从真实工具轨迹归因 token 消耗与合规失效。
- **JevEvolve**：[主观文本评估中类型化决策模型的呈现敏感性](#item-25)说明快决策器训练与评测需随机化位置、背书和量表，并单独报告内容不变时的校准漂移。
- **DataEvolve**：[Rogers 悖论下的模型坍缩](#rogers)提示数据飞轮必须持续引入人类独立获取和验证的稀有信息，不能只依赖模型生成数据闭环。
- **CacheEvolve**：[SEED](#seed)证明混合架构可通过浅层编码与低秩循环状态压缩，在近乎无损条件下降低长上下文记忆成本。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-05/  

