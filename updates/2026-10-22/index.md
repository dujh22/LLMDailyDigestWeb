# 2026-10-22 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进走向模型—脚手架—任务协同闭环**：4 项代表工作分别探索“脑—身体”协同演化、从文献持续吸收算法、作品与能力共同迭代及低预算脚手架搜索，包括 [CoEvo-RSI：模型与测试框架协同演化](#coevo-rsi)、[ScholarEvolve：从科研文献中持续演化 Agent Harness](#scholarevolve-agent-harness)、[RSIGame：自主试玩、修复与迭代的游戏开发智能体](#rsigame) 和 [HGM-Dual：面向长程规划的谱系感知智能体脚手架优化](#hgm-dual)。
- **Agent 训练与评测进一步动态化、交互化**：[LongZero：零数据增强长上下文推理](#longzero)展示自生成任务驱动的零外部数据训练，[Environment Duels：LLM 环境创作与求解的协同演化评测](#environment-duels-llm)与[SWE-DIVE：动态用户模拟的多轮编程智能体评测](#swe-dive)则把环境创作、用户反馈和可执行验证纳入能力测量。
- **记忆与合成数据研究开始强调投入产出和长期稳定性**：[MemoryTax：智能体记忆的苦涩教训](#memorytax)质疑预构建记忆相对原始历史搜索的价值，[Uni-Mem：统一在线策略优化的长程智能体记忆管理器](#uni-mem)转向端到端学习写入与检索策略，[Dreaming Learning 缓解合成数据训练中的模型坍缩](#dreaming-learning)则从谱分析出发控制递归数据退化。
- **自主科研出现大规模并行与真实实验闭环**：[Claude 64小时生成31.8万种蝎毒结合蛋白方案](#claude-64-31-8)取得湿实验验证，[数千个 GPT‑Rosalind 智能体并行挖掘全脑 CRISPR 图谱](#gpt-rosalind-crispr)展示科研群体并行分析能力，[多智能体团队自主发现线性注意力架构](#item-86)进一步把持久化团队用于模型架构发现。
- **长程模型与低成本决策基础设施同步推进**：[阶跃星辰开放 Step 5 Preview 权重，面向长程 Agent](#step-5-preview-agent)以百万 token 上下文和端到端压缩训练支撑复杂执行，[Our Own Jev：单次前向传播的类型化决策与开放 LoRA 评判模型](#our-own-jev-lora)则提供可自托管的低延迟数据筛选与评判方案。

## 对当前研究的启发
- **Awesome-RSI**：[CoEvo-RSI](#coevo-rsi)表明 RSI 不应只优化模型或脚手架一侧，而应通过历史继承、检查点合并与轨迹微调共同控制能力和执行框架的迭代错配。
- **HarnessEvolve**：[ScholarEvolve](#scholarevolve-agent-harness)和[HGM-Dual](#hgm-dual)提供了两条可直接复用的 harness 演化路线，即从文献自动实现候选算法，以及利用谱系与错误条件生成减少评估预算。
- **AgentTrainEvolve**：[LongZero](#longzero)说明可由模型自主合成长上下文检索课程，[Uni-Mem](#uni-mem)则展示了用事件级信用分配联合训练记忆构建与检索策略的方法。
- **MemoryEvolve**：[MemoryTax](#memorytax)提示新记忆架构必须与“强模型直接工具搜索原始历史”进行成本—准确率对照，而[Uni-Mem](#uni-mem)支持将记忆操作从人工规则改为在线策略优化。
- **DataEvolve**：[Dreaming Learning](#dreaming-learning)给出了以高温自采样正则化维持递归合成数据多样性的机制，可作为数据飞轮防坍缩的候选控制器。
- **EvalEvolve**：[Environment Duels](#environment-duels-llm)和[SWE-DIVE](#swe-dive)说明动态评测可分别通过模型互创环境和动态用户模拟持续生成能力边界附近、可执行验证的新任务。
- **ResearchEvolve**：[Claude 蛋白设计](#claude-64-31-8)与[GPT‑Rosalind](#gpt-rosalind-crispr)表明自主科研系统应把候选规模化生成、并行分析和实验验证调度设计为同一闭环，而非只评估文本研究产出。
- **SwarmEvolve**：[多智能体团队自主发现线性注意力架构](#item-86)显示私有研究历史、异质角色与自适应实验资源分配可以共同支撑有限预算下的群体科学发现。
- **JevEvolve**：[Our Own Jev](#our-own-jev-lora)验证了从 logits 或隐藏状态单次前向读取类型化判断、再以 LoRA 自托管迭代的低成本评判路径。
- **NewModel**：[Step 5 Preview](#step-5-preview-agent)将百万 token、上下文压缩训练与可验证环境联合起来，为评估长程 Agent 模型是否真正获得持续执行能力提供了新样本。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-22/  

