# 2026-11-17 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归改进**
  - [Post-Training RSI](#post-training-rsi)：把数据、奖励、验证器、搜索策略都纳入递归优化，避免自提升退化为反复训练模型权重。
  - [Terminal-RSI](#terminal-rsi)：交替固化已验证行为与精炼策略，把零散修复汇聚成完整任务成功，宏平均成功率提升29.90个百分点。
- **脚手架演化**
  - [HarnessDev](#harnessdev)：让智能体从种子框架自主创建并迭代执行系统，补上固定脚手架无法检验自进化与泛化的问题。
  - [HARNESS-ZERO](#harness-zero)：用审核智能体把专用脚手架的纠正蒸馏进模型，移除脚手架后成功率仍从23.3%升至44.3%。
  - [Harness-of-Harness](#harness-of-harness)：以规划、开发、独立测试和版本证据闭环维持多轮软件开发，三轮平均相对提升52.25%。
  - [RiseHarness](#riseharness)：对照成功与失败轨迹持续修改执行流程，提升长程终端任务重复运行时的稳定性。
- **经验与记忆**
  - [SkillMaster](#skillmaster)：按技能对后续任务的实际贡献决定创建、修订和保留，让智能体自主维护可复用技能库。
  - [ReHarness](#reharness)：用新轨迹反向修订导致当前决策的旧反思，使智能体适应分布变化而不只追加记忆。
  - [DeLoop](#deloop)：从重复动作及其后续恢复动作自动生成偏好数据，无需人工标注即可训练智能体减少空转。
  - [MEM-SQL](#mem-sql)：分层保存并按需复用已验证查询，避免每次从头生成 SQL，执行准确率从37.1%升至50.0%。
- **常驻智能**
  - [持续在线个人智能](#item-1)：以感知、记忆、行动三模块持续闭环，解决个人助手跨请求失去状态且难以安全自我改进的问题。
- **系统与模型**
  - [Mobile AI Factory](#mobile-ai-factory)：让智能体依据目标手机实测自动搜索微调与量化配置，把 GPU 搜索时间降至穷举的1/19。
  - [Qwen4-Max](#qwen4-max)：以稀疏专家计算和上下文压缩降低编程、办公及长程任务的模型调用成本。
- **热点延伸**：[Gamer](#gamer)、[DySENSE](#dysense)、[MMFlash](#mmflash)

## 对当前研究的启发
- **HarnessEvolve**
  - 迁移｜从 [HarnessDev](#harnessdev) 把创建、反馈迭代、跨模型迁移和未见任务测试用于脚手架验收：统一记录成功率、成本与排名变化
  - 延续｜[RiseHarness](#riseharness) 未覆盖始终失败轨迹：加入故障注入与中间检查点，对比双轨迹基线的恢复率、成本和方差
- **AgentTrainEvolve**
  - 迁移｜从 [DeLoop](#deloop) 把“重复调用—恢复动作”用于偏好训练：从工具日志挖掘样本，以DPO评测循环率、成功率和调用成本
  - 延续｜[Terminal-RSI](#terminal-rsi) 缺少等算力消融：固定轨迹数与Token预算，对比完整循环及各删减版的成功率和跨任务泛化
- **AgentEvolve**
  - 迁移｜从 [SkillMaster](#skillmaster) 把反事实下游效用用于技能淘汰：屏蔽单项技能重跑相似任务，按成功率差更新保留权重
  - 延续｜[MEM-SQL](#mem-sql) 的多历史组合复用明显退化：构造多表连接任务，对比分层与扁平检索的准确率、延迟和成本
- **AutonomousAgentEvolve**
  - 延续｜[持续在线个人智能](#item-1) 缺少自改追踪与撤回：记录每次修改并设置回滚组，对比危险修改拦截率和故障恢复时间
- **Awesome-RSI**
  - 迁移｜从 [Post-Training RSI](#post-training-rsi) 把数据、奖励、验证器和搜索策略设为共同进化对象：逐周期测量改进速率与退化率
- **CodeEvolve**
  - 迁移｜从 [Harness-of-Harness](#harness-of-harness) 把独立验收和版本化证据用于编码闭环：每轮保存测试、缺陷与回归结果后再规划
- **InfraEvolve**
  - 迁移｜从 [Mobile AI Factory](#mobile-ai-factory) 把真机测量接入配置搜索：按设备联合优化量化位宽、后端、时延、内存与能耗

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-17/  

