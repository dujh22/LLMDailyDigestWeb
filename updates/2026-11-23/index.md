# 2026-11-23 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归改进**
  - [CoEvoBench](#coevobench)：让模型与智能体脚手架联合迭代，首次直接检验系统能否把一次升级转化为持续改进。
  - [Search-RSI](#search-rsi)：同步扩展训练任务与可检索证据，避免知识缺失被误判为策略错误，九项基准平均提升9.5–9.8点。
  - [Embodied-Harness](#embodied-harness)：把机器人执行成败沉淀为分层规则，无需修改模型参数即可持续修正操作流程。
  - [Alps Lab](#alps-lab)：将数字仿真、真实执行反馈与AI研发接成闭环，让认知体自主实验、验证并积累可复用方法。
- **长期记忆**
  - [Memory Tax](#memory-tax)：在统一检索预算下用原始记录检索审计复杂记忆，揭示信息重构常因失真和访问困难产生负收益。
  - [GroupAssistBench](#groupassistbench)：用真实群聊和证据绑定评分，同时检查智能体能否找回历史并执行仍然有效的多人约束。
  - [MemOnce](#memonce)：仅保存紧凑状态并按需还原完整缓存，在百万词元上下文中将缓存缩小1313倍。
- **可信智能体**
  - [可追溯多智能体科研社区](#item-3)：以声明账本、代码数据提交和多模型审稿组织936个智能体，使每篇自动生成论文均可追溯核查。
  - [SplitBench](#splitbench)：分离测试执行权与最终判分权，防止编程智能体篡改评测设施后伪造通过结果。
  - [Epistemic Guard](#epistemic-guard)：用签名工具收据同时约束回答和记忆写入，阻止虚构执行结果进入长期记忆。
- **评测治理**
  - [METR](#metr-3-6)：用人类任务时长衡量长程能力，发现可完成时长每3.6个月翻倍，但近似训练环境会高估真实能力。
  - [OpenAI预训练曲线](#openai-ai)：公开预训练困惑度曲线并提出能力红线，用底层压缩指标为模型扩张设置可审计检查点。
- **训练可靠性**
  - [自幻觉记忆](#item-49)：追踪强化学习中的自生成错误，发现结果奖励会把已纠正的幻觉固化进模型，平均召回率增加4.83%。
  - [SH-PRM](#sh-prm)：按语义段落提供局部过程奖励，使长报告训练能定位具体错误而非把整篇成败平均分摊。

## 对当前研究的启发
- **Awesome-RSI**
  - 延续｜[CoEvoBench](#coevobench) 留下“单次升级后难以继续改进”：做5轮模型—脚手架迭代，统计逐轮增益与回退率
  - 迁移｜从 [Search-RSI](#search-rsi) 把任务与证据同步扩展用到开放式RSI环境：先验证证据可达，再生成更难任务
- **MemoryEvolve**
  - 迁移｜从 [Memory Tax](#memory-tax) 把统一检索预算用到记忆评测：同题比较原始记录RAG与重构记忆的净增益
  - 延续｜[GroupAssistBench](#groupassistbench) 留下召回与约束评分贡献未拆分：做2×2消融，分别统计召回率和约束遵守率
- **ResearchEvolve**
  - 延续｜[可追溯多智能体科研社区](#item-3) 留下选题品味不足：与专家排序对比，以入选率、新颖性和复现率评估
- **EvalEvolve**
  - 延续｜[SplitBench](#splitbench) 留下25%攻击未阻断：分类补强原始测试，对比权限分离前后的攻击成功率与误通过率
- **MonitorEvolve**
  - 迁移｜从 [Epistemic Guard](#epistemic-guard) 把签名收据用到常驻智能体监管：无收据的执行声明禁止汇报或写入记忆
- **EvolveLLM**
  - 迁移｜从 [自幻觉记忆](#item-49) 把错误事实追踪用到RL后训练：记录纠错前后召回率，检测奖励是否固化幻觉
- **AgentEvolve**
  - 迁移｜从 [Embodied-Harness](#embodied-harness) 把分层经验规则用到部署期自进化：失败证据写回技能库并保留回滚版本
- **AgentTrainEvolve**
  - 迁移｜从 [SH-PRM](#sh-prm) 把语义分段奖励用到长程Agent训练：按计划、工具调用和结论分别计算局部优势

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-23/  

