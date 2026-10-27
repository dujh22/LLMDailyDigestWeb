# 2026-10-27 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进进一步转向“可验证、可泛化、可复现”的系统工程：[RRSI：正则化智能体脚手架的递归自我改进](#rrsi)用修改约束、泄漏筛查和成本感知选择抑制过拟合，[RSIHub：可组合的智能体演化方法框架](#rsihub)则提供统一算子与评测基础设施。
- 在线学习与测试时自进化出现两条代表路线：[ASCENT：智能体将成功经验自蒸馏进权重，实现在线持续学习](#ascent)把验证过的单次成功轨迹写入 LoRA 快权重，[TTPO：无标签测试时策略优化实现自进化](#ttpo)则利用伪标签的错误识别优势，在无真值条件下优化推理策略。
- 数据、代码与科研自动化正在形成端到端闭环：[LegoFlow：智能体自动化代码数据构建与训练评测](#legoflow)贯通任务构建、轨迹生成、训练和评测，[DataMaster：自演进数据飞轮科研智能体](#datamaster)以实验反馈迭代科研数据与方案，[策略内自训练：无数据监督的语言模型自我改进](#item-18)进一步展示了仅从主题描述自造课程和监督信号的可能性。
- Agent 架构与评测更强调削减无效复杂度并拆分能力来源：[Anthropic：谨慎使用子智能体，优先考虑单 Agent + Skills](#anthropic-agent-skills)给出生产侧架构取舍，[Dual Exam：多模态智能体与世界模型的受控评估](#dual-exam)和 [UserArena：长时程购物智能体的交互式用户模拟基准](#userarena)分别通过干预实验与真实轨迹模拟提升诊断有效性。
- 具身与世界模型方向继续走向统一的长程规划和交互：[RynnUnify：统一具身理解、视觉规划与机器人控制的 16B 模型](#rynnunify-16b)把视频预测作为按需调用的推理工具，显示世界模型与 VLA 控制逐步从模块拼接转向统一建模。
- 热点延伸方面，今日低相关性条目集中于多语言安全评测，[TenetBench：条款锚定的俄语专业伦理准则评测语料库](#tenetbench)以具体伦理条款为锚点检验规则理解与遵循。

## 对当前研究的启发
- **Awesome-RSI**：[RRSI](#rrsi)的防泄漏、修改正则化与成本感知选择可作为 RSI 是否真实改进的最低验证规范，[RSIHub](#rsihub)则适合作为方法复现和公平横评的统一底座。
- **CodeEvolve**：[LegoFlow](#legoflow)可直接参考为“代码任务生成—轨迹采集—模型训练—基准反馈—再生成”的自动化进化流水线架构。
- **AgentTrainEvolve**：[ASCENT](#ascent)表明将经过验证的成功轨迹即时蒸馏到 LoRA 快权重，可能成为连接单次环境交互与持续参数进化的轻量方案。
- **GeneralizeEvolve**：[TTPO](#ttpo)利用伪标签更善于识错的非对称性构造无标签优化信号，而 [RRSI](#rrsi)提供了用留出集和分布外评测约束自改进过拟合的互补机制。
- **DataEvolve**：[策略内自训练](#item-18)说明高层主题即可驱动课程、问答和特权推理轨迹的联合生成，可用于探索低人工数据依赖的数据飞轮。
- **ResearchEvolve**：[DataMaster](#datamaster)把实验结果直接反馈到数据集和研究方案迭代，为自主科研系统补上了数据中心型闭环设计。
- **EvalEvolve**：[Dual Exam](#dual-exam)的环境响应固定与动作干预可用于解耦策略和世界模型缺陷，[UserArena](#userarena)的在策略轨迹蒸馏则可提升长时程用户模拟评测的线上效度。
- **SwarmEvolve**：[Anthropic 的实践总结](#anthropic-agent-skills)提示应先证明上下文隔离、并发或工具冲突的必要性再引入子智能体，并把单 Agent + Skills 设为默认强基线。
- **RobotEvolve**：[RynnUnify](#rynnunify-16b)按需调用视频预测来补全未观测状态，为 VLA 中“何时启用世界模型想象”提供了可训练的统一实现路径。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-27/  

