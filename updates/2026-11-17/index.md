# 2026-11-17 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自改进**
  - [Post-Training RSI](#post-training-rsi)：把数据、奖励、验证器和搜索策略全部纳入递归优化，避免自提升退化为反复训练模型权重。
  - [Terminal-RSI](#terminal-rsi)：交替保留已验证行为并精炼策略，把终端任务的局部修复累积为完整成功，宏平均成功率提升29.90个百分点。
- **技能与记忆**
  - [SkillMaster](#skillmaster)：让智能体按后续任务的实际收益自主创建、修订和淘汰技能，摆脱外部教师对技能价值的主观判断。
  - [ReHarness](#reharness)：根据新交互轨迹反向修订旧反思，使智能体在任务分布变化时更新经验而不过度遗忘。
  - [MEM-SQL](#mem-sql)：分层检索并复用已验证的历史SQL，避免每次从头生成，将执行准确率由37.1%提升至50.0%。
- **脚手架演化**
  - [HarnessDev](#harnessdev)：让智能体从种子自主创建和迭代执行框架，并以跨模型、未见任务测试揭露反馈集过拟合。
  - [RiseHarness](#riseharness)：对照成功与失败轨迹诊断并更新执行脚手架，减少长程终端智能体同题重复运行时的结果波动。
  - [HARNESS-ZERO](#harness-zero)：用审核智能体把专用脚手架的纠正改写为可学习轨迹，移除脚手架后成功率仍由23.3%升至44.3%。
  - [Harness-of-Harness](#harness-of-harness)：以规划、开发、独立验收和版本证据闭环维持跨轮软件状态，三轮平均相对提升52.25%。
- **常驻智能体**
  - [持续在线个人智能](#item-1)：以感知、记忆、行动三模块持续闭环和分级审查，定义能跨请求保留状态并安全自改进的个人助手。
  - [Always-on Agent](#always-on-agent)：用事件唤醒、持久状态和休眠替代持续推理，让智能体低成本全天候执行长程任务。
- **端侧部署**
  - [Mobile AI Factory](#mobile-ai-factory)：让智能体依据真机时延和精度自动微调、量化并筛选手机模型，搜索耗时降至穷举的1/19。
- **模型发布**
  - [Qwen4-Max](#qwen4-max)：以稀疏专家激活和更少上下文用量降低编程、办公及长程任务的端到端成本。
- **热点延伸**：[Gamer](#gamer)、[DySENSE](#dysense)、[MMFlash](#mmflash)

## 对当前研究的启发
- **AgentEvolve**
  - 迁移｜从 [SkillMaster](#skillmaster) 把“下游任务因果效用”用于技能淘汰：同题回放有无技能两版，按成功率与成本差决定保留
  - 延续｜[ReHarness](#reharness) 缺少长期指标与开销：构造连续分布漂移，对比只追加与反向修订，测成功率、遗忘率和成本
- **HarnessEvolve**
  - 迁移｜从 [HarnessDev](#harnessdev) 把创建—进化协议用于验收：加入从零创建、反馈迭代、跨模型迁移和未见任务测试
  - 延续｜[RiseHarness](#riseharness) 的改进依赖模型与基准：同一脚手架跨三种模型测试，统计成功率、方差和Token成本
- **Awesome-RSI**
  - 迁移｜从 [Post-Training RSI](#post-training-rsi) 把全栈递归用于实验闭环：分别版本化数据、奖励、验证器和搜索器，追踪跨轮增益
  - 延续｜[Terminal-RSI](#terminal-rsi) 五阶段同时改变多项因素：做等算力单变量消融，测成功率、分布外迁移和能力回退
- **AutonomousAgentEvolve**
  - 迁移｜从 [Always-on Agent](#always-on-agent) 把事件唤醒用于常驻运行时：实现持久收件箱、状态快照、定时器和审批后续跑
  - 延续｜[持续在线个人智能](#item-1) 缺少可撤回自修改：记录修改来源与影响，支持沙箱复演、人工审查和一键回滚
- **CodeEvolve**
  - 迁移｜从 [Harness-of-Harness](#harness-of-harness) 把独立验收用于长程开发：每轮保存版本、测试证据和失败清单，再规划下一轮
- **InfraEvolve**
  - 迁移｜从 [Mobile AI Factory](#mobile-ai-factory) 把真机测量用于模型搜索：联合优化量化配置、时延、内存和任务准确率

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-17/  

