# 2026-11-28 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **协同进化**
  - [CoEvo-RSI](#coevo-rsi)：跨代保存并重配模型与脚手架，避免各自升级后的接口错配，使9B模型胜过大型模型。
  - [RSI 2026](#rsi-2026)：用自主性分级、独立留出集和轨迹审计，区分真实自我改进与任务过拟合。
  - [AutoSFT](#autosft)：让执行、分析和合成智能体共同筛选、修复与扩增数据，突破单智能体只能调样本比例的限制。
- **模型记忆**
  - [Stable Gated DeltaNet-2](#stable-gated-deltanet-2)：用对称擦除限制循环状态放大，使线性注意力可稳定训练至128K上下文。
  - [定向监督激活线性注意力召回](#item-23)：用句子重复和重点加权训练，释放线性注意力原本未被利用的远距离召回能力。
  - [BiDE-Mem](#bide-mem)：先拆解问题所需证据类型再组织可溯源记忆，解决检索相关却不足以作答的问题。
- **评测监管**
  - [RAP](#rap)：先测候选模型是否真有逐题互补性，避免把偶然路由收益误判为通用能力。
  - [置信度注入揭示自监控失效](#item-28)：用反事实置信度提示分离发现错误与修复错误，证明模型能被疑虑引导却难以自查。
  - [Conartist](#conartist)：根据安全审计反馈自适应串联两阶段提示注入，使电脑智能体护栏最高被绕过66.67%。
  - [FORK](#fork)：让护栏与读取拒绝信息的攻击者共同演化，同时优化拦截边界和拒绝信息泄露。
- **推理训练**
  - [SAEPO](#saepo)：用稀疏语义概念把最终成败拆成逐词奖惩，无需过程标注即可改善推理信用分配。
  - [Solve Vision with Code](#solve-vision-with-code)：让编码智能体编程渲染答案视频，以可检查程序替代不稳定的像素直接生成。
- **具身系统**
  - [Motubrain 2.0](#motubrain-2-0)：以统一动作表示和执行反馈闭环，让机器人迁移视频经验并自主规划、验证和纠错。
  - [RUIBench](#ruibench)：隔离比较机器人动作接口，发现仅更换接口即可把智能体成功率从45%提高到81%。
- **代码改进**
  - [Kolpona](#kolpona)：用仿真结果定位并闭式编辑少数神经元，无需再训练便把27B模型的RTL通过率提升至94.9%。
- **热点延伸**：[ProxyGenBench](#proxygenbench)、[StateWeaver](#stateweaver)、[Boundary-Aware Policy Learning](#boundary-aware-policy-learning)、[JudiAct](#judiact)

## 对当前研究的启发
- **AgentEvolve**
  - 迁移｜从 [CoEvo-RSI](#coevo-rsi) 把模型与脚手架版本配对用于迭代筛选：保留历史组合，按任务得分跨代重组。
- **DataEvolve**
  - 迁移｜从 [AutoSFT](#autosft) 把六类数据动作用于SFT数据飞轮：按失败类型执行筛选、修复、重标和合成。
- **Awesome-RSI**
  - 延续｜[RSI 2026](#rsi-2026) 留下跨任务泛化与能力保持问题：等算力迭代五轮，测留出任务增益和旧任务退化。
  - 迁移｜从 [置信度注入揭示自监控失效](#item-28) 把置信度当控制接口用于纠错评测：分别注入真假疑虑，测检错率与修复率。
- **CacheEvolve**
  - 迁移｜从 [Stable Gated DeltaNet-2](#stable-gated-deltanet-2) 把状态非扩张约束用于缓存更新：监测谱范数、长程召回和128K训练稳定性。
- **MemoryEvolve**
  - 迁移｜从 [BiDE-Mem](#bide-mem) 把类型化需求用于记忆检索：先预测时序、多跳等约束，再按来源组装充分证据。
- **EvalEvolve**
  - 迁移｜从 [RAP](#rap) 把可路由性审计用于多模型基准：分析逐题得分矩阵，并报告理论路由上限与实际增益。
- **HarnessEvolve**
  - 延续｜[RUIBench](#ruibench) 留下任务级执行验证缺口：比较单步检查、模型自报与终态验证的误报率和任务成功率。
  - 迁移｜从 [Conartist](#conartist) 把级联注入用于Harness红队：开放审计反馈与附加动作，测攻击成功率和恢复率。
- **EvolveLRM**
  - 迁移｜从 [SAEPO](#saepo) 把稀疏概念归因用于结果奖励训练：接入GRPO，对比样本效率、正确率和奖励作弊率。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-28/  

