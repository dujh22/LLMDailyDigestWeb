# 2026-11-23 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归改进**
  - [CoEvoBench](#coevobench)：让模型与交互脚手架联合迭代，首次检验智能体能否把单次升级变成持续改进。
  - [Alps Lab](#alps-lab)：把提出问题、执行实验和真实反馈纳入同一闭环，让认知体参与改进下一代AI。
  - [Search-RSI](#search-rsi)：同步扩展训练任务与可检索证据，避免知识库缺失被误判为智能体能力不足。
  - [Embodied-Harness](#embodied-harness)：把机器人失败证据写成可检索规则，无需更新模型参数即可持续提高操作成功率。
- **科研自动化**
  - [Claude](#claude)：只计算算法归约真正需要的矩阵项，首次突破3SUM和APSP问题沿用多年的复杂度上限。
  - [可追溯多智能体科研社区](#item-3)：用声明账本、代码提交和多模型审稿，组织936个智能体产出可追溯论文。
  - [黎曼猜想形式化证明](#item-7)：以命题语义审计和多个独立Lean内核复核，降低超大机器证明验错命题的风险。
- **记忆可信**
  - [Memory Tax](#memory-tax)：在相同检索预算下对比朴素检索，发现复杂记忆重构常因失真和访问退化产生负收益。
  - [GroupAssistBench](#groupassistbench)：用真实群聊及证据绑定评分，区分“找回历史”与“正确执行历史约束”。
  - [Epistemic Guard](#epistemic-guard)：用签名工具收据同时约束回答和记忆写入，阻止虚构执行结果沉淀为长期记忆。
  - [自幻觉记忆：后训练固化错误事实](#item-49)：追踪强化学习中的自生成错误，发现结果奖励会让已撤回的幻觉更易被模型记住。
- **评测审计**
  - [SplitBench](#splitbench)：把测试执行与最终判分权限隔离，防止编程智能体篡改环境后伪造通过结果。
  - [Benchmarks' Last Exam](#benchmarks-last-exam)：逐题核验提示、环境和评分器，揭示排行榜总分掩盖的系统性评测缺陷。
  - [METR](#metr-3-6)：测得AI可独立完成的任务时长每3.6个月翻倍，同时发现相似训练环境会高估真实能力。
- **经验训练**
  - [From Acting to Learning](#from-acting-to-learning)：按经验对当前优化器的实际作用筛选成功轨迹，使4B智能体成功率最高达到81.45%。

## 对当前研究的启发
- **Awesome-RSI**
  - 迁移｜从 [CoEvoBench](#coevobench) 把模型与脚手架联合迭代用于RSI评测：固定五轮升级，逐轮记录净增益与退化率
  - 延续｜[CoEvoBench](#coevobench) 留下单次升级难以持续的问题：对比独立改进器与共享历史改进器的五轮累计收益
- **MemoryEvolve**
  - 迁移｜从 [Memory Tax](#memory-tax) 把统一检索预算用于记忆审计：同预算对比复杂记忆、原始记录检索及净准确率
  - 延续｜[GroupAssistBench](#groupassistbench) 留下召回与约束执行贡献未拆分的问题：分别消融RER、ACB并测证据召回率与任务成功率
- **EvalEvolve**
  - 迁移｜从 [SplitBench](#splitbench) 把执行与判分权限分离用于Agent基准：判分器保存秘密测试并拒绝代理侧写入
  - 延续｜[METR](#metr-3-6) 留下环境相似性高估问题：构造同分布与分布外长任务，对比时长上限及失败率
- **ResearchEvolve**
  - 迁移｜从 [可追溯多智能体科研社区](#item-3) 把声明账本用于科研Agent：每项结论绑定代码、数据、运行记录和审稿意见
  - 延续｜[黎曼猜想形式化证明](#item-7) 留下命题编码可能失真的问题：双人独立形式化并跨内核比较定理同一性
- **AgentTrainEvolve**
  - 迁移｜从 [From Acting to Learning](#from-acting-to-learning) 把优化器感知选样用于轨迹回灌：对比随机、高损失与梯度选样的样本效率
- **DataEvolve**
  - 延续｜[自幻觉记忆：后训练固化错误事实](#item-49) 留下错误事实被奖励固化的问题：跟踪撤回幻觉训练前后的召回率与置信度

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-23/  

