# 2026-11-14 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- RSI 从方法探索走向完整系统与治理闭环：[openJiuwen发布RSI原生AgentOS，支持Agent持续自我扩展](#openjiuwen-rsi-agentos-agent)实现扩展的生成、验证、热插拔与回退，[No Second Run：预训练RSI炼出801-30B-A3B模型](#no-second-run-rsi-801-30b-a3b)把闭环推进至大模型预训练，[自主智能体自生成更新的证据治理采纳框架 EGE](#ege)则补上持久更新的审计与灰度机制。
- 自进化信号进一步深入数据、经验与物理一致性：[PhysLoop：以 LLM 物理认知驱动视频生成模型自我改进](#physloop-llm)把生成、筛选和纠错转化为训练数据，[ACE-RL：基于经验交接强化学习的递归自我改进](#ace-rl)直接优化经验对后续轨迹的真实增益。
- 长程智能体的核心转向“按决策价值管理上下文”：编程场景的[CoReMem：面向连续编程任务的成本内化记忆框架](#coremem)、Web 场景的[MemCredit：以决策效用优化长程 Web 智能体记忆](#memcredit-web)和可恢复折叠的[Folio：面向长程智能体的可恢复多分辨率上下文折叠](#folio)分别推进记忆估值、反事实信用与证据恢复；[CoACT：面向 Coding Agent 的动作保持式上下文压缩](#coact-coding-agent)则以“是否保持下一步动作”衡量压缩质量。
- 快决策模型同时推进效率、评测与攻防：[思考的价值：混合决策模型学习何时推理](#item-22)学习何时升级到完整推理，[SO-Arena：System One 模型能力谱系与决策可靠性基准](#so-arena-system-one)揭示综合性能与可靠性并不等价，[S1-Evo：面向类型化 System-1 决策模型的证据竞争攻击](#s1-evo-system-1)进一步暴露路由、审核和授权决策的可操纵性。
- Agent 训练与自动科研继续细化可验证反馈：[OMA：控制多轮智能体强化学习中的长度依赖轨迹影响](#oma)校正轨迹长度偏置，[OPSD4MAS：将多智能体通信转化为词元级信用](#opsd4mas)分配通信信用，[梯度感知智能体通过可微 CFD 自主发现湍流模型](#cfd)则展示了语言模型搜索与可微物理求解器结合的科研闭环；热点延伸主要集中于驾驶世界模型、图像 Token 压缩、4D 视频评测和视图合成加速。

## 对当前研究的启发
- **Awesome-RSI**：openJiuwen、No Second Run 与 EGE 分别提供可回退自扩展、预训练级闭环和证据化更新采纳机制，可据此完善 RSI 清单中“提出修改—验证增益—安全持久化”的完整技术谱系。
- **SystemEvolve**：openJiuwen 的版本化热插拔扩展与 EGE 的冻结、独立审计和灰度部署，可直接作为自修改 AgentOS 的运行时架构和变更治理模板。
- **MemoryEvolve**：CoReMem 与 MemCredit 表明记忆应按未来决策增益而非语义相似度估值，Folio 则提供压缩后按需恢复原始证据的工程实现路径。
- **Groom**：CoACT 将“压缩后下一步动作是否保持”设为过程级 Token 效用准则，可用于补充 Groom 对编码 Agent 上下文消费的可审计归因指标。
- **JevEvolve**：思考价值路由、SO-Arena 的可靠性分解和 S1-Evo 的证据竞争攻击共同指出，快决策模型需要联合优化升级阈值、置信度校准与对抗鲁棒性。
- **AgentTrainEvolve**：OMA 的源轨迹质量校准与 OPSD4MAS 的词元级通信信用，为长程、多智能体 RL 中消除长度偏置和定位有效协作信号提供了可直接复用的目标设计。
- **DataEvolve**：PhysLoop 将物理知识通过筛选与纠错蒸馏为细粒度训练数据，为构建具备外部约束、可迭代验收的数据飞轮提供了具体范式。
- **ResearchEvolve**：可微 CFD 工作展示了让多智能体负责离散假设搜索、让科学求解器提供连续梯度反馈的组合，可扩展为其他可微仿真领域的自主发现框架。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-14/  

