# 2026-11-17 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **自主常驻**
  - [持续在线个人智能](#item-1)：用感知、记忆、行动闭环与分级审查，让个人助手跨请求保持状态并安全自我改进。
  - [Always-on Agent](#always-on-agent)：用事件唤醒、持久状态和休眠替代持续推理，让智能体低成本全天候执行长程任务。
- **技能与脚手架**
  - [SkillMaster](#skillmaster)：把技能编辑纳入策略，并按后续任务的实际收益决定创建、修订或保留技能。
  - [HarnessDev](#harnessdev)：让智能体从种子自主创建和迭代执行框架，并以跨模型、未见任务测试揭示反馈过拟合。
  - [Terminal-RSI](#terminal-rsi)：交替继承已验证行为与精炼策略，把局部终端修复汇聚为完整成功，宏平均提升29.9个百分点。
- **记忆演化**
  - [CLAM](#clam)：用循环超网络把跨会话经验一次编译进固定容量适配器，学习文本检索难以发现的隐含规律。
- **可信执行**
  - [SilentGuard](#silentguard)：把返回值不变量强制放入工具执行层，拦截“显示成功但内容错误”的结果，使错误率从74%降至1.7%。
  - [MetaAct](#metaact)：把执行反馈编译成可验证动作规则，在行动前阻止违规或不可逆操作，最高将违规率降至0%。
- **训练与评测**
  - [RISE](#rise)：用完整知识图谱替代答案周边子图，消除位置泄漏并训练智能体真正搜索和自主停止。
  - [Benchmark Factory](#benchmark-factory)：以已知强弱模型作无标签质量锚点，自动从私有代码变更中发现坏任务和坏评分器。
- **科研与程序**
  - [书生·S2.1 Flash](#s2-1-flash)：以统一多模态表征、真实工具执行和结果核验完成可复查科研任务，推理成本降至十分之一。
  - [CompoundingKernel](#compoundingkernel)：用外置谱系归档、并行搜索和独立验真从零进化GPU内核，公开题速度达参考实现4.4倍。
- **推理效率**
  - [Karpo Decision](#karpo-decision)：以单次前向的并行概率评分替代逐字生成，让高频行动选择降至毫秒级。
  - [GaugeRoPE](#gaugerope-rope)：构造可直接执行旋转位置编码的潜态缓存，免除历史重建并实现5.85倍压缩。
  - [Beyond Plain MCP](#beyond-plain-mcp)：让智能体编写工具调用脚本并声明返回结构，比额外路由器更有效地降低70%至90%词元。
- **热点延伸**：[Gamer](#gamer)、[DySENSE](#dysense)、[MMFlash](#mmflash)

## 对当前研究的启发
- **AutonomousAgentEvolve**
  - 迁移｜从 [Always-on Agent](#always-on-agent) 把事件收件箱与休眠恢复用于常驻循环：记录唤醒原因、检查点和审批状态。
- **AgentEvolve**
  - 迁移｜从 [SkillMaster](#skillmaster) 把下游反事实效用用于技能淘汰：遮蔽单项技能重跑相似任务，按成功率差值更新技能库。
- **HarnessEvolve**
  - 延续｜[HarnessDev](#harnessdev) 留下固定环境和单轨迹局限：跨模型各跑多条演化轨迹，以未见任务成功率和迁移损失比较。
  - 延续｜[SilentGuard](#silentguard) 留下只拒绝、不恢复的问题：注入新型工具故障，对比提示守卫与执行守卫的恢复率、误拒率。
- **AgentTrainEvolve**
  - 迁移｜从 [RISE](#rise) 把完整环境与自主停止用于检索训练：对比答案邻域环境，测成功率、搜索步数和停止准确率。
- **MemoryEvolve**
  - 迁移｜从 [CLAM](#clam) 把固定容量参数记忆用于跨会话学习：对比文本检索、适配器及混合方案的规律题准确率、延迟和容量。
- **EvalEvolve**
  - 迁移｜从 [Benchmark Factory](#benchmark-factory) 把强弱模型排序用作质量锚点：自动筛除过易任务并标记评分器反常样本供复核。
- **JevEvolve**
  - 迁移｜从 [Karpo Decision](#karpo-decision) 把单次前向概率读出用于工具路由：按置信度升级慢模型，测延迟、校准误差和任务成功率。
- **CacheEvolve**
  - 迁移｜从 [GaugeRoPE](#gaugerope-rope) 把频率保持约束用于潜态KV压缩：逐压缩率测试长文召回、吞吐和重建开销。
- **InfraEvolve**
  - 迁移｜从 [CompoundingKernel](#compoundingkernel) 把谱系归档接入内核搜索：并行生成后独立验真，按正确率、加速比和测量吞吐保留分支。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-17/  

