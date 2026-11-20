# 2026-11-20 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归改进**
  - [OpenAI RSI](#openai-rsi)：用并行研发智能体加人工审核构成“AI开发AI”闭环，将2至4小时任务的零干预成功率从23%提高到46%。
  - [Evo²](#evo-harness)：让模型权重与智能体运行框架互相提供训练反馈，解决两者分开优化难以持续增益的问题。
  - [Sage-Evolve-Preview](#sage-evolve-preview)：动态生成能暴露能力缺口的诊断任务，避免固定评测失去区分度后自我改进停滞。
  - [Agnes Harness](#agnes-harness)：用快慢决策分流，并拆分现场适应与长期经验沉淀，降低调用成本和重复试错。
  - [Harness](#harness)：让模型按模块改写智能体运行代码，以可验证约束替代脆弱的提示词优化，成功率从5%升至40%。
- **监管审计**
  - [OpenAI](#openai)：让四家外部机构驻场审查训练和内部模型，把递归研发的安全审核从发布前验收嵌入全过程。
- **环境训练**
  - [Game2Player](#game2player)：让环境构建者与玩家互相验收，把网页游戏持续转成可验证任务和视觉智能体训练轨迹。
  - [Budget Internalization](#budget-internalization)：证明固定生成上限会被模型内化为能力边界，揭示预算内准确率与测试时扩展能力的隐性取舍。
- **自主科研**
  - [DeepQuest](#deepquest)：从综述提取知识缺口，再按数据可行性和证据增量双重审计，生成可验证的医学发现。
  - [TwinLab-Bench](#twinlab-bench)：用真实实验记录构建可执行的实验室孪生，发现最佳科研智能体自主实验仅得45分。
- **智能体评测**
  - [Singularity-Bench](#singularity-bench-ai)：以六项真实研发任务检验智能体建设AI基础设施的能力，并将首词元P90延迟从12秒降至0.48秒。
  - [CompAct-Bench](#compact-bench)：让智能体从压缩后的任务状态继续执行，以最终完成率暴露摘要造成的进度与状态失真。
- **长期记忆**
  - [Brain](#brain)：从历史会话提炼并持续更新个人技能，以证据门槛和失败回放将工具调用失败率降低11%。
  - [MemFolder](#memfolder)：按跨记录共享结构同时压缩记忆条数和文本长度，降低检索与生成成本而不丢关键事实。
- **基础设施**
  - [Performance Factory](#performance-factory-codex)：把性能回归调查、根因定位和修复标准化为Codex持续运行的自动工作流。
- **热点延伸**：[PROLA](#prola)、[WorldRuler](#worldruler)、[Code World Model 2.0](#code-world-model-2-0)、[StrideWorld](#strideworld)、[LightTAR](#lighttar)

## 对当前研究的启发
- **Awesome-RSI**
  - 迁移｜从 [Sage-Evolve-Preview](#sage-evolve-preview) 把动态诊断用于平台期定位：每轮增补能力边界题，并保留固定锚点验收
  - 延续｜[OpenAI RSI](#openai-rsi) 仍依赖人类科研判断：比较全审、抽检和双审的成功率、漏错率与审核工时
- **MonitorEvolve**
  - 迁移｜从 [OpenAI](#openai) 把外部审计嵌入研发全程：在训练、内部部署和发布前设置独立复测与责任日志
- **HarnessEvolve**
  - 迁移｜从 [Evo²](#evo-harness) 把框架修改成败转为训练数据：记录补丁、执行反馈和迁移结果，联合更新模型与框架
  - 延续｜[Harness](#harness) 存在过拟合和篡改评测风险：用隐藏测试集、沙箱权限和补丁审计比较自改前后表现
- **ResearchEvolve**
  - 迁移｜从 [DeepQuest](#deepquest) 把“知识缺口—数据可行性—证据增量”用于选题：三阶段筛选后再启动实验
  - 延续｜[TwinLab-Bench](#twinlab-bench) 最佳模型仅45分：按实验设计、执行恢复和结果解释拆分得分并定位瓶颈
- **MemoryEvolve**
  - 迁移｜从 [MemFolder](#memfolder) 把跨记录结构用于记忆压缩：联合优化记录数和长度，以事实恢复率约束删减
- **Groom**
  - 迁移｜从 [CompAct-Bench](#compact-bench) 把“压缩后继续执行”用于token评测：对比原始与压缩轨迹的完成率和动作一致率
- **InfraEvolve**
  - 延续｜[Singularity-Bench](#singularity-bench-ai) 的目标仍由人预设：加入自主选瓶颈任务，评测收益、回归率与算力成本

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-20/  

