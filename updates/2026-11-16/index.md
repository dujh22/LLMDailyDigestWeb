# 2026-11-16 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归改进**
  - [RSI Arena](#rsi-arena)：用等预算自主后训练与人类盲测，分开衡量能力、偏好和安全，发现更受欢迎不代表更强或更安全。
  - [RSI综述](#rsi)：用四类可进化组件和七步验证闭环，把交互经验转成可回归测试、可回滚的长期改进。
- **数据配比**
  - [OptiMer](#optimer)：把各类训练数据造成的参数变化保存为可合并向量，免去反复重训，配比搜索提速15～35倍。
- **热点延伸**：[RSI预测](#rsi-ai)

## 对当前研究的启发
- **Awesome-RSI**
  - 迁移｜从 [RSI Arena](#rsi-arena) 把能力、偏好、安全分开用于改进审计：等预算迭代后分别盲测三类指标。
  - 延续｜[RSI综述](#rsi) 留下跨组件信用分配问题：逐一冻结记忆、工具和工作流，对比增益、退化率与回滚次数。
- **AgentEvolve**
  - 迁移｜从 [RSI综述](#rsi) 把独立验证与回滚用于技能库更新：新技能先跑留出任务和旧任务回归，通过后再入库。
- **DataEvolve**
  - 迁移｜从 [OptiMer](#optimer) 把训练差分向量用于数据配比：各数据源等预算训练向量，再搜索合并权重并与重训对比。
  - 延续｜[OptiMer](#optimer) 留下负权重是否代表选择性遗忘：允许有符号合并，测目标增益、源能力保留率和困惑度。
- **EvolveLRM**
  - 延续｜[OptiMer](#optimer) 尚未覆盖后训练：在同一基座上分别训练推理数据向量，比较合并与混合重训的得分和成本。
- **EvalEvolve**
  - 迁移｜从 [RSI Arena](#rsi-arena) 把开放盲测用于动态评测：隐藏迭代版本，分别收集正确性、偏好与安全判断。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-16/  

