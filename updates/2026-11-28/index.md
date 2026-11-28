# 2026-11-28 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **协同进化**
  - [CoEvo-RSI](#coevo-rsi)：跨代保存并重组模型与执行框架，避免独立升级造成接口错配，使9B模型在垂直任务上超过大模型。
- **自改进验证**
  - [RSI 2026](#rsi-2026)：用自主性分级、独立留出集和轨迹审计，区分真正可泛化的自我改进与评测过拟合。
  - [AutoSFT](#autosft)：让执行、分析和合成智能体协作筛选、修复及生成微调数据，突破单智能体只能调整样本比例的限制。
- **模型与记忆**
  - [Stable Gated DeltaNet-2](#stable-gated-deltanet-2)：用对称擦除限制循环状态放大，解决线性注意力长序列训练失稳，支持128K上下文。
  - [定向监督激活线性注意力召回](#item-23)：用句子重复和重点损失激活线性注意力潜在的远距离召回能力，而非继续扩大记忆容量。
  - [双时间尺度遗忘](#item-21)：用受控文法分别测量输出与内部表征，发现微调先压制行为、再缓慢遗忘知识。
  - [BiDE-Mem](#bide-mem)：按问题所需信息类型组织可溯源证据，解决检索结果相关却不足以完整作答的问题，LongMemEval达91.80%。
- **评测审计**
  - [RAP](#rap)：先测候选模型是否按题互补，再训练路由器，避免把偶然的模型切换收益误判为可泛化能力。
  - [置信度注入揭示自监控失效](#item-28)：用反事实置信度提示分离查错与改错能力，发现模型能被疑虑触发重思，却不会可靠发现自身错误。
  - [RUIBench](#ruibench)：统一比较机器人动作接口，证明仅改变接口即可将智能体成功率从45%提升至81%。
  - [Memphis](#memphis)：从真实执行记录反向构造仿真任务，使评测能复现开放式现实工作中的决策失误。
- **可靠训练**
  - [DAPO-V](#dapo-v)：按错误被人类发现的难度分配风险惩罚，减少准确率优化后仍隐蔽存在的多模态幻觉。
  - [GREMLIN](#gremlin)：筛选随机生成的神经环境来学习强化学习规则，替代昂贵人工游戏，并在26款游戏上超过未训练教师。
- **程序化求解**
  - [Solve Vision with Code](#solve-vision-with-code)：让编码智能体编程渲染答案视频，绕开直接生成像素的不稳定性，最高得分0.923。
  - [Kolpona](#kolpona)：定位并闭式编辑引发重复代码错误的少数神经元，无需再训练便将27B模型的RTL通过率提升至94.9%。
- **热点延伸**：[ProxyGenBench](#proxygenbench)、[StateWeaver](#stateweaver)、[Boundary-Aware Policy Learning](#boundary-aware-policy-learning)、[JudiAct](#judiact)

## 对当前研究的启发
- **AgentEvolve**
  - 迁移｜从 [CoEvo-RSI](#coevo-rsi) 把历史模型与脚手架重组用于版本选择：维护配对档案，按任务分数跨代搜索而非只用最新版。
- **Awesome-RSI**
  - 迁移｜从 [RSI 2026](#rsi-2026) 把分级与独立验证用于迭代验收：固定算力，逐轮测跨任务收益、能力保持率并审计轨迹。
- **DataEvolve**
  - 延续｜[AutoSFT](#autosft) 留下固定训练器及零分能力未改善：跨模型与预算比较单双智能体，测能力增益、耗时和API成本。
- **CacheEvolve**
  - 迁移｜从 [Stable Gated DeltaNet-2](#stable-gated-deltanet-2) 把非扩张状态更新用于循环缓存：对比原更新，测128K状态范数、困惑度与吞吐。
  - 迁移｜从 [定向监督激活线性注意力召回](#item-23) 把重复句与重点损失用于中期训练：对比普通语料，测远距召回率和通用困惑度。
- **EvalEvolve**
  - 迁移｜从 [RAP](#rap) 把可路由性审计用于路由基准：对比固定最优、理论最优和学习路由器，报告净准确率与成本。
  - 延续｜[Memphis](#memphis) 留下单任务证据不足：采集三类真实长程工作流，对比普通合成题，测现实失败复现率。
- **MemoryEvolve**
  - 迁移｜从 [BiDE-Mem](#bide-mem) 把类型化需求用于记忆检索：先拆分事实、时序和多跳约束，再测证据覆盖率与答案准确率。
- **RobotEvolve**
  - 延续｜[RUIBench](#ruibench) 留下自报成功与实际结果缺口：加入任务级独立验收，对比单步检查，测误报率和真实成功率。
- **Groom**
  - 迁移｜从 [RUIBench](#ruibench) 把接口作为受控变量用于token评测：同模型同任务切换接口，统计成功率、动作数和有效token占比。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-28/  

