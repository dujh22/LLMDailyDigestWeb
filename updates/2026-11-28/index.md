# 2026-11-28 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **系统协同**
  - [CoEvo-RSI](#coevo-rsi)：跨代搜索历史模型与脚手架的最佳组合，避免独立升级造成接口错配，使9B模型在垂直任务上超过大型模型。
- **进化验证**
  - [RSI 2026](#rsi-2026)：用自主性分级、独立留出集和轨迹审计，区分真正可泛化的自我改进与基准过拟合。
- **数据与训练**
  - [AutoSFT](#autosft)：让执行、分析和合成智能体联合筛选、修复与生成微调数据，突破只调整样本比例的自动优化。
  - [AutoRL](#autorl)：用多智能体在线诊断、低成本验证和可回滚热更新，自动修复强化学习的平台期、异常与中断。
- **智能体评测**
  - [OS-Omni](#os-omni)：在六类真实平台的统一活态环境中评测长程操作，揭示最强智能体仍落后人类8.8个百分点。
  - [DRBench Pro](#drbench-pro)：以知识树和证据化评分分别衡量深研报告的探索广度与链路深度，最佳覆盖率仅57.04%。
  - [Vernier](#vernier)：计算排行榜可辨别的最小分差，发现零样本时序预测榜单常无法可靠区分前十模型。
- **可审计推理**
  - [Solve Vision with Code](#solve-vision-with-code)：让编码智能体编写程序并渲染答案视频，以可检查的符号计算替代不稳定的直接像素生成。
- **安全恢复**
  - [数据库智能体错误损失分层评测](#item-13)：通过预置错误、权限分组和恢复演练，分离模型失误、访问控制与数据库恢复对事故损失的影响。
- **实时生成**
  - [ShowNow](#shownow)：在播放期间预计算不同动作的未来画面并细粒度提交，将交互世界模型延迟从620降至208毫秒。
- **热点延伸**：[ProxyGenBench](#proxygenbench)、[StateWeaver](#stateweaver)、[Boundary-Aware Policy Learning](#boundary-aware-policy-learning)、[JudiAct](#judiact)

## 对当前研究的启发
- **HarnessEvolve**
  - 迁移｜从 [CoEvo-RSI](#coevo-rsi) 把跨代配对搜索用到版本选择：保留模型与脚手架档案，交叉组合后按任务得分和TIMR排序。
  - 延续｜[CoEvo-RSI](#coevo-rsi) 留下开放环境泛化未验证：在OS-Omni对比最新版本直配与档案搜索，统计成功率和平台方差。
- **Awesome-RSI**
  - 迁移｜从 [RSI 2026](#rsi-2026) 把独立验证门槛用到RSI收录：要求等预算留出集、轨迹审计及原能力回归结果。
- **GeneralizeEvolve**
  - 延续｜[RSI 2026](#rsi-2026) 留下跨任务增益与能力保持问题：连续自改多轮，测留出任务迁移率和旧任务退化率。
- **DataEvolve**
  - 迁移｜从 [AutoSFT](#autosft) 把六类数据动作加入数据飞轮：按失败类型自动筛选、修复、重标与合成样本。
  - 延续｜[AutoSFT](#autosft) 留下零分能力和多智能体成本：等预算对比单体与多体，报告能力增益、API费和耗时。
- **AgentTrainEvolve**
  - 迁移｜从 [AutoRL](#autorl) 把诊断—验证—回滚闭环用于长程RL：注入训练故障，对比静态配方的恢复率和最终奖励。
- **EvalEvolve**
  - 迁移｜从 [Vernier](#vernier) 把最小可辨分差用于动态榜单：公开逐任务得分，仅在差异超过分辨率时报告排名。
  - 延续｜[OS-Omni](#os-omni) 留下跨平台迁移差距：固定模型和预算做六平台交叉测试，报告成功率与状态跟踪错误率。
- **ResearchEvolve**
  - 迁移｜从 [DRBench Pro](#drbench-pro) 把知识树用于深研验收：分别计算方向覆盖率、证据链深度和无来源断言率。
- **ReasoningEvolve**
  - 延续｜[Solve Vision with Code](#solve-vision-with-code) 留下开源编码模型落差：同题对比开闭源智能体的得分、执行率与可审计性。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-28/  

