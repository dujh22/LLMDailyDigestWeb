# 2026-11-14 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- RSI 从概念验证走向完整系统栈：既有支持热插拔、版本化与回退的 [openJiuwen RSI 原生 AgentOS](#openjiuwen-rsi-agentos-agent)，也有将六智能体闭环用于预训练的 [No Second Run](#no-second-run-rsi-801-30b-a3b)，并出现 [Singularity-Bench](#singularity-bench) 与 [EGE](#ege) 这类能力评测和更新治理机制。
- 长程记忆与上下文管理转向“按决策效用优化”：从自动搜索记忆程序的 [MAPE](#mape)、以反事实边际贡献筛选记忆的 [MemCredit](#memcredit-web)，到可恢复上下文折叠的 [Folio](#folio) 和面向编码动作保持的 [CoACT](#coact-coding-agent)，共同兼顾成功率、证据保真与词元成本。
- Agent 训练进一步细化长轨迹信用分配：[行动者、评判者还是教师？](#item-11)表明弱行动模型可凭事后完整轨迹成为有效教师，[OPSD4MAS](#opsd4mas)则把未来通信转化为词元级信用，显著改善多智能体协作训练。
- 快决策模型的主线从单纯低延迟扩展到可靠路由与安全：[SO-Arena](#so-arena-system-one)揭示综合性能不等于决策可靠，[思考的价值](#item-22)学习何时升级到完整推理，[MobileProbe](#mobileprobe)则以轨迹感知注入检验移动智能体的环境攻击面。
- 物理与科研闭环开始获得更强的自动反馈：[PhysLoop](#physloop-llm)把物理知识转化为视频生成的筛选和修复信号，[梯度感知 CFD 智能体](#cfd)则直接借助可微求解器迭代发现湍流闭合模型。
- 热点延伸集中在世界模型、视觉压缩与渲染效率，包括 [BirdDreams](#birddreams-bev)、[G-STAR](#g-star-token)、[WorldDraft](#worlddraft-4d) 和 [TTB](#ttb)，但与当前核心研究方向的直接关联相对较弱。

## 对当前研究的启发
- **Awesome-RSI**：[openJiuwen RSI 原生 AgentOS](#openjiuwen-rsi-agentos-agent)、[Singularity-Bench](#singularity-bench) 与 [EGE](#ege)分别补齐了可回退自改写、端到端能力评测和更新采纳治理，可串成 RSI 系统的完整生命周期框架。
- **SystemEvolve**：[No Second Run](#no-second-run-rsi-801-30b-a3b)证明数据、训练配置与基础设施可纳入统一多智能体演化闭环，而 [EGE](#ege)提供了修改进入生产系统前的审计与灰度部署协议。
- **MemoryEvolve**：[MAPE](#mape)可用于自动搜索记忆程序，[MemCredit](#memcredit-web)可作为其中按真实决策增益评价单条记忆的目标函数。
- **Groom**：[CoACT](#coact-coding-agent)以“压缩后是否保持下一步动作”为准则，为过程级 token 利用评测提供了比语义相似度更贴近 Agent 成效的指标。
- **AgentTrainEvolve**：[行动者、评判者还是教师？](#item-11)提示可将低成功率模型保留为轨迹教师，[OPSD4MAS](#opsd4mas)则给出了把多智能体通信细化为词元级训练信用的方法。
- **JevEvolve**：[SO-Arena](#so-arena-system-one)说明快决策模型必须分开评估准确率、稳定性与拒答能力，而 [思考的价值](#item-22)可用于学习快决策升级慢推理的动态边界。
- **HarnessEvolve**：[MobileProbe](#mobileprobe)的轨迹感知注入与进化式载荷优化可直接扩展为 GUI Agent harness 的自适应安全测试模块。
- **CodeEvolve**：[CoReMem](#coremem)将记忆价值、来源信用和执行成本统一到连续仓库任务中，可用于构建能跨 issue 复用经验的编码 Agent。
- **PhysicalEvolve**：[PhysLoop](#physloop-llm)与[梯度感知 CFD 智能体](#cfd)分别展示了离散知识约束和连续物理梯度两类反馈，可组合为物理模型自进化的双重验证信号。
- **ResearchEvolve**：[梯度感知 CFD 智能体](#cfd)把可微求解器变成假设搜索的机器裁判，为自主科研建立了比语言评判器更可靠的实验闭环。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-14/  

