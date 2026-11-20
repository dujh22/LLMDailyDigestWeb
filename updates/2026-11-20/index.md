# 2026-11-20 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归改进**
  - [OpenAI RSI](#openai-rsi)：用并行研发智能体与人工审核组成“AI开发AI”闭环，将2至4小时任务的零干预成功率从23%提至46%。
  - [Evo²](#evo-harness)：让模型权重与智能体执行框架互相生成训练反馈，解决两条自我改进路线彼此割裂的问题。
  - [OpenAI](#openai)：把四家外部机构驻场嵌入训练与内部部署审查，解决发布前一次性验收无法持续监管AI研发的问题。
- **智能体评测**
  - [MultiAgentBench](#multiagentbench)：用统一环境分别测量智能体间协作与竞争，避免用单体任务成绩代替群体互动能力。
- **数据与训练**
  - [LogT](#logt)：自动合成视觉落地且逻辑一致的工具调用轨迹，解决视觉模型不会可靠放大搜索的问题，训练成本降低超120倍。
  - [HINT-WAM](#hint-wam)：把示范中的未来视频作为训练期教师，在策略自身轨迹上提供稠密动作监督，无需奖励或模拟器交互。
  - [CurvDelta](#curvdelta)：把通用能力保持写成低曲率参数更新约束，减少模型学习新知识或定向遗忘时的能力损伤。
- **多模态模型**
  - [Jeveration](#jeveration)：用所有图像位置共享的随机状态协调并行预测，使单次前向生成兼顾全局一致性与多样性，512×512图像耗时78毫秒。
  - [ALIVE](#alive)：联合学习何时回应、沉默或追问反馈，解决流式视频模型只能被动理解画面、难以持续配合用户的问题。
- **热点延伸**：[PROLA](#prola)、[LightTAR](#lighttar)、[WorldRuler](#worldruler)、[Code World Model 2.0](#code-world-model-2-0)

## 对当前研究的启发
- **Awesome-RSI**
  - 迁移｜从 [OpenAI RSI](#openai-rsi) 把零干预成功率用于闭环评测：按任务时长分桶，统计无人接管完成率与人工返工率。
- **ResearchEvolve**
  - 迁移｜从 [OpenAI RSI](#openai-rsi) 把“单例执行—人工审核—批量扩展”用于自动实验：先验收一例的假设、代码与结果再并行复制。
- **MonitorEvolve**
  - 迁移｜从 [OpenAI](#openai) 把外部评估驻场用于研发监管：在训练、内部部署和发布前设置独立审计记录与强制复测门槛。
- **SystemEvolve**
  - 迁移｜从 [Evo²](#evo-harness) 把框架编辑成败转为模型训练数据：交替搜索工作流、回灌执行轨迹并更新框架编辑器。
- **HarnessEvolve**
  - 延续｜[Evo²](#evo-harness) 留下跨任务迁移不稳定且统计证据不足：在全量SWE-bench上对比静态框架，报告迁移增益、置信区间与p值。
- **SwarmEvolve**
  - 迁移｜从 [MultiAgentBench](#multiagentbench) 把互动质量用于群体评测：固定单体模型，改变通信拓扑并测协作收益、冲突率与消息成本。
- **DataEvolve**
  - 迁移｜从 [LogT](#logt) 把逻辑链约束用于视觉轨迹合成：过滤目标未落地或调用顺序矛盾的样本，再测工具成功率与数据效率。
- **RobotEvolve**
  - 迁移｜从 [HINT-WAM](#hint-wam) 把未来观测教师用于策略后训练：仅训练时提供示范后续帧，对比行为克隆的真机成功率与分布偏移。
- **GeneralizeEvolve**
  - 迁移｜从 [CurvDelta](#curvdelta) 把低曲率更新约束用于持续学习：同预算对比LoRA，测新任务增益、旧任务遗忘率与通用能力保持率。
- **NewModel**
  - 迁移｜从 [ALIVE](#alive) 把回应、沉默和追问建模为联合动作：构造连续视频任务，对比被动模型的完成率、打扰率与追问时机误差。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-20/  

