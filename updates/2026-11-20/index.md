# 2026-11-20 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **研发闭环**
  - [OpenAI RSI](#openai-rsi)：以智能体试做、人类审核再并行扩展形成“AI 开发 AI”闭环，将中长任务零干预成功率从 23% 提至 46%。
  - [OpenAI](#openai)：让四家外部机构驻场审查训练与内部模型，把高风险 AI 监督从发布验收前移到研发全过程。
- **协同演化**
  - [Evo²](#evo-harness)：把智能体脚手架的执行成败回灌模型训练，同时搜索新脚手架，解决权重与系统框架各自优化的问题。
  - [Game2Player](#game2player)：让环境构建者与玩家互相验收，把网页游戏自动转成可验证任务和视觉智能体训练轨迹。
- **评测与泛化**
  - [MultiAgentBench](#multiagentbench)：用统一环境分别测试协作与竞争，解决单体任务分数无法衡量智能体互动质量的问题。
  - [CurvDelta](#curvdelta)：把能力保持限制写入低曲率参数更新空间，减少模型学习新知识或定向遗忘时的通用能力损失。
- **训练数据**
  - [HINT-WAM](#hint-wam)：用示范中的未来视频指导策略自身轨迹，无需奖励或模拟器交互即可获得稠密动作监督。
  - [LogT](#logt)：自动合成视觉位置准确、逻辑连贯的工具调用轨迹，使模型学会按需放大搜索图像，训练成本降低超 120 倍。
- **热点延伸**：[PROLA](#prola)、[LightTAR](#lighttar)、[WorldRuler](#worldruler)、[Code World Model 2.0](#code-world-model-2-0)

## 对当前研究的启发
- **MonitorEvolve**
  - 迁移｜从 [OpenAI](#openai) 把外部机构驻场审计用于研发监管：覆盖训练、内部部署与发布复测，记录发现、修复和放行责任。
- **Awesome-RSI**
  - 迁移｜从 [OpenAI RSI](#openai-rsi) 把“单例执行—人审纠错—并行扩展”用于 RSI 实验：持续统计零干预成功率与人工接管率。
- **SystemEvolve**
  - 迁移｜从 [Evo²](#evo-harness) 把脚手架编辑成败转为训练数据：交替更新模型权重与工作流，并保留跨任务有效修改。
  - 延续｜[Evo²](#evo-harness) 的跨任务优势尚不稳定：对比仅训权重、仅改脚手架与协同进化，报告全量任务迁移率和置信区间。
- **EnvironmentEvolve**
  - 迁移｜从 [Game2Player](#game2player) 把玩家执行同时用于环境验收和轨迹采集：按完成进度筛选任务，再回灌有效操作。
- **DataEvolve**
  - 迁移｜从 [LogT](#logt) 把视觉落地与逻辑一致性用于轨迹筛选：自动剔除放大区域错误或调用链矛盾的合成样本。
- **RobotEvolve**
  - 迁移｜从 [HINT-WAM](#hint-wam) 把未来观测作为训练期教师：在策略自身状态上蒸馏动作分布，以真机成功率检验收益。
- **SwarmEvolve**
  - 迁移｜从 [MultiAgentBench](#multiagentbench) 把互动质量设为独立指标：固定单体模型，对比通信拓扑的协作收益与竞争鲁棒性。
- **GeneralizeEvolve**
  - 迁移｜从 [CurvDelta](#curvdelta) 把能力保持编码进更新空间：对比普通 LoRA，测新任务增益、旧任务遗忘率与参数成本。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-20/  

