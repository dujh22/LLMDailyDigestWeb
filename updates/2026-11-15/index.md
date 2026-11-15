# 2026-11-15 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **科研自治**
  - [MolRSI](#molrsi)：用跨任务成败记忆引导分子搜索策略迭代，将抗菌湿实验命中率从8.7%提升至15.9%。
  - [SPU](#spu)：隐藏真实湿实验结果并允许模型自主检索计算，补上科研AI缺少真实预测评测的问题。
  - [AI4AI](#ai4ai)：把科研控制权拆成搜索方向、方案空间和评价信号，避免用自动化步骤数误判AI的科研自主性。
- **训练稳定**
  - [RL训练](#item-1)：把训练前后的既有能力变化纳入评测，揭示只看目标分数会漏掉强化学习造成的能力漂移。
- **工具沉淀**
  - [DeepSeek Harness](#deepseek-harness)：通过对话生成插件并封装GitHub项目，让一次性想法沉淀为可复用的个人工具。
- **RSI图谱**
  - [递归自我改进](#ai-ai)：用8讲统一梳理AI改进AI的机制、评测与安全，解决相关路线分散、缺少全景框架的问题。

## 对当前研究的启发
- **ResearchEvolve**
  - 迁移｜从 [MolRSI](#molrsi) 把跨任务成败记忆用到假设筛选：对比无记忆搜索，以命中率和实验成本评估。
  - 迁移｜从 [AI4AI](#ai4ai) 把方向、空间、评价三类控制权用于科研智能体审计：逐步标注人机决策边界。
- **EvalEvolve**
  - 迁移｜从 [SPU](#spu) 把隐藏实测结果用于动态评测：对比公开答案任务，统计误差、校准度、拒答率和成本。
  - 延续｜[AI4AI](#ai4ai) 留下AI评价器可信性问题：固定预算运行五代，对比独立评价器并测隐藏集增益与退化率。
- **EvolveLRM**
  - 迁移｜从 [RL训练](#item-1) 把能力漂移用于后训练验收：固定多能力题集，报告目标增益、回退率和最差能力降幅。
- **PhysicalEvolve**
  - 延续｜[MolRSI](#molrsi) 尚未把湿实验反馈纳入循环：对比纯计算与实验回灌，测命中率、亲和力和交叉反应。
- **HarnessEvolve**
  - 迁移｜从 [DeepSeek Harness](#deepseek-harness) 把仓库自动封装用于适配器生成：测接入耗时、复用率和任务通过率。
- **PersonalEvolve**
  - 迁移｜从 [DeepSeek Harness](#deepseek-harness) 把临时需求插件化用于个人技能沉淀：选20类重复请求测试复用率与纠错次数。
- **Awesome-RSI**
  - 迁移｜从 [递归自我改进](#ai-ai) 把8讲分类用于资源清单重构：按机制、评测、安全补齐论文、实现与未解问题。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-15/  

