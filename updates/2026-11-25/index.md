# 2026-11-25 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **可信自改进**
  - [Online Environment Repair](#online-environment-repair)：训练中异步修补被策略利用的验证漏洞，把奖励作弊率从36.9%降至0.06%。
  - [Detection Gap](#detection-gap)：从正常运行轨迹学习故障监控器，补上自改进智能体能修复却发现不了自身故障的盲区。
  - [DoppelVet](#doppelvet)：用证据完全匹配的对照更新回放行为，在没有安全标签时拦截有害记忆和技能。
  - [SELFWRITE](#selfwrite)：让模型编程生成并递归合并自身的低秩权重修改，无需梯度即可持续提升数学能力。
- **评测闭环**
  - [RecurSciBench](#recurscibench-rsi)：用可执行、科学可验证的独立任务，检验科研智能体自我改进能否迁移到新任务和新领域。
  - [Transport-Safe Evaluation](#transport-safe-evaluation)：按各智能体的轨迹分布随机审计裁判，避免复用统一错误率造成排名偏差。
- **经验演化**
  - [ReHarness](#reharness)：根据任务结果反向修正实际调用过的历史经验，使经验库能在长期使用中持续纠错。
  - [VISE](#vise)：直接分析工具源码和执行轨迹修订技能说明，无需任务验证器也能提升成功率9.14至13.35个百分点。
  - [E2L](#e2l)：按经验产生的梯度是否与目标更新一致来筛选训练材料，排除解题有效却妨碍参数学习的经验。
- **训练信号**
  - [RLVB](#rlvb)：用真实答案后验奖励取证与提交时机，减少长任务中证据不足的提前猜答，准确率提升17.1%。
- **具身数据**
  - [RoboUniverse-10K](#robouniverse-10k)：把真实操作视频自动转成万级可验证仿真任务，同时隔离评分逻辑以抑制背题和奖励作弊。
  - [RynnVLA-Latent](#rynnvla-latent)：用三维几何约束的潜在动作把3.01万小时无控制标签视频转成机器人预训练监督。
- **执行效率**
  - [JevAgentHarness](#jevagentharness-jev)：用专用快速模型选择有限动作，只把内容生成交给昂贵模型，成本最多降低49.6%。
  - [LoomKV](#loomkv-kv)：以逐注意力头的3位编码无损压缩跨GPU、内存和SSD的KV缓存，扩大长请求服务容量。
- **常驻运行**
  - [Wactorz](#wactorz)：以演员级故障隔离和状态保持迁移，让边缘智能体自修复时无需中断整个长期任务。
- **热点延伸**：[ViDecide](#videcide)

## 对当前研究的启发
- **Awesome-RSI**
  - 迁移｜从 [DoppelVet](#doppelvet) 把“证据等价对照回放”用于更新准入：比较候选与对照行为后再持久化。
  - 延续｜[Detection Gap](#detection-gap) 留下故障发现能力未被单独评测：注入可修复故障，统计发现率、误报率和修复率。
- **AgentEvolve**
  - 迁移｜从 [ReHarness](#reharness) 把结果反向修正用于经验库：仅更新本次检索项，并保留原轨迹供复核。
- **AgentTrainEvolve**
  - 迁移｜从 [Online Environment Repair](#online-environment-repair) 把异步环境修补接入训练：监测异常高奖励并三重验证后热更新。
  - 迁移｜从 [RLVB](#rlvb) 把后验置信度用于提交奖励：分别奖励有效取证、延迟猜答和证据充分后作答。
- **EvalEvolve**
  - 迁移｜从 [RecurSciBench](#recurscibench-rsi) 把独立迁移评测用于RSI：分报源任务、新任务、新领域增益与局部退化。
  - 延续｜[Transport-Safe Evaluation](#transport-safe-evaluation) 留下轨迹覆盖不足问题：逐系统分层抽样，报告置信区间与不可识别界。
- **RobotEvolve**
  - 延续｜[RynnVLA-Latent](#rynnvla-latent) 依赖估计几何与真机示教：对比几何噪声强度，测迁移成功率和示教需求量。
- **JevEvolve**
  - 迁移｜从 [JevAgentHarness](#jevagentharness-jev) 把有限动作快路由用于工具选择：以轨迹长度、总成本和成功率联合训练。
- **AutonomousAgentEvolve**
  - 迁移｜从 [Wactorz](#wactorz) 把演员级隔离用于常驻Agent：分别持久化状态与代码，故障时只重启责任演员。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-25/  

