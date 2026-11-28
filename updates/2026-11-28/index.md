# 2026-11-28 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **协同进化**
  - [CoEvo-RSI](#coevo-rsi)：跨代保存并重组模型与脚手架版本，避免独立升级导致接口错配，使9B模型在垂直任务上超过大型模型。
  - [RSI 2026](#rsi-2026)：用自主性分级、独立留出集和轨迹审计，区分真正可泛化的自我改进与基准过拟合。
  - [AutoSFT](#autosft)：让执行、分析、合成智能体协作筛选、修复和生成微调数据，将IFEval最高推至81.58。
  - [AutoRL](#autorl)：用多智能体在线诊断、低成本验证和可回滚热更新，自动修复强化学习训练的平台期与中断。

- **评测方法**
  - [OS-Omni](#os-omni)：在六类真实平台的统一活态环境中评测长程操作，发现最强智能体仍落后人类8.8个百分点。
  - [DRBench Pro](#drbench-pro)：用知识树分别衡量研究报告覆盖多广、追索多深，最佳智能体知识覆盖率仅57.04%。
  - [Vernier](#vernier)：计算榜单能够可靠区分的最小分差，揭示零样本时序预测前十名常无法统计区分。
  - [数据库智能体错误损失分层评测](#item-13)：用预设错误、权限分组和恢复演练，拆分模型失误、护栏与回滚能力各自造成的损失。

- **推理与架构**
  - [Solve Vision with Code](#solve-vision-with-code)：让编码智能体写程序渲染答案视频，以可检查计算替代不稳定的直接像素生成，最高得分0.923。
  - [Stable Gated DeltaNet-2](#stable-gated-deltanet-2)：用对称擦除和受控写入抑制循环状态爆炸，同时改善长上下文信息检索。

- **实时生成**
  - [ShowNow](#shownow)：播放时预计算不同动作的未来画面并细粒度提交，将交互世界模型延迟从620降至208毫秒。

- **热点延伸**：[ProxyGenBench](#proxygenbench)、[StateWeaver](#stateweaver)、[Boundary-Aware Policy Learning](#boundary-aware-policy-learning)、[JudiAct](#judiact)

## 对当前研究的启发
- **AgentEvolve**
  - 迁移｜从 [CoEvo-RSI](#coevo-rsi) 把跨代版本重组用于智能体迭代：归档模型、提示和工具配置，按任务得分搜索历史配对。
  - 延续｜[CoEvo-RSI](#coevo-rsi) 尚未验证开放环境泛化：加入跨领域任务，对比线性升级与跨代重组的成功率和成本。

- **Awesome-RSI**
  - 迁移｜从 [RSI 2026](#rsi-2026) 把独立留出集和等算力预算用于RSI验证：逐轮记录泛化增益、能力保持率与轨迹异常。
  - 延续｜[RSI 2026](#rsi-2026) 留下评估器可信度问题：用人工盲评和异构评估器对照，测一致率与奖励作弊率。

- **DataEvolve**
  - 延续｜[AutoSFT](#autosft) 固定了模型、训练器和预算：做跨模型与多预算实验，比较收益、数据多样性和API成本。

- **AgentTrainEvolve**
  - 迁移｜从 [AutoRL](#autorl) 把可回滚在线干预用于长周期RL：小流量验证配方后热更新，以恢复次数和最终回报验收。

- **EvalEvolve**
  - 迁移｜从 [Vernier](#vernier) 把最小可辨分差用于动态榜单：公开逐任务得分，并只报告超过统计分辨率的排名变化。
  - 迁移｜从 [DRBench Pro](#drbench-pro) 把知识树用于科研智能体评测：分开统计方向覆盖率、证据链深度和引用正确率。

- **ReasoningEvolve**
  - 延续｜[Solve Vision with Code](#solve-vision-with-code) 仅覆盖可符号验证任务：扩展到近似物理场景，对比程序解法与视频模型的正确率和可审计性。

- **CacheEvolve**
  - 迁移｜从 [Stable Gated DeltaNet-2](#stable-gated-deltanet-2) 把对称擦除用于固定预算循环记忆：测长序列状态范数、检索率和吞吐。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-28/  

