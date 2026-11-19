# 2026-11-19 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **自我改进**
  - [GUARD](#guard)：用“新版本比旧版本多犯了什么错”约束工作流修改，避免智能体改进新任务时破坏已有能力。
  - [RSI-Prime](#rsi-prime)：只用实验轨迹中的高质量决策训练模型自主开展后训练，整体性能相对提升31.95%。
  - [ARISE](#arise)：将失败归因写成分层记忆，并经留出任务验收后才固化，避免错误经验持续污染企业智能体。

- **训练反馈**
  - [SEED](#seed)：从当前策略的完整轨迹提炼可更新技能，把任务最终成败转成每一步都可学习的监督信号。

- **记忆管理**
  - [MoE-Context](#moe-context)：按步骤选择可见的历史块而非永久删除信息，使长程查找准确率从93/120升至119/120。
  - [OpenKAGE](#openkage)：用带适用条件的分层知识和群体共享图谱，让不同智能体及不同模型复用开放世界技能。

- **评测可信**
  - [Resolution Hypothesis](#resolution-hypothesis)：以千万次调用的方差分析证明，评测噪声会掩盖真实改进并阻断智能体持续进化。
  - [STEMBench](#stembench)：用学科公认指标和真实实验结果双重锚定，评测智能体是否真正推进博士后级科学问题。
  - [编程基准高分不等于实际产出](#item-49)：借助19天模型禁用实验发现，基准高11分并未显著增加真实代码合并产出。

- **环境与基建**
  - [CrossEnv](#crossenv)：用实体与工具关系图连接多个服务，自动合成状态一致、可执行且可验证的长程训练任务。
  - [RSIBench-Infra](#rsibench-infra)：以跨引擎、内核和指令层的生产任务，检验基础设施智能体能否把局部优化变成端到端加速。
  - [Codex 沙箱](#codex)：利用宿主系统原生隔离、网络代理和逐命令提权，让本地编程智能体安全执行真实开发命令。

- **物理闭环**
  - [RoboBuilder](#robobuilder)：把实机失败视频同时反馈给仿真器和机器人设计流程，消除72%的中低难度现实失败。

- **成本审计**
  - [软件热力学](#item-47)：把词元区分为推动任务改动的“功”和无效耗散的“热”，发现成功运行约80%的词元未改变目标状态。

- **热点延伸**：[FastFrames](#fastframes)、[π⁴](#item-10)、[Breath-Dx](#breath-dx)

## 对当前研究的启发
- **AgentEvolve**
  - 迁移｜从 [ARISE](#arise) 把“留出任务验收后才固化”用于记忆写入：比较直接写入与验收写入的长期成功率和退化率
  - 延续｜[GUARD](#guard) 留下非退化保证仅覆盖门控缓冲区：扩大任务分布，对比无门控版本并统计旧能力回退率

- **AgentTrainEvolve**
  - 迁移｜从 [SEED](#seed) 把事后技能重打分用于长程工具训练：与终局奖励对比每步信用质量、成功率和样本效率

- **EvalEvolve**
  - 迁移｜从 [Resolution Hypothesis](#resolution-hypothesis) 把重复运行方差用于候选筛选：报告最小可检测增益和误选率
  - 迁移｜从 [编程基准高分不等于实际产出](#item-49) 把真实PR合并率用于模型选型：检验基准分与周交付量的因果关联

- **ResearchEvolve**
  - 迁移｜从 [STEMBench](#stembench) 把领域指标与实测结果双锚定用于科研评测：分别报告科学增益和工程优化增益

- **EnvironmentEvolve**
  - 迁移｜从 [CrossEnv](#crossenv) 把实体—工具图用于跨服务任务合成：检查可执行率、验证覆盖率和状态一致性

- **InfraEvolve**
  - 延续｜[RSIBench-Infra](#rsibench-infra) 留下局部加速难转化为端到端收益：按算子、引擎、服务三级复测吞吐与质量

- **Groom**
  - 迁移｜从 [软件热力学](#item-47) 把“是否改变任务状态”用于词元归因：按规划、工具、恢复统计有效功占比

- **RobotEvolve**
  - 延续｜[RoboBuilder](#robobuilder) 留下高难障碍与实机泛化不足：跨机器人和障碍复测成功率、修复轮数与仿真实机差距

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-19/  

