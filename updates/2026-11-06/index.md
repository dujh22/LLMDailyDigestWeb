# 2026-11-06 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **科研智能体评测走向真实全流程与细粒度判断**：高相关工作 [FrontierPhysics：端到端物理研究智能体评测基准](#frontierphysics) 用 56 项真实任务检验端到端科研能力，[CLAIMNOV：基于原子主张的科研创意新颖性评估](#claimnov) 则将新颖性判断落实到可检索、可举证的原子主张。
- **推理系统开始显式管理计算与控制接口**：[StartLux-Decision：按需推理与概率校准](#startlux-decision) 以校准概率决定何时追加思考，[TAC-CoT：交错显式 Token 增强工具化隐式思维链](#tac-cot-token) 为隐式推理加入可观测的工具调用接口，[清华、米哈游开源 GameScaling 系列模型，迈向通用游戏智能](#gamescaling) 则探索规模化训练下的通用游戏推理与决策。
- **强化学习后的能力巩固与信用分配成为焦点**：[在策略蒸馏用于强化学习后能力巩固的泛化局限](#item-14) 揭示分布内能力保持可能掩盖分布外遗忘，[TurnWise：回合级信用分配推进流式视频强化学习](#turnwise) 则以回合级优化改善连续交互训练信号。
- **具身智能同时推进原生策略架构与真实数据飞轮**：[NEO-VLA：从像素到动作的原生视觉-语言-动作策略](#neo-vla) 让视觉与语言表征在主干中联合演化，[PyRUA-DataFarm：LLM 远程操作者驱动的真实场景机器人数据采集](#pyrua-datafarm-llm) 则尝试用 LLM 操作者降低真机数据采集成本。
- **热点延伸覆盖长时程世界模型、三维视觉与 AI 基础设施**：低相关性条目集中于分钟级游戏交互数据、循环式多视图三维求解、光学数据中心预测控制及未知游戏实时解说，显示长程环境建模与实时系统仍在持续升温。

## 对当前研究的启发
- **JevEvolve**：[StartLux-Decision：按需推理与概率校准](#startlux-decision) 可直接用于学习“快决策还是升级慢思考”的校准路由边界，在受控风险下压低平均延迟。
- **GeneralizeEvolve**：[在策略蒸馏用于强化学习后能力巩固的泛化局限](#item-14) 表明能力巩固不能只测分布内保持率，应加入分布外遗忘测试，并评估基础能力回放与几何补丁。
- **ResearchEvolve**：[FrontierPhysics：端到端物理研究智能体评测基准](#frontierphysics) 提供了覆盖调研、规划、实验和写作的真实任务模板，可用于定位科研闭环中推理严谨性与专家直觉的具体瓶颈。
- **EvalEvolve**：[CLAIMNOV：基于原子主张的科研创意新颖性评估](#claimnov) 的同维度检索、分级蕴含和证据画像可用于构建更可审计、且不易误伤增量创新的动态科研评测。
- **AgentTrainEvolve**：[TurnWise：回合级信用分配推进流式视频强化学习](#turnwise) 提示多轮 Agentic RL 可将整轨奖励下沉到回合级，以减少冗余动作并强化真正影响后续结果的响应。
- **RobotEvolve**：[PyRUA-DataFarm：LLM 远程操作者驱动的真实场景机器人数据采集](#pyrua-datafarm-llm) 与 [NEO-VLA：从像素到动作的原生视觉-语言-动作策略](#neo-vla) 可组合成“低成本自主采集—原生 VLA 回灌”的真实世界数据闭环。
- **LogicEvolve**：[TAC-CoT：交错显式 Token 增强工具化隐式思维链](#tac-cot-token) 为兼顾隐式推理效率和过程可控性提供了中间路线，可重点检验显式接口是否提升逻辑忠实度与可验证性。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-06/  

