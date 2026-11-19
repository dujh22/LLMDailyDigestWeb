# 2026-11-19 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **研发效能**
  - [研究加速报告：量化智能体研发效能](#item-15)：用内部任务日志衡量真实研发加速，发现编码智能体在2至4小时任务上的自主成功率已达46%。
- **训练进化**
  - [SEED](#seed)：从当前策略的完整轨迹提炼技能并重标步骤奖励，解决长程强化学习只有最终成败信号的问题。
  - [RSI-Prime](#rsi-prime)：只用实验轨迹中的高质量决策训练模型，避免自主后训练把失败操作一并学入参数。
  - [WATERFALL](#waterfall)：仅凭视觉轨迹开展进化锦标赛，在没有任务描述和真实奖励时自动发现长程任务奖励。
- **记忆演化**
  - [MoE-Context](#moe-context)：按步骤隐藏无关历史块而不删除内容，使长程智能体兼顾低缓存成本、失败回滚与准确检索。
  - [OpenKAGE](#openkage)：用记录适用条件的分层记忆和群体知识图谱，让开放世界智能体持续共享并迁移技能。
- **科研智能体**
  - [automodel](#automodel)：把专家的模型发现流程封装成可移植技能，使通用编程智能体能跨学科提出并改进模型。
  - [STEMBench](#stembench)：以学科公认指标和真实实验结果双重锚定，解决开放科学任务无法用答题正确率可靠评测的问题。
- **递归改进**
  - [GUARD](#guard)：用方向性后悔区分新修改造成的退化与旧错误，使脚手架无需外部评分器也能稳定演化。
  - [AeroRSI](#aerorsi)：让无人机续飞检验自身修复是否有效，以闭环结果生成监督，成功率从46.4%升至67.5%。
  - [Safe Personal RSI](#safe-personal-rsi)：把提示自改进当作可回滚的软件更新，以重复安全测试阻止泄露信息或越权的新版本上线。
- **持续个性化**
  - [Learning through Discernment](#learning-through-discernment)：先用冻结判断器识别用户是否明确反馈真实结果，再更新端侧模型，避免错误轨迹造成持续退化。
- **可信执行**
  - [SCAFFOLD](#scaffold)：用可撤销授权和证据迁移规则，判断环境或版本变化后旧技能的成功证据是否仍可信。
- **决策效率**
  - [AnyS1](#anys1)：把程序技能编译成通用决策点，由4B模型处理常规选择、低置信时回退大模型，成本降低75%至91%。
  - [软件热力学：热功分解编码成本](#item-47)：按是否真正改变任务状态拆分词元成本，发现成功轨迹约80%的词元未推动目标改动。
- **热点延伸**：[FastFrames](#fastframes)、[π⁴](#item-10)、[Breath-Dx](#breath-dx)

## 对当前研究的启发
- **AgentTrainEvolve**
  - 迁移｜从 [SEED](#seed) 把“轨迹后验技能重打分”用于长程工具RL：每轮提炼技能并重标步骤奖励，与结果奖励联合训练。
- **AgentEvolve**
  - 迁移｜从 [GUARD](#guard) 把方向性后悔用于记忆和工作流更新：逐项回放新旧版本，只保留不破坏已掌握任务的修改。
- **CacheEvolve**
  - 延续｜[MoE-Context](#moe-context) 的选择器跨任务失效：在任务A训练后冻结测试任务B，对比专用选择器的准确率与KV占用。
- **ResearchEvolve**
  - 迁移｜从 [automodel](#automodel) 把模型发现流程封装为技能：让同一编码智能体搜索方程和神经架构，对比领域专用流水线。
  - 迁移｜从 [STEMBench](#stembench) 把领域指标和实测结果用于科研评测：同时报告科学增益、工程增益及与真实实验的差距。
- **Awesome-RSI**
  - 迁移｜从 [RSI-Prime](#rsi-prime) 把决策级损失掩码用于自主后训练：仅训练被验证为优质的实验选择，屏蔽失败操作。
  - 延续｜[Safe Personal RSI](#safe-personal-rsi) 仅验证提示更新：扩展到技能与工具修改，对比回滚前后成功率、越权率和泄露率。
- **PersonalEvolve**
  - 延续｜[Learning through Discernment](#learning-through-discernment) 依赖干净反馈：控制反馈稀缺度和偏斜度，测污染率、遗忘与能力收窄。
- **Groom**
  - 迁移｜从 [软件热力学：热功分解编码成本](#item-47) 把状态改动视为有效功：按轨迹差分归因词元并报告每千词元有效改动数。
- **JevEvolve**
  - 迁移｜从 [AnyS1](#anys1) 把技能编译成决策点：由快模型处理高置信选择，按成功率—成本曲线校准慢模型回退阈值。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-19/  

