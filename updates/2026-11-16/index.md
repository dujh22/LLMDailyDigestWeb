# 2026-11-16 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **改进审计**
  - [RSI Arena](#rsi-arena)：用等预算沙箱和人类盲测指导自主后训练，并分开衡量真实能力、受欢迎度与安全性，避免把迎合误判为进步。
- **进化框架**
  - [RSI综述](#rsi)：用四类可进化组件和七步验证闭环，把智能体交互经验转化为可复用、可回滚的长期改进。
- **数据配比**
  - [OptiMer](#optimer)：将各类训练数据产生的参数变化保存为可合并向量，免去反复重训即可搜索配比，提速15～35倍。

## 对当前研究的启发
- **Awesome-RSI**
  - 迁移｜从 [RSI Arena](#rsi-arena) 把能力、偏好、安全分离用于改进审计：固定起点与预算，分别盲测三类指标。
  - 延续｜[RSI Arena](#rsi-arena) 仅测单一基座且每个智能体运行一次：跨三种基座重复五次，检验改进均值与方差。
- **AgentEvolve**
  - 迁移｜从 [RSI综述](#rsi) 把七步闭环用于技能库更新：经验先归因、独立回归测试，再合并或回滚。
  - 延续｜[RSI综述](#rsi) 未解决跨组件信用分配：逐项消融记忆、工具和工作流，以任务成功率归因增益。
- **DataEvolve**
  - 迁移｜从 [OptiMer](#optimer) 把训练差分向量用于数据配比搜索：分源训练向量后优化权重，再仅重训最优组合。
  - 延续｜[OptiMer](#optimer) 尚未验证负权重是否代表选择性遗忘：对照数据删除与反向向量，测目标增益和旧能力损失。
- **EvolveLRM**
  - 延续｜[OptiMer](#optimer) 尚未覆盖后训练：在SFT与RL数据源上比较向量合并和真实混训的得分误差、成本与泛化。
- **EvalEvolve**
  - 迁移｜从 [RSI Arena](#rsi-arena) 把开放盲测用于动态评测：隐藏系统版本，持续采集偏好并同步独立能力与安全测试。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-16/  

