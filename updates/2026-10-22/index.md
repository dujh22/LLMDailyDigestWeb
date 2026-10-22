# 2026-10-22 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从单体反思走向“模型—脚手架—开放环境”协同演化：[ScholarEvolve](#scholarevolve-agent-harness) 从文献中持续组合 Agent Harness，[CoEvo-RSI](#coevo-rsi) 处理模型与执行框架的“脑—身体”错配，[DeepEvolve](#deepevolve) 则把可验证的未来预测环境纳入长期演化闭环。
- 长程 Agent 的模型与训练基础设施同步推进：[阶跃星辰开放 Step 5 Preview 权重，面向长程 Agent](#step-5-preview-agent) 提供百万 token 上下文与端到端压缩训练，[FlashNext-RL](#flashnext-rl) 将单节点 Agentic RL 扩展至 131K 上下文，[HGM-Dual](#hgm-dual) 以谱系和错误条件化降低脚手架搜索成本。
- 动态、交互式评测成为主线：[Environment Duels](#environment-duels-llm) 让模型互相创作和求解环境，[SWE-DIVE](#swe-dive) 用动态用户与可执行测试评估多轮编程，而 [BRA](#bra) 进一步因果量化计算、信息和反馈各自对失败恢复的价值。
- 记忆研究同时出现“端到端学习”与“是否需要预构建记忆”的路线分歧：[Uni-Mem](#uni-mem) 联合优化长期记忆写入和检索，[MemoryTax](#memorytax) 则发现强模型直接搜索原始历史可能具有更优的成本—准确率表现。
- 自主科研与群体智能开始产生可验证成果：[数千个 GPT‑Rosalind 智能体并行挖掘全脑 CRISPR 图谱](#gpt-rosalind-crispr) 展示近两千智能体的并行假设发现，[多智能体团队自主发现线性注意力架构](#item-86) 则把持久化科研团队用于模型架构创新。
- 热点延伸仅有两项：产业侧关注 [Novix 招募 RSI、Agentic RL 与新架构研究人才](#novix-rsi-agentic-rl)，生成模型侧探索 [扩散模型的纠错训练](#item-16)，但与今日核心研究主线的直接关联较弱。

## 对当前研究的启发
- **Awesome-RSI**：[CoEvo-RSI](#coevo-rsi) 表明 RSI 评测不能只追踪模型能力，还应同步记录脚手架版本、历史继承和检查点合并带来的协同或错配。
- **AgentEvolve**：[DeepEvolve](#deepevolve) 可借鉴为“开放世界事件—可验证结果—技能蒸馏”闭环，使推理时经验积累不再局限于固定任务集。
- **HarnessEvolve**：[ScholarEvolve](#scholarevolve-agent-harness) 与 [HGM-Dual](#hgm-dual) 分别提供文献驱动候选生成和谱系感知低预算筛选，可组合成持续演化 Harness 的生成—评估管线。
- **AgentTrainEvolve**：[FlashNext-RL](#flashnext-rl) 给出了超长上下文软件工程 Agent 训练的单节点实现路径，可直接参考其架构定制与显存治理方案。
- **EnvironmentEvolve**：[Environment Duels](#environment-duels-llm) 将环境创作能力与任务求解能力放入同一对抗循环，可用于检验环境难度是否真正随策略能力共同增长。
- **MemoryEvolve**：[MemoryTax](#memorytax) 与 [Uni-Mem](#uni-mem) 提示应把“原始历史搜索”设为强基线，并仅在端到端学习的写入、检索策略取得净成本收益时引入结构化记忆。
- **JevEvolve**：[Our Own Jev](#our-own-jev-lora) 证明单次前向传播的自托管 LoRA 评判器可用于低成本数据筛选，适合进一步研究快决策模型与慢推理模型的升级边界。
- **Groom**：[BRA](#bra) 的因果资源归因显示任务规格信息往往比追加计算或测试反馈更有价值，可转化为 Harness 内不同 token 类型的边际效用度量。
- **ResearchEvolve**：[数千个 GPT‑Rosalind 智能体并行挖掘全脑 CRISPR 图谱](#gpt-rosalind-crispr) 与 [多智能体团队自主发现线性注意力架构](#item-86) 说明科研群体应同时具备私有研究历史、并行分工和面向实验价值的资源调度机制。
- **TaskEvolve**：[RSIGame](#rsigame) 的局部试玩修复闭环与全局质量控制可直接用于设计“作品持续变好”与“开发能力持续变强”的双层验收指标。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-22/  

