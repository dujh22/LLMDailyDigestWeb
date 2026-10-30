# 2026-10-30 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从概念验证走向可审计系统：[RSI-Master](#rsi-master) 以动态研究 DAG 驱动自主后训练，[RSI Arena](#rsi-arena) 则揭示人类偏好提升未必同步改善能力与安全，[CMU开源Hermit](#cmu-hermit-harness-rsi) 进一步将持续改进能力外置到统一 Harness 层。
- 环境演化成为 Agent 与机器人训练的关键扩展路径：[WorkRover](#workrover) 用执行反馈递归修复长程协同环境并细化信用分配，[Gym-Anything](#gym-anything) 通过创建—审计闭环规模化生成机器人仿真。
- 推理模型训练集中攻克自主数据、探索与过程监督：[LongZero](#longzero) 实现零外部数据的长上下文任务合成，[PSN-RLVR](#psn-rlvr) 以轨迹一致的参数扰动恢复探索能力，多项工作还分别改进教师纠正、分层奖励与置信度对齐。
- 具身智能进一步转向真实规模的经验共享与持续学习：[群体经验学习 CEL](#cel) 在96台机器人上验证跨个体经验复用，[CausGround](#causground) 则将交互经验提炼为无需更新参数即可迁移的因果动作知识。
- 自主科研同时推进“发现能力”与“质量验证”：[MoLRSI](#molrsi) 将工作流、架构和持久记忆纳入分子发现的递归改进，[协作式 AI 智能体自主开展固态量子自旋实验研究](#item-32) 展示了多智能体通过反驳实验发现并修正测量漂移的闭环。
- 模型与系统侧出现开放权重旗舰、扩散 Agent 模型及缓存量化等进展，其中[Mistral Large 4](#mistral-1t-large-4) 开放1T参数多模态权重；热点延伸则集中在流式音视频分离、全向视频生成、指令容量与模型安全评估。

## 对当前研究的启发
- **Awesome-RSI**：RSI-Master 的可审计实验 DAG 与 RSI Arena 的偏好—能力—安全错位表明，RSI 基准必须同时记录改进过程、资源约束和多维退化，而不能只看单一最终得分。
- **HarnessEvolve**：Hermit 的外置 Adapter 与 KARMA 的可验证、可回滚原子知识编辑说明，冻结模型后仍可把 Harness 设计成统一且可持续演化的能力层。
- **EnvironmentEvolve**：WorkRover 的执行反馈修复和 Gym-Anything 的对抗式创建—审计闭环，可直接用于建立“生成、运行、验错、修复、验收”的自动环境生产线。
- **AgentTrainEvolve**：WorkRover 将终端奖励归因到具体回合、ZEST-Search 让任务提出者与求解器协同演化，为长程 Agentic RL 的信用分配和零标签课程生成提供了可组合方案。
- **EvolveLRM**：PSN-RLVR、PIVOT 与 H²R 分别从探索、在线纠正和分层中间奖励入手，可组合成兼顾解法多样性与密集学习信号的 RLVR 配方。
- **RobotEvolve**：CEL 的96台真机异步经验共享与 Gym-Anything 的规模化仿真生成，为构建“群体采集—失败检索—仿真扩增—真机回灌”的具身数据飞轮提供了直接路径。
- **EvalEvolve**：EnvOS 的前后环境审计、VeriCUA 的动态取证及前缀可执行性协议共同表明，动态 Agent 评测应把环境变化、过程失效和评分器错误分开归因。
- **Groom**：前缀可执行性与 EnvOS 的证据复核可用于把 token 消耗映射到有效推进、错误恢复和无效重复，并以可审计证据替代 Agent 自述。
- **ResearchEvolve**：量子自旋实验中的相互审查与反驳性实验，以及 MoLRSI 的真实实验验证，说明科研智能体应把异常检测、反证实验和外部实证设为闭环中的强制关卡。
- **MemoryEvolve**：Google“睡眠”框架的清醒期采集与睡眠期巩固，以及 CORAL 的自主检查点和上下文重置，为长期记忆的写入、压缩与参数化巩固提供了双时间尺度设计。
- **DataEvolve**：合成数据预预训练的计算量对齐负结果说明，数据自进化必须以等算力自然数据基线衡量真实边际收益，并联合优化验证阈值、噪声与训练阶段。
- **CacheEvolve**：低比特 GDN 的梯度感知精度分配和 dLLM-KVQ 的轨迹感知校准表明，缓存压缩策略需要针对状态随时间或去噪步骤演化的误差结构进行自适应管理。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-30/  

