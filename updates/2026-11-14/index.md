# 2026-11-14 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从方法走向完整系统与治理： [openJiuwen RSI 原生 AgentOS](#openjiuwen-rsi-agentos-agent)支持能力热插拔、验证与回退，[No Second Run](#no-second-run-rsi-801-30b-a3b)把多智能体 RSI 闭环用于大模型预训练，[Singularity-Bench](#singularity-bench)与[EGE](#ege)则分别补上端到端评测和更新采纳治理。
- 长程智能体记忆转向“按决策效用管理预算”： [Folio](#folio)支持可恢复的多分辨率上下文折叠，[MemCredit](#memcredit-web)用反事实边际贡献筛选记忆，[MAPE](#mape)自动进化完整记忆程序，[CoACT](#coact-coding-agent)则以保持下一步动作为编程上下文压缩准则。
- Agent 训练进一步细化信用分配与经验利用：[行动者、评判者还是教师？](#item-11)表明弱行动模型仍可凭事后轨迹判断充当有效教师，[ACE-RL](#ace-rl)直接按交接经验对后续轨迹的增益联合训练行动、反思与策展能力。
- 快决策模型的效率、可靠性与安全形成完整议题：[思考的价值](#item-22)学习何时升级到完整推理，[SO-Arena](#so-arena-system-one)揭示综合性能与决策可靠性并不等价，[MobileProbe](#mobileprobe)进一步以进化式载荷评测移动智能体的环境注入风险。
- 物理与科研自进化继续强调可验证闭环：[PhysLoop](#physloop-llm)把 LLM 物理知识转化为视频模型的筛选、纠错和训练信号，另有可微 CFD 湍流模型发现、神经影像工作流评测及可验证奖励科研环境等多项进展。
- 热点延伸集中于生成式世界模型与视觉推理，包括[BirdDreams](#birddreams-bev)的驾驶视角—BEV 联合生成、[G-STAR](#g-star-token)的高压缩图像生成、[WorldDraft](#worlddraft-4d)的 4D 世界评测及[TTB](#ttb)的快速视图合成。

## 对当前研究的启发
- **Awesome-RSI**：openJiuwen 的可版本化回退、EGE 的独立审计与灰度采纳、Singularity-Bench 的奖励作弊防护可组合成“生成更新—验证增益—安全部署—失败回滚”的 RSI 基础闭环。
- **MemoryEvolve**：MemCredit 的反事实效用估计、Folio 的按需证据恢复与 MAPE 的程序进化表明，记忆优化应从语义相关性检索升级为固定预算下的决策效用最大化。
- **AgentEvolve**：ACE-RL 对经验交接实际增益的优化和 MAPE 对记忆程序的自动搜索，为冻结参数条件下持续筛选、重组并验证经验提供了直接机制。
- **AgentTrainEvolve**：事后轨迹教师与 OMA 的轨迹质量校准可分别改善长程任务中的动作级信用信号和长度偏置，适合纳入多轮 Agentic RL 训练管线。
- **Groom**：CoACT 以“是否保持下一步动作”衡量上下文价值，为过程级 token 归因提供了比压缩率或最终成功率更贴近 Agent 决策的评测指标。
- **JevEvolve**：思考价值路由、SO-Arena 的可靠性谱系和 S1-Evo 的证据竞争攻击共同提示，快决策模型必须联合优化升级策略、置信度校准与对抗稳健性。
- **PhysicalEvolve**：PhysLoop 展示了将物理知识具体化为样本筛选和局部修复信号的闭环，可迁移到由模拟或实验误差驱动的物理模型持续改进。
- **ResearchEvolve**：可微 CFD 的梯度反馈与对撞机环境的连续可验证奖励说明，科研智能体应优先进入反馈可机器判定、能支持稳定迭代的科学问题。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-14/  

