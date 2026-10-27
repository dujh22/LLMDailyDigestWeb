# 2026-10-27 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从概念走向“可演化、可验证、可回滚”的工程体系：[Infinity Machine](#infinity-machine)展示科研脚手架自主演化，[AREX-2](#arex-2)探索长程反思训练，[RRSI](#rrsi)以留出集、泄漏筛查和成本约束抑制过拟合，而[编程智能体脚手架如何自我演化](#item-59)则表明自动改写并不天然有效。
- 长程智能体训练集中攻坚经验固化、信用分配与奖励可靠性：[ASCENT](#ascent)把单次成功轨迹在线蒸馏进快权重，[Outcome RL 的收益](#outcome-rl)指出强化学习主要提高完成率而非拓展能力边界，[有限强验证器预算下审计 GRPO](#grpo)则给出低成本抑制奖励作弊的方法。
- 数据与科研闭环进一步平台化：[LegoFlow](#legoflow)让编码智能体自主编排数据、训练和评测流水线，[Auto-Research Arena](#auto-research-arena)以统一环境和多目标指标检验自动研究发现能否真正改善预训练。
- 长期记忆与上下文优化开始关注“访问状态”和真实系统成本：[AMIE](#amie)通过轻量适应层持续演化记忆索引，[编码智能体上下文的物理成本](#item-67)则揭示删减上下文可能因前缀缓存失效反而增加计算与能耗。
- 新模型与快决策路线同步推进：[GPT-6.1 Terra](#openai-gpt-6-1-terra)强化电脑操作与写作，[Jeva](#nus-jeva)提出原生 System One 决策架构，但[Jev 风格结构的选择偏差研究](#jev-system-one)提醒整体准确率稳定不等于对选项重排鲁棒。
- 具身系统的重点由单模型能力转向控制层级选择：[EBench](#ebench)显示直接控制适合短程任务，调用 VLA/WAM 策略可降低词元成本并提升成功率，但策略选择与控制权切换仍是核心瓶颈。

## 对当前研究的启发
- **Awesome-RSI**：[Infinity Machine](#infinity-machine)、[RRSI](#rrsi)与负向实证共同说明，RSI 清单应把留出集验证、任务泄漏筛查、成本预算和改动回滚列为核心评判维度。
- **AgentTrainEvolve**：[ASCENT](#ascent)提供“成功轨迹验证后立即自蒸馏”的在线学习范式，而[GRPO 审计](#grpo)表明训练闭环还应按低通过率优先分配强验证器预算。
- **GeneralizeEvolve**：[Outcome RL 的收益](#outcome-rl)提示应将“既有能力可靠化”与“能力边界拓展”分开测量，避免把 pass@1 提升误判为真实泛化。
- **CodeEvolve**：[LegoFlow](#legoflow)可作为代码数据飞轮的编排底座，但[脚手架演化实证](#item-59)要求每次自动改动都配套持续验证、修订和淘汰机制。
- **ResearchEvolve**：[Auto-Research Arena](#auto-research-arena)提供了以发现能否复用于改善预训练为标准的外部效度评测，可补足只看论文产出或单次实验分数的不足。
- **MemoryEvolve**：[AMIE](#amie)表明无需重写记忆内容，也可通过独立演化访问状态实现持续个性化检索，适合作为现有记忆系统的低侵入适配层。
- **Groom**：[编码智能体上下文的物理成本](#item-67)说明过程级 token 评测应同时核算前缀缓存命中、重取、预填充计算与能耗，不能把上下文缩短直接等同于成本下降。
- **JevEvolve**：[Jeva](#nus-jeva)与其选择偏差反例共同提示，快决策模型除准确率、延迟外还必须加入候选置换不变性和答案缺席识别测试。
- **RobotEvolve**：[EBench](#ebench)表明具身 Agent 的演化对象应包含“直接控制还是调用专用策略”的路由器，以及不同控制层之间的可靠交接机制。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-27/  

