# 2026-10-29 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **新模型与个人智能体加速落地**：OpenAI 推出低成本电脑操作模型 [GPT-6.1 Terra](#openai-gpt-6-1-terra-astra)，蚂蚁开源面向长程个人任务的 [Ling-3.1-flash-1019](#personal-agent-ling-3-1-flash-1019)，超衍智能则以 [Apex-35B-V1.0](#35b-apex-35b-v1-0) 展示 AI 参与训练实验与成果回用的模型自进化路线。
- **递归与系统级自进化从概念走向可验证闭环**：[The Trinity](#the-trinity) 协同演化环境、能力树与 Harness，[Evo²](#evo) 在冻结模型时搜索工作流及演化策略，[ForgeKernel](#forgekernel) 则以跨硬件榜单成绩证明自动生成和优化基础设施的实用性。
- **持续学习与记忆进入“净收益”检验阶段**：[DeepMind 的连续任务研究](#deepmind) 与 [CLE](#cle-llm) 均揭示现有智能体的遗忘和经验复用瓶颈，[Memory Tax](#memory-tax) 进一步发现复杂记忆系统未必优于朴素 RAG，而 [TTME](#ttme) 展示了低成本外部记忆演化的可行替代路线。
- **Agent 训练、编排与运行评测同步演进**：[Trajectory2Gym](#trajectory2gym) 合成决策驱动的工具交互，[DynaFlow](#dynaflow) 学习任务自适应的多智能体工作流，[TraceTrial-Bench](#tracetrial-bench) 则把评测推进到运行框架故障归因与轨迹审计层面。
- **自主科研开始强化机制发现能力**：[Principia](#principia) 在测试时循环形成并修正因果假设和科学原理，与记忆演化路线共同指向无需频繁更新参数的闭环科学发现系统。
- **热点延伸**主要覆盖主动式 AI 框架、空间音视频生成、长视频取证与空间 VLM 等多模态方向，反映连续交互和时空一致性仍是当日外围热点。

## 对当前研究的启发
- **Awesome-RSI**：[The Trinity](#the-trinity) 将环境生成、能力刻画和 Harness 演化纳入同一闭环，可作为判定 RSI 是否真正改进“改进机制本身”的代表案例。
- **AgentEvolve**：[TTME](#ttme) 证明冻结权重、只演化外部记忆也能持续提升科学任务表现，可直接补充推理时经验积累与免训练自进化路线。
- **MemoryEvolve**：[Memory Tax](#memory-tax) 与 [HABIT-Bench](#habit-bench) 表明记忆研究应同时测量相对原始历史检索的净收益，以及跨数百次会话归纳弱证据习惯的能力。
- **GeneralizeEvolve**：[DeepMind 的连续任务研究](#deepmind) 和 [CLE](#cle-llm) 提供了从跨任务干扰、遗忘及经验迁移角度区分真实持续学习与局部适配的评测框架。
- **HarnessEvolve**：[Evo²](#evo) 展示了冻结执行器后联合搜索工作流与演化策略的方法，可用于研究 Harness 改进能否跨任务持续迁移。
- **Groom**：[TraceTrial-Bench](#tracetrial-bench) 的轨迹、多源证据与机制链归因可直接借鉴到过程级 token 利用评测，定位成本消耗与失败机制。
- **AgentTrainEvolve**：[Trajectory2Gym](#trajectory2gym) 以组合依赖覆盖和决策依据充分性合成交互，为多轮工具调用训练提供了比表层轨迹模仿更有针对性的数据构造准则。
- **SystemEvolve**：[DynaFlow](#dynaflow) 将工作流合成纳入主智能体动作空间，说明系统架构可以作为在线决策对象，而不必预先固定为人工设计的图。
- **InfraEvolve**：[ForgeKernel](#forgekernel) 在华为与英伟达硬件上的共同领先证明，真实硬件反馈能够支撑跨平台算子生成、验证与择优保留的进化闭环。
- **ResearchEvolve**：[Principia](#principia) 的“观察—因果假设—原理—修正”循环可为自主科研系统增加显式机制模型，避免仅靠试错搜索实验结果。
- **PersonalEvolve**：[Ling-3.1-flash-1019](#personal-agent-ling-3-1-flash-1019) 与 [HABIT-Bench](#habit-bench) 分别提供个人智能体底座和长期弱证据画像评测，可用于构建“部署—积累习惯—验证个性化收益”的闭环。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-29/  

