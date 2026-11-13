# 2026-11-13 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **长程智能体训练与持续进步评测成为主线**：[TreeOPSD](#treeopsd)以树式信用分配提升深度研究智能体强化学习效果，[RSI 持续进步评测](#rsi-rsibench-data-s-gym)则要求联合审查版本轨迹、计算预算、历史峰值与未见任务泛化，分别补齐“如何进步”与“如何证明进步”。
- **Agent 评测进一步走向真实闭环与抗高估**：[TestPrism](#testprism-coding-agent)揭示单参考实现会将 Coding Agent 测试生成成功率高估一倍以上，[Interactive Visual Gym](#interactive-visual-gym)和[GTAGym](#gtagym-aaa)则把评测扩展到模拟用户交互及真实 AAA 游戏环境。
- **结构化知识与自主研读推动推理能力扩展**：[TOME-Math](#tome-math)从数千本教材提取带课程顺序和证明依赖的监督数据，[强化学习激励大语言模型从长篇教材中自我学习](#item-7)则让模型自主检索、研读并应用长篇知识。
- **系统优化聚焦按需分配推理资源**：[SparseRead](#sparseread-ai)通过意图跟踪与预算门控削减外部内容读取成本，[PISA-E](#pisa-e)按提示动态路由模型集成，[SteerDistill](#steerdistill-llm)利用执行反馈修正量化智能体的失败行为。
- **产品与模型侧出现新的落地信号**：[Personal Agent 的北极星指标](#personal-agent)主张从 DAU 转向事务托管完成率和人工接管频率，[文心 5.5 Flash Preview](#5-5-flash-preview-3d)则以稀疏注意力、MoE 和多 Token 预测强化百万上下文及游戏、3D 开发；热点延伸还涉及跨模态表征对齐、按不确定性切换量化精度和 GPU 二次规划求解。

## 对当前研究的启发
- **AgentTrainEvolve**：[TreeOPSD](#treeopsd)表明长程 Agentic RL 可用树式轮次信用、后验蒸馏和动态残差更新缓解稀疏终局奖励问题。
- **Awesome-RSI**：[RSI 持续进步评测](#rsi-rsibench-data-s-gym)提供了区分持续自改进与预算扩张、基线波动或历史峰值复现的多维审计框架。
- **EvalEvolve**：[TestPrism](#testprism-coding-agent)证明动态评测不能依赖单一参考答案，而应同时引入多样化正确实现与错误实现来测量测试用例的真实判别力。
- **EnvironmentEvolve**：[GTAGym](#gtagym-aaa)展示了将高复杂度商业游戏改造成可执行、可训练 Agent 环境的路径，可用于研究环境复用与自动课程生成。
- **EvolveLLM**：[强化学习激励大语言模型从长篇教材中自我学习](#item-7)说明“自主导航知识源—细粒度奖励—跨域验证”可成为少依赖人工标注的模型自学习闭环。
- **DataEvolve**：[TOME-Math](#tome-math)表明保留教材顺序、证明依赖和来源溯源的数据结构，比单纯扩充数学样本量更适合构造课程化自进化数据。
- **Groom**：[SparseRead](#sparseread-ai)的意图跟踪和预算门控可转化为过程级 token 归因维度，用于判断 Agent 是否把读取预算花在与当前目标相关的证据上。
- **JevEvolve**：[PISA-E](#pisa-e)提供了按提示与成本偏好动态决定模型组合规模的路由范式，可作为快决策模型学习“直接处理或升级慢思考”边界的参考。
- **PersonalEvolve**：[Personal Agent 的北极星指标](#personal-agent)将事务托管量、完成率、长期留存与人工接管率定义为核心指标，为个性化 Agent 的长期进化提供了比活跃度更贴近真实价值的目标函数。
- **GeneralizeEvolve**：[视觉语言模型中的潜意识学习与隐性偏好迁移](#item-14)提示能力迁移评测必须同时检查与任务无关的偏好和措辞是否被隐式继承，避免把隐藏偏差当成泛化收益。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-13/  

