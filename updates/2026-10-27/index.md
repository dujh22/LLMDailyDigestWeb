# 2026-10-27 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进开始从“生成修改”转向“可靠验证与泛化”： [RRSI](#rrsi) 用修改约束、泄漏筛查和成本感知选择抑制过拟合，[RSI 递归之桥](#rsi) 则将验证预算与证据标准明确为 RSI 的核心工程边界。
- 智能体演化基础设施趋向模块化和闭环化：[RSIHub](#rsihub) 以可组合算子和统一评测底座支持演化方法复现比较，[LegoFlow](#legoflow) 进一步让编码智能体自主编排数据、轨迹、训练和评测全流程。
- 在线自适应与无标签自训练取得集中进展：[ASCENT](#ascent) 将单次任务中的成功轨迹蒸馏进 LoRA 快权重，[TTPO](#ttpo) 借助错误识别更可靠的伪标签开展测试时策略优化，[策略内自训练](#item-18) 则展示了仅凭高层主题自造课程与监督信号的路径。
- 数据自进化覆盖从通用合成到科研闭环：[AutoData](#autodata) 通过多智能体流程动态调整任务难度与提示，[DataMaster](#datamaster) 以实验反馈迭代数据集和研究方案，形成端到端科研数据飞轮。
- Agent 系统设计呈现“先简后繁”的工程判断：[Anthropic：谨慎使用子智能体，优先考虑单 Agent + Skills](#anthropic-agent-skills) 强调渐进披露工具通常优于复杂多智能体架构，而 [Dual Exam](#dual-exam) 通过解耦动作选择与状态演化揭示智能体—世界模型耦合瓶颈。
- 具身方向继续推进统一模型与长程执行：[RynnUnify](#rynnunify-16b) 统一具身理解、视觉规划和控制，[HiSTEVE 1.0](#histeve-1-0-vla) 则以分层编排和结构化记忆支持开放世界长程任务；热点延伸还关注多语言专业伦理评测。

## 对当前研究的启发
- **Awesome-RSI**：RRSI 的泄漏筛查、修改正则化与成本感知选择结合“递归之桥”的证据标准，可直接转化为 RSI 工作的可靠改进准入机制。
- **HarnessEvolve**：RSIHub 的声明式可变资源和统一执行评测底座，为隔离模型、脚手架与评测配置影响并公平比较演化方法提供了可复用架构。
- **CodeEvolve**：LegoFlow 将代码任务构建、轨迹生成、训练和基准反馈封装为可由编码 Agent 自主重组的闭环，可作为软件工程 Agent 自训练流水线的工程参考。
- **AgentTrainEvolve**：ASCENT 证明经验证的单次成功轨迹可在线蒸馏到 LoRA 快权重，为把长程 Agent 交互经验低成本转化为参数更新提供了具体方案。
- **GeneralizeEvolve**：TTPO 的无标签策略优化与 RRSI 的留出集、分布外筛选可组合为“测试时适应—泛化验收”流程，降低自进化对伪标签和训练任务的过拟合。
- **DataEvolve**：AutoData 的难度自调节、策略内自训练的零数据课程生成和 LegoFlow 的评测反馈闭环，共同给出了生成、筛选、训练、再生成的数据飞轮组件。
- **ResearchEvolve**：DataMaster 将研究构想、实验执行、数据迭代和结论输出串成反馈闭环，可用于验证科研智能体是否真正依据实验结果修正方案。
- **SystemEvolve**：Anthropic 的实践提示系统演化不应默认增加子智能体，而应先搜索单 Agent 的 Skills、工具披露和上下文配置，仅在并发或上下文隔离收益明确时扩展拓扑。
- **RobotEvolve**：RynnUnify 的按需视频预测与 Dual Exam 的智能体—世界模型解耦评测，可分别作为世界模型调用策略和耦合失效诊断的设计依据。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-27/  

