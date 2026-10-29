# 2026-10-29 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **模型发布更强调低成本执行与长程智能体能力**：OpenAI 的 [GPT-6.1 Terra](#openai-gpt-6-1-terra-astra) 以约旗舰十分之一的单 Token 成本逼近 Astra 的电脑操作能力，端侧、多模态和个人 Agent 模型也同步密集更新。
- **递归自我改进从单点优化走向“环境—评测—Harness—策略”闭环**：[The Trinity](#the-trinity) 以能力树和可验证环境驱动 Harness 演化，[RuHarness](#ruharness) 协同更新评判准则与脚手架，[Genie Master](#genie-master) 则在真实便利店中验证具身系统的失败诊断与持续改进。
- **智能体记忆与持续学习开始接受净收益检验**：[Memory Tax](#memory-tax) 发现复杂记忆系统常不及朴素 RAG，[CLE](#cle-llm) 揭示前沿智能体仍难长期积累经验，而 [TTME](#ttme) 展示了冻结权重、仅演化外部记忆的低成本科学发现路径。
- **训练数据与环境工程趋向可执行、可验证和可预测扩展**：[Trajectory2Gym](#trajectory2gym) 从决策依据出发合成交互轨迹，[SynthAPI](#item-58) 给出工具环境多样性与泛化能力的缩放规律，为课程生成和训练预算配置提供量化依据。
- **自动科研出现大规模形式化成果，但验证机制成为核心瓶颈**：[多智能体形式化有限单群分类定理](#ai-agent-24) 展示群体协作处理超长文献与 Lean 证明的规模潜力，[Principia](#principia) 推进测试时假设—原理闭环；与此同时，[Ai2 新颖性评判基准](#ai2-llm) 表明 LLM 科研裁判仍高度不稳定。
- **热点延伸**集中在主动式 AI 综述、世界一致视频生成、空间音频、长视频取证及空间 VLM 等方向，但相关性分为 0 或 1，暂不作为今日重点展开。

## 对当前研究的启发
- **Awesome-RSI**：[The Trinity](#the-trinity) 与 [RuHarness](#ruharness) 表明 RSI 应同时演化可验证环境、能力表征、评判准则和 Harness，而非只让模型反复自评与改写。
- **HarnessEvolve**：[TraceTrial-Bench](#tracetrial-bench) 的轨迹证据与机制链归因可用于区分底模失败和运行框架失败，[RuHarness](#ruharness) 则提供了让这一诊断结果直接驱动脚手架迭代的方法。
- **Groom**：[TraceTrial-Bench](#tracetrial-bench) 的多源证据和故障归因框架可扩展为过程级 Token 归因，将冗余搜索、错误恢复与有效进展对应到可审计轨迹。
- **MemoryEvolve**：[Memory Tax](#memory-tax) 提醒记忆方案必须报告相对原始历史检索的净收益，而 [TTME](#ttme) 说明在固定模型下持续更新外部记忆可能比测试时训练更高效。
- **AgentTrainEvolve**：[Trajectory2Gym](#trajectory2gym) 与 [SynthAPI](#item-58) 可分别用于提升轨迹中的决策依据质量、估计环境多样性带来的泛化收益，从而优化多轮工具智能体的数据配方。
- **EnvironmentEvolve**：[SynthAPI](#item-58) 给出的环境数据缩放规律提示，应将工具、任务和数据库多样性作为可控变量，而不只是盲目增加环境实例数量。
- **ResearchEvolve**：[Principia](#principia) 可作为“观察—假设—原理—修正”科研闭环模板，而 [Ai2 新颖性评判基准](#ai2-llm) 说明新颖性判断不能依赖单一 LLM 裁判。
- **LogicEvolve**：[多智能体形式化有限单群分类定理](#ai-agent-24) 显示 Lean 可把群体智能体的超大规模推理转化为机器可检验证据，但仍需检查自然语言论证与形式化代码是否语义一致。
- **InfraEvolve**：[ForgeKernel](#forgekernel) 在华为与英伟达榜单上的跨硬件结果说明，真实硬件反馈、正确性验证和迭代式代码生成已能形成可迁移的基础设施进化闭环。
- **HumanEvolve**：[Anthropic 专家决策实验](#anthropic-ai) 表明 AI 的预设立场会显著影响专家且难被自我察觉，因此人机协作界面应显式呈现建议来源、反方证据与影响审计。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-29/  

