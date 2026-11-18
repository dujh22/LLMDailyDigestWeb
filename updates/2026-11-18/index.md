# 2026-11-18 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **快速决策**
  - [Karpo Decision](#karpo-decision)：把逐词生成改成一次并行评估所有候选动作，使31B模型的智能体决策中位延迟降至94毫秒。
- **训练与演化**
  - [Axion 1.0](#axion-1-0-sft)：用递进的两阶段监督训练和分阶段奖励训练科学智能体，在高难知识与工具任务HLE上达到59.0%。
  - [自我改进分支混合](#item-5)：让多个脚手架搜索分支分别积累经验，再按任务动态组合，避免所有候选收敛到同一种局部最优方案。
- **真实评测**
  - [GPT-6.2 Astra](#gpt-6-2-astra)：对高分模型进行真实长程任务测试，暴露出静态基准未能测出的停摆、循环和算力浪费。
  - [SWE-CoWork](#swe-cowork)：用模拟工程组织检验智能体能否持续追踪需求并完成交付，领先模型完成率仍不足8%。
  - [Accelerate Bench](#accelerate-bench)：以完整应用和独立正确性验证器评测代码智能体，避免用局部代码提速冒充端到端优化。
- **执行底座**
  - [CubeSandbox](#cubesandbox)：用可保存、回滚和迁移状态的微虚拟机隔离不可信操作，同时支持生产级智能体高密度并发。
- **开放模型**
  - [K2-Horizon](#k2-horizon)：结合稀疏上下文读取与无损扩散式解码，并开放数据和训练轨迹，最高实现2.2倍解码提速。
  - [Sage S2.1 Flash](#sage-s2-1-flash)：把科学图表等证据接入通用模型，并用环境执行结果验收答案，统一科学推理与交互操作。
- **具身学习**
  - [SALA](#sala)：用语言语义对齐人类和机器人的潜在动作，使未配对的人类视频也能训练可迁移的机器人策略。
  - [ScaleVLA](#scalevla-vlm-dit)：把5520亿参数视觉语言模型接入动作生成器，以更少机器人样本提升跨场景泛化和精细操作。
- **长程生成**
  - [MovieRoll](#movieroll)：通过分窗训练、分层压缩历史缓存和长滚动蒸馏，抑制流式视频的持续失真与显存增长。
- **热点延伸**：[AllocFlow](#allocflow)、[InclusionMed](#inclusionmed)、[SPILLWAY](#spillway)

## 对当前研究的启发
- **JevEvolve**
  - 迁移｜从 [Karpo Decision](#karpo-decision) 把候选并行打分用于快慢路由：按置信度升级慢模型，测准确率、校准误差和P95延迟。
- **AgentTrainEvolve**
  - 迁移｜从 [Axion 1.0](#axion-1-0-sft) 把两阶段SFT与阶段奖励用于工具训练：对比单阶段SFT，测任务成功率和证据有效率。
- **EvalEvolve**
  - 迁移｜从 [GPT-6.2 Astra](#gpt-6-2-astra) 把有效进展与停止行为用于长程评测：记录循环次数、无效算力和人工接管率。
  - 迁移｜从 [SWE-CoWork](#swe-cowork) 把需求到交付的证据链用于动态基准：生成需求变更，测追踪、验证与交接完成率。
- **SystemEvolve**
  - 延续｜[自我改进分支混合](#item-5) 的路由器未稳定胜过最佳分支：固定预算改变路由上下文和更新频率，测成功率与token成本。
- **EnvironmentEvolve**
  - 迁移｜从 [CubeSandbox](#cubesandbox) 把快照分岔用于环境生成：同一初态并行运行任务变体，验证隔离性、恢复耗时和状态一致性。
- **CodeEvolve**
  - 迁移｜从 [Accelerate Bench](#accelerate-bench) 把完整应用与独立验证器用于程序进化：对比局部基准，测端到端加速和正确率。
- **CacheEvolve**
  - 迁移｜从 [MovieRoll](#movieroll) 把分层历史压缩用于固定预算缓存：对比全量缓存与固定窗口，测质量漂移、显存和吞吐。
- **RobotEvolve**
  - 迁移｜从 [SALA](#sala) 把语言语义软邻域用于人类视频预训练：对比重建式对齐，测真机成功率和跨本体迁移率。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-18/  

