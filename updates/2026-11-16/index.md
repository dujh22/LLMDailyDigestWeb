# 2026-11-16 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归改进**
  - [RSI Arena](#rsi-arena)：用等预算沙箱和人类盲测指导自主后训练，同时分开测能力、偏好与安全，揭示更讨喜不等于更强或更安全。
  - [RSI综述](#rsi)：以四类可进化组件和七步闭环统一经验归因、更新验证与回滚，解决智能体经验难以沉淀为长期改进的问题。
  - [权重空间编程](#item-36)：让通用模型按自然语言直接修改另一模型的权重，无需数据或梯度、最少改6个参数即可植入后门。

- **脚手架演化**
  - [ModHarness-RL](#modharness-rl)：把上下文压缩和行动引导写成可学习程序，使脚手架能随强化学习中的行为变化共同更新。
  - [G-CAST](#g-cast)：用奖励路由、数据编排和累积能力门控持续训练智能体，避免学习新需求和工具时破坏既有能力。
  - [Co-Sight Harness](#co-sight-harness)：把业务规则外置为版本化控制资产并逐步机器验收，将长链任务完成率从50%提升至100%。

- **评测审计**
  - [Verification Transport](#verification-transport)：对同一轨迹比较原生、抽象和恢复视图，发现验证器跨工具封装或历史压缩后的判断失败率最高约31%。
  - [多智能体评测](#item-33)：用匹配采样次数与推理预算的分层基线重测协作收益，发现74%的可比实验不优于单体基线。
  - [Singularity-Bench](#singularity-bench-ai)：以六项真实基础设施构建任务和同硬件性能验收，衡量智能体能否自主实现训练、推理与集群系统。

- **记忆与缓存**
  - [CarryOn](#carryon)：用紧凑执行状态保存进度、用源链接保留精确证据，避免长程智能体在压缩历史时丢失决策依据。
  - [Callo](#callo-kv)：把上下文编辑后失效的KV缓存用于提前生成候选，再精确重算验证，以无损方式回收缓存价值、缩短等待。

- **自主科研**
  - [Verifiable pXRD](#verifiable-pxrd)：用前向物理模拟验证候选结构，并从合成任务学习搜索策略，将真实粉末衍射结构恢复率从27%提高到69%。
  - [NeoResearch](#neoresearch)：让文献证据循环提出模型、实验经验循环修正适用条件，自动发现面向不同领域的轻量时序模型。
  - [PaperCritic](#papercritic-f1)：把论文健全性评审拆成意见可信度与问题覆盖度，并用F1奖励训练可跨领域迁移的审稿模型。

- **具身学习**
  - [PEAR](#pear)：仅用仿真强化学习、无需示范数据训练27B推理模型，使其迁移到真实双臂机器人后达到60%任务成功率。

- **热点延伸**：[RSI预测](#rsi-ai)

## 对当前研究的启发
- **Awesome-RSI**
  - 迁移｜从 [RSI Arena](#rsi-arena) 把能力、偏好与安全分离用到自改进验收：每轮同预算盲测三类指标并设退化否决线
  - 延续｜[RSI Arena](#rsi-arena) 留下单模型单次运行且反馈归因不清：跨模型重复多轮，对比有无人类反馈的能力与安全增量

- **HarnessEvolve**
  - 迁移｜从 [ModHarness-RL](#modharness-rl) 把脚手架参数化为可学习程序：联合优化压缩、状态表示和偏离引导，以任务成功率验收
  - 延续｜[Verification Transport](#verification-transport) 留下有损溯源时恢复率下降：分级删除轨迹证据，测判断一致率、弃答率和误判率

- **AgentTrainEvolve**
  - 迁移｜从 [G-CAST](#g-cast) 把累积能力契约用到持续后训练：每轮同时回归旧工具与新需求，任一旧能力退化即拒绝更新

- **MemoryEvolve**
  - 迁移｜从 [CarryOn](#carryon) 把“状态摘要＋源链接证据”用到长程记忆：分别测成功率、证据命中率和每步上下文成本

- **ResearchEvolve**
  - 迁移｜从 [Verifiable pXRD](#verifiable-pxrd) 把前向模拟验证用到无标准答案科研任务：合成可验样本训练，再在真实数据测恢复率
  - 迁移｜从 [PaperCritic](#papercritic-f1) 把精确率—召回率奖励用到科研审稿：分别标注误报与漏报，对比偏好奖励的跨领域迁移

- **RobotEvolve**
  - 延续｜[PEAR](#pear) 留下纯仿真迁移边界未明：改变物体、视角和机器人本体，对比模仿学习并测真机成功率与能力遗忘

- **SwarmEvolve**
  - 迁移｜从 [多智能体评测](#item-33) 把资源匹配基线用到群体实验：固定模型、采样和token预算，对比协作、独立采样与证据分区

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-16/  

