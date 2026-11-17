# 2026-11-17 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **技能与递归**
  - [SkillMaster](#skillmaster)：把技能创建、修订和保留纳入策略训练，并按后续任务收益判断技能是否值得沉淀。
  - [Terminal-RSI](#terminal-rsi)：交替保留已验证行为与精炼策略，把零散修复汇聚成完整成功，宏平均成功率提升29.90个百分点。
  - [HarnessDev](#harnessdev)：让智能体从种子框架自主创建和迭代执行系统，并以跨模型、未见任务测试暴露反馈过拟合。
- **长期记忆**
  - [CLAM](#clam)：用循环超网络把跨会话规律一次编译进固定大小适配器，避免文本记忆随使用持续膨胀。
  - [HEAMS](#heams)：把记忆视为用户信息托管服务，统一审计准确性、效率、隐私、安全及用户删除权。
- **可信评测**
  - [SilentGuard](#silentguard)：在工具执行层强制检查返回值不变量，拦截“显示成功但内容错误”的结果，将错误率从74.0%降至1.7%。
  - [Benchmark Factory](#benchmark-factory)：以已知强弱模型作为无标签质量锚点，自动从私有代码变更中筛任务并修复评分器。
- **具身与科研**
  - [RoboFinals RL Envs](#robofinals-rl-envs)：用连续状态和柔体交互构建物理可信的长程机器人环境，让前序动作真实影响后续训练。
  - [书生·S2.1 Flash](#s2-1-flash)：统一科学多模态表征、专业工具执行与结果核验，以十分之一推理成本交付可复查科研证据。
- **系统与效率**
  - [CompoundingKernel](#compoundingkernel)：用外置谱系归档和并行智能体持续搜索GPU内核，在209道题上达到参考实现的4.40倍速度。
  - [Karpo Decision](#karpo-decision)：以单次前向并行评分替代逐字生成，让工具路由等高频决策降至毫秒级。
  - [Qwen4-Max](#qwen4-max)：以稀疏计算处理百万级上下文和长程工具任务，将平均使用费用降低58%。
- **常驻智能体**
  - [Always-on Agent](#always-on-agent)：用事件唤醒、持久状态和休眠替代持续推理，让长程智能体低成本全天候运行。
- **热点延伸**：[Gamer](#gamer)、[DySENSE](#dysense)、[MMFlash](#mmflash)

## 对当前研究的启发
- **AgentEvolve**
  - 迁移｜从 [SkillMaster](#skillmaster) 把“后续任务因果收益”用于技能淘汰：回放有无该技能的同类任务并比较成功率与成本。
- **AgentTrainEvolve**
  - 迁移｜从 [Terminal-RSI](#terminal-rsi) 把已验证行为跨阶段继承用于长程训练：与全量重训对比最终成功率、退化率和样本效率。
- **AutonomousAgentEvolve**
  - 迁移｜从 [Always-on Agent](#always-on-agent) 把事件唤醒和持久状态用于常驻运行时：实现休眠、定时器、审批暂停及断点恢复测试。
- **MemoryEvolve**
  - 迁移｜从 [CLAM](#clam) 把固定容量参数记忆用于跨会话助手：对比文本检索、在线微调及混合方案的准确率、延迟和存储量。
  - 延续｜[HEAMS](#heams) 尚未覆盖全部记忆责任：补充撤回、越权共享和陈旧信息测试，统计违规率与删除残留率。
- **HarnessEvolve**
  - 迁移｜从 [SilentGuard](#silentguard) 把工具返回不变量用于执行层：注入伪成功、缺字段和越界值，测错误拦截率与误拒率。
  - 延续｜[HarnessDev](#harnessdev) 仅有4领域和单条进化轨迹：扩至多模型多种子，比较未见任务成功率与跨模型排名稳定性。
- **InfraEvolve**
  - 迁移｜从 [CompoundingKernel](#compoundingkernel) 把谱系归档用于算子搜索：保存父子修改、正确性和性能，按吞吐与验证耗时调度并发。
- **EvalEvolve**
  - 迁移｜从 [Benchmark Factory](#benchmark-factory) 把强弱模型排序作为质量锚点用于动态基准：自动筛除过易题并标记异常评分器供人工复核。
- **ResearchEvolve**
  - 迁移｜从 [书生·S2.1 Flash](#s2-1-flash) 把原始工具产物和核验记录用于科研交付：要求每项结论可追溯、复算并通过独立检查。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-17/  

