# 2026-11-20 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **研发闭环**
  - [OpenAI RSI](#openai-rsi)：并行研发智能体配合人类审核与批量扩展，将2至4小时任务的零干预成功率从23%提升至46%。
  - [Evo²](#evo-harness)：让模型权重与智能体脚手架互相提供训练反馈，解决二者分开优化难以形成持续改进闭环的问题。
- **过程监管**
  - [OpenAI](#openai)：让四家外部机构驻场审查训练与内部模型，把安全监管从发布前验收嵌入AI辅助研发全过程。
- **环境与数据**
  - [Game2Player](#game2player)：让环境构建者与玩家共同迭代，把网页游戏自动转成可验证任务和可规模化训练轨迹。
  - [LogT](#logt)：用逻辑一致的视觉搜索轨迹自动合成微调数据，使模型学会何时放大图像并将训练成本降低超120倍。
- **持续学习**
  - [CurvDelta](#curvdelta)：把能力保持限制写进低曲率参数更新空间，减少模型学习新知识或定向遗忘时的通用能力损失。
- **具身训练**
  - [HINT-WAM](#hint-wam)：以示范中的未来视频作为训练期教师，在策略自身轨迹上提供无需奖励和模拟器交互的稠密动作监督。
- **群体评测**
  - [MultiAgentBench](#multiagentbench)：以统一环境分别衡量智能体间的协作与竞争，避免用单体任务成绩代替群体互动能力。
- **热点延伸**：[PROLA](#prola)、[LightTAR](#lighttar)、[WorldRuler](#worldruler)、[Code World Model 2.0](#code-world-model-2-0)、[StrideWorld](#strideworld)

## 对当前研究的启发
- **Awesome-RSI**
  - 迁移｜从 [OpenAI RSI](#openai-rsi) 把“单例执行—人审修正—批量扩展”用于RSI闭环：按任务时长统计零干预成功率与人工接管率
- **MonitorEvolve**
  - 迁移｜从 [OpenAI](#openai) 把外部驻场审计用于模型研发监管：覆盖训练、内部部署和发布复测，记录告警、干预与缺陷闭环
- **SystemEvolve**
  - 迁移｜从 [Evo²](#evo-harness) 把脚手架编辑成败转为训练数据：交替更新模型权重与Harness，并保留跨任务有效改动
  - 延续｜[Evo²](#evo-harness) 留下跨任务收益不稳定且显著性不足：多种子比较权重单改、Harness单改与联合进化
- **AgentTrainEvolve**
  - 迁移｜从 [Game2Player](#game2player) 把玩家执行轨迹用于训练：按任务进度加权有效步骤，并与普通SFT比较长程成功率
- **EnvironmentEvolve**
  - 迁移｜从 [Game2Player](#game2player) 把“生成环境—试玩验收—回收轨迹”用于环境生产：以可执行率、可验证率和难度覆盖率筛选
- **DataEvolve**
  - 迁移｜从 [LogT](#logt) 把逻辑一致性检查用于视觉工具轨迹合成：过滤目标未落地或调用顺序矛盾的数据后再微调
- **EvolveLLM**
  - 迁移｜从 [CurvDelta](#curvdelta) 把低曲率更新用于持续学习：对比LoRA与CurvLoRA的新能力增益、旧能力保持率和遗忘率
- **RobotEvolve**
  - 迁移｜从 [HINT-WAM](#hint-wam) 把未来观测作为训练期教师：在策略自采样状态上蒸馏动作分布，评测成功率与分布偏移
- **SwarmEvolve**
  - 迁移｜从 [MultiAgentBench](#multiagentbench) 把协作与竞争拆成独立指标：比较通信拓扑时同时报告团队收益、个体收益与协调成本

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-20/  

