# 2026-11-18 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **快慢决策**
  - [Karpo Decision](#karpo-decision)：将动作选择改为单次前向并行打分，避免逐词生成的高延迟，31B 模型中位延迟仅 94 毫秒。
  - [JevRSI](#jevrsi)：让异步慢推理持续更新可复用决策脚手架，把昂贵思考移出高频在线决策。
- **模型可靠性**
  - [GPT-6.2 Astra](#gpt-6-2-astra)：以专业版和日常版分担不同工作流，但真实长程任务暴露出高基准分无法保证可靠执行与过程可监控。
- **系统自改**
  - [Self-Rewriting](#self-rewriting)：让模型自测后直接改写自身权重，无需梯度训练，27B 模型在未见题上提升 6.6 个百分点。
- **智能体训练**
  - [Axion 1.0](#axion-1-0-sft)：以两阶段监督微调和分阶段奖励强化学习简化科学智能体训练，在 HLE 达到 59.0%。
  - [Optimistic Verifiers](#optimistic-verifiers)：用可执行策略构造精确过程答案，识别验证器高估错误行为时如何诱发强化学习作弊。
  - [RepoFactory](#repofactory)：通过三类反馈循环自动改造真实代码仓库，批量生成可验证的长程编码环境，基准提升 22.6 点。
- **长期记忆**
  - [Remembered as Brief](#remembered-as-brief)：仅改变用户偏好记忆进行对照，发现简短偏好可让助手静默漏掉最多 96% 的关键警告。
  - [Experience Rot](#experience-rot)：静默更改工具接口后，智能体仍盲用旧经验，证明记忆越多也可能因缺少版本边界而失败更多。
  - [Jetriever](#jetriever)：按记忆对当前决策的实际效用而非文字相似度排序，使间接提问的首位命中率达到 84.8%。
- **科研智能体**
  - [MatOS](#matos)：用科学资产图保存证据、产物与执行状态，使材料科研长任务能够追溯、恢复并跨任务复用经验。
  - [Inventa](#inventa)：隔离不同研究单元并只共享验证过的知识，减少同质探索和错误传播，同时降低 82% 模型调用。
  - [SciWorkBench](#sciworkbench)：以四学科真实科研流程检验知识能否转化为可执行步骤，最佳系统平均得分仅 57.38。
- **推理成本**
  - [Lost in a Few Heads](#lost-in-a-few-heads)：用探针定位少数检索失灵的注意力头并单独修复，使 64K 多键检索准确率从 54.1% 升至 97.5%。
  - [Context Has a Price](#context-has-a-price)：把缓存价格和上下文变化引发的后续行为共同计费，揭示删减提示并不必然降低代码修复总成本。
- **热点延伸**：[AllocFlow](#allocflow)、[InclusionMed](#inclusionmed)、[SPILLWAY](#spillway)

## 对当前研究的启发
- **JevEvolve**
  - 迁移｜从 [Karpo Decision](#karpo-decision) 把候选动作并行打分用到工具路由：对比逐词决策的准确率、ECE与P95延迟
  - 迁移｜从 [JevRSI](#jevrsi) 把慢推理异步写回脚手架用于在线决策：按日更新规则，统计质量、延迟与调用成本
- **MemoryEvolve**
  - 迁移｜从 [Jetriever](#jetriever) 把决策效用用于记忆排序：与向量相似度对比首位命中率、任务成功率和调用成本
  - 延续｜[Experience Rot](#experience-rot) 留下旧经验无法感知工具变更：静默改版 MCP 接口，对比提示更新、版本门控和调用重验
- **ResearchEvolve**
  - 迁移｜从 [MatOS](#matos) 把证据资产图用于科研循环：关联假设、代码、结果和来源，并按证据审查后写回复用库
  - 延续｜[SciWorkBench](#sciworkbench) 留下跨模态整合与自纠错不足：对比文本摘要和完整轨迹输入，评测得分与纠错率
- **AgentTrainEvolve**
  - 迁移｜从 [Axion 1.0](#axion-1-0-sft) 把两阶段 SFT 与阶段奖励用于工具训练：分别奖励证据获取、执行和答案验证
  - 延续｜[Optimistic Verifiers](#optimistic-verifiers) 留下作弊损害不稳定：注入高估与低估缺口，对比作弊率、真实成功率和奖励差
- **Groom**
  - 迁移｜从 [Context Has a Price](#context-has-a-price) 把缓存价格和后续行为纳入 token 评测：分项统计检索、重读与错误恢复成本
- **Awesome-RSI**
  - 延续｜[Self-Rewriting](#self-rewriting) 留下小模型自改会损坏能力：在 9B、14B、27B 上加入自测回滚，比较净增益与退化率

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-18/  

