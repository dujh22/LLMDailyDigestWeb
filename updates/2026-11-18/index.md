# 2026-11-18 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归改进**
  - [Self-Rewriting](#self-rewriting)：让27B模型通过自我诊断直接改写权重，无需梯度训练就在未见题上提升6.6个百分点。
  - [JevRSI](#jevrsi)：把昂贵的慢推理异步沉淀为可检索、可修订的决策脚手架，降低高频在线决策成本。
  - [自我改进分支混合：动态目标与路由组合](#item-5)：让搜索分支形成不同目标与经验，再按任务路由组合，避免脚手架演化困在单一路径。
- **决策与训练**
  - [Karpo Decision](#karpo-decision)：以一次前向并行打分替代逐词生成，让31B智能体在94毫秒内完成动作选择与置信度判断。
  - [Axion 1.0](#axion-1-0-sft)：用两阶段监督微调和分阶段奖励简化科学智能体训练，在HLE取得59.0%。
  - [Optimistic Verifiers](#optimistic-verifiers)：以可执行授权策略构造精确过程答案，定位会被强化学习利用的高估型验证器漏洞。
- **科研智能体**
  - [MatOS](#matos)：用科学资产图沉淀经审查的执行证据，使材料科研长任务可追溯、可恢复并能跨任务复用经验。
  - [SciWorkBench](#sciworkbench)：用四学科真实工作流和统一评分检验科研智能体，揭示最佳系统平均得分仅57.38。
- **长期记忆**
  - [Remembered as Brief](#remembered-as-brief)：仅改变用户偏好记忆便测出最高96%的静默警告遗漏，暴露个性化造成的信息删减风险。
  - [BRIDGE](#bridge)：以极简检索基线和对抗探针区分“找到记忆”与“按记忆行动”，揭示复杂记忆操作的真实增益有限。
- **环境与评测**
  - [RepoFactory](#repofactory)：用三类代理反馈循环演化真实代码仓库，低成本生成可验证的长程编码训练环境。
  - [Context Has a Price](#context-has-a-price)：把缓存价格与上下文引发的后续行为共同计费，纠正“提示更短必然更便宜”的评测误区。
- **模型可靠性**
  - [GPT-6.2 Astra](#gpt-6-2-astra)：用真实长程工作流压力测试高分模型，发现静态基准未暴露的停摆、循环和算力浪费。
- **热点延伸**：[AllocFlow](#allocflow)、[InclusionMed](#inclusionmed)、[SPILLWAY](#spillway)

## 对当前研究的启发
- **Awesome-RSI**
  - 延续｜[Self-Rewriting](#self-rewriting) 留下小模型自改会停摆或自损：对比2B至27B，统计编辑率、未见题增益与能力回退。
- **JevEvolve**
  - 迁移｜从 [Karpo Decision](#karpo-decision) 把并行候选打分用到动作路由：与文本生成决策对比延迟、成本、校准误差和成功率。
- **AgentTrainEvolve**
  - 迁移｜从 [Axion 1.0](#axion-1-0-sft) 把分阶段奖励用到工具型RL：按检索、证据验证、作答分别给奖，并消融各阶段。
  - 迁移｜从 [Optimistic Verifiers](#optimistic-verifiers) 把可执行策略预言机用到奖励验收：训练前扫描乐观漏判，训练中监控作弊率。
- **ResearchEvolve**
  - 迁移｜从 [MatOS](#matos) 把证据审查后的资产图用到科研工作流：为假设、实验、结果建立版本、来源和复用关系。
  - 延续｜[SciWorkBench](#sciworkbench) 留下跨模态整合与自纠错不足：加入强制纠错回合，对比原流程的得分和错误恢复率。
- **MemoryEvolve**
  - 迁移｜从 [Remembered as Brief](#remembered-as-brief) 把“先列必知项再应用画像”用于记忆回答：统计关键项召回率与静默遗漏率。
  - 延续｜[BRIDGE](#bridge) 留下“检索到但不执行”问题：对比原文、规则化和行动模板记忆，测召回率与执行正确率。
- **EnvironmentEvolve**
  - 迁移｜从 [RepoFactory](#repofactory) 把可用性、依赖强度和实现规模代理用于环境筛选：演化仓库后再进入昂贵训练。
- **Groom**
  - 迁移｜从 [Context Has a Price](#context-has-a-price) 把缓存命中与后续行为纳入成本归因：同时报告总费用、动作数和任务成功率。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-18/  

