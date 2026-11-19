# 2026-11-19 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **稳定自改进**
  - [Resolution Hypothesis](#resolution-hypothesis)：用千万次调用的方差分析发现，智能体进化停滞常因评测噪声盖过真实改进。
  - [GUARD](#guard)：用“新改动造成的退化”约束脚手架更新，无需外部评分器也能持续改进并减少遗忘。
  - [自主自学习](#item-48)：冻结智能体仅凭游戏经验和文本笔记自行设计学习循环，持续提升并迁移能力。
- **训练信号**
  - [SEED](#seed)：把当前策略轨迹提炼成持续更新的技能监督，补足长程强化学习只有终局成败信号的问题。
  - [RSI-Prime](#rsi-prime)：只用轨迹中的高质量决策计算训练损失，避免模型把失败实验一并学会，整体性能提高31.95%。
- **记忆演化**
  - [MoE-Context](#moe-context)：按步骤选择可见历史块并复用缓存，避免智能体反复读取全部上下文，查找准确率升至119/120。
  - [ARISE](#arise)：将失败归因为细粒度记忆和通用规则，并经留出任务验收后写入，防止有害经验长期累积。
  - [OpenKAGE](#openkage)：用分层记忆和群体知识图谱记录技能及适用条件，使经验能跨智能体与模型迁移。
- **评测可信度**
  - [STEMBench](#stembench)：用学科公认指标和真实实验结果双重校准，评测智能体能否推进开放科学问题而非只会答题。
  - [RSIBench-Infra](#rsibench-infra)：以跨软件栈生产任务检验智能体能否把局部优化转化为质量不降的端到端加速。
  - [编程基准高分不等于实际产出](#item-49)：借助19天模型禁用实验发现，基准高11分并未显著增加真实代码合并产出。
- **可信工程**
  - [Codex 沙箱](#codex)：用宿主系统原生隔离、最小权限和逐命令提权，约束本地编程智能体的文件与网络访问。
  - [芯片PPA优化](#ppa)：把大模型重写RTL接入综合、仿真和形式验证闭环，使成熟芯片的功耗性能面积最高改善14%。
- **热点延伸**：[FastFrames](#fastframes)、[π⁴](#item-10)、[Breath-Dx](#breath-dx)

## 对当前研究的启发
- **Awesome-RSI**
  - 迁移｜从 [Resolution Hypothesis](#resolution-hypothesis) 把重复运行方差用于改进验收：按候选重跑并报告可检出最小增益
  - 延续｜[GUARD](#guard) 的非退化保证仅覆盖门控缓冲区：比较区内外连续编辑的收益、回退率与遗忘率
- **AgentTrainEvolve**
  - 迁移｜从 [SEED](#seed) 把事后技能重打分用于长程工具训练：比较终局奖励与技能稠密奖励的成功率和样本效率
  - 迁移｜从 [RSI-Prime](#rsi-prime) 把决策级损失掩码用于实验轨迹训练：仅监督经执行验证有效的规划与操作
- **MemoryEvolve**
  - 延续｜[MoE-Context](#moe-context) 的上下文选择器难以跨任务迁移：跨任务训练选择器并评测召回率、成本与成功率
  - 迁移｜从 [ARISE](#arise) 把留出集验收用于记忆写入：候选记忆仅在独立任务提分且无回归时固化
- **AutonomousAgentEvolve**
  - 延续｜[自主自学习](#item-48) 尚未验证现实任务：在常驻桌面任务中对比固定流程与自建循环的长期成功率和回滚率
- **EvalEvolve**
  - 迁移｜从 [编程基准高分不等于实际产出](#item-49) 把真实交付纳入评测：同步记录基准分、PR合并率和周交付量
  - 迁移｜从 [STEMBench](#stembench) 把领域指标与实测结果双锚定用于科研评测：分别报告科学增益与工程增益
- **InfraEvolve**
  - 延续｜[RSIBench-Infra](#rsibench-infra) 难把局部加速变成全链路收益：记录算子、引擎和服务三级吞吐及质量回归

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-19/  

