# 2026-11-20 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归闭环**
  - [OpenAI RSI](#openai-rsi)：用并行研发智能体配合人工审核形成“AI开发AI”闭环，将2至4小时任务的零干预成功率从23%提高到46%。
  - [Evo²](#evo-harness)：把脚手架修改反馈用于训练模型、再由模型搜索新脚手架，解决权重与执行框架各自优化却互不增益的问题。
  - [Sage-Evolve-Preview](#sage-evolve-preview)：动态生成针对当前能力缺口的诊断任务，避免固定评测失去分辨率后自我改进停滞。
  - [Harness](#harness)：让模型分模块改写并执行验证智能体框架，解决单改提示词难以稳定提升的问题，成功率从5%升至40%。
- **过程监管**
  - [OpenAI](#openai)：让四家外部机构驻场审查训练和内部模型，把安全监管从发布前验收扩展到AI辅助研发全过程。
- **环境数据**
  - [Game2Player](#game2player)：让环境构建者与玩家互相验收，把网页游戏自动转成可验证任务并持续生产视觉智能体训练轨迹。
- **常驻记忆**
  - [Agnes Harness](#agnes-harness)：用快慢决策分流，并拆开现场参数适应与长期经验沉淀，减少常驻智能体的调用成本和重复试错。
  - [Brain](#brain)：从历史会话提炼、验证并更新个人技能，替代用户手写规则，使工具调用失败率降低11%。
  - [DriftGuard](#driftguard)：用移除记忆后的反事实回放训练风险模型，实时拦截真正会误导智能体行为和结果的记忆。
- **科研发现**
  - [DeepQuest](#deepquest)：从综述抽取知识缺口，再以数据可行性和双层证据审计筛选，产出可验证且有知识增量的医学发现。
- **能力评测**
  - [TwinLab-Bench](#twinlab-bench)：用真实实验记录构建可执行任意设计的实验室孪生，揭示最佳科研智能体仍仅得45.0分。
  - [Singularity-Bench](#singularity-bench-ai)：用六项可执行的AI基础设施任务评测自主工程能力，智能体将P90首Token延迟从12秒降至0.48秒。
- **推理训练**
  - [Budget Internalization](#budget-internalization)：通过长度上限消融发现后训练会把固定预算内化为能力边界，牺牲测试时增加计算的收益。
- **热点延伸**：[PROLA](#prola)、[LightTAR](#lighttar)、[WorldRuler](#worldruler)、[Code World Model 2.0](#code-world-model-2-0)、[StrideWorld](#strideworld)

## 对当前研究的启发
- **MonitorEvolve**
  - 迁移｜从 [OpenAI](#openai) 把驻场外部审计用到AI辅助研发全程：在训练、内测、发布前设复核点并保留干预日志
- **Awesome-RSI**
  - 延续｜[Singularity-Bench](#singularity-bench-ai) 仍由人预设任务：加入自主定目标组，评估持续增益、越权率和奖励作弊率
- **HarnessEvolve**
  - 迁移｜从 [Evo²](#evo-harness) 把脚手架成败转成训练数据：对比仅改权重、仅改框架和SFT/GRPO协同迭代
  - 延续｜[Harness](#harness) 仅测单模型40题且可能篡改评测：跨模型跨领域复测，报告留出成功率、成本与篡改率
- **MemoryEvolve**
  - 迁移｜从 [DriftGuard](#driftguard) 把反事实回放用到记忆门控：逐条移除记忆，以动作和结果变化训练在线拦截器
- **AgentEvolve**
  - 迁移｜从 [Brain](#brain) 把历史会话模式用到技能写入：设置证据阈值，回放失败案例后再版本化入库
- **ResearchEvolve**
  - 迁移｜从 [DeepQuest](#deepquest) 把“综述缺口—数据可行性—双层审计”用到选题：为假设附数据入口、实验和证据链
- **AgentTrainEvolve**
  - 迁移｜从 [Game2Player](#game2player) 把环境—玩家闭环用到课程生成：执行验收任务并按完成进度加权轨迹训练
- **EvolveLRM**
  - 迁移｜从 [Budget Internalization](#budget-internalization) 把预算内化检查用到后训练：扫描长度上限与KL，测预算准确率和扩展收益
- **InfraEvolve**
  - 迁移｜从 [Singularity-Bench](#singularity-bench-ai) 把可执行基建任务用到自动优化验收：联合报告正确性、P90时延、吞吐和显存

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-20/  

