# 2026-10-08 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **智能体 Harness 成为自我改进的核心载体**：至少 6 项工作从不同环节推进脚手架演化，[RRSI](#rrsi-harness)用正则化抑制递归迭代中的过拟合与复杂度膨胀，[RSR](#rsr)将专用脚手架经验重写为通用训练轨迹，[Raven](#raven-harness-harness)则进一步自动构建和编排可组合 Harness。
- **长期运行的稳定性从“存更多”转向“验证状态与反馈”**：[自生成反馈破坏测试时训练的长期稳定性](#item-26)揭示闭环更新的退化风险，[超越记忆：用显式信念状态驱动长时程智能体](#item-41)以持续验证和修复信念状态维持任务一致性，[RealCompanion](#realcompanion)则用最长 120 天真实对话检验远程记忆与过度推断。
- **评测与环境开始随智能体能力共同演化**：[AutoSciBench](#autoscibench)依据求解轨迹和评判反馈持续生成科学任务，[HERA](#hera)协同演化脚手架与环境以改善可靠拒答，[MiniCorp](#minicorp-ai)则提供可回放、可反事实的多智能体企业环境。
- **推理研究强调结构先验、可验证性与跨域迁移**：[SAGE](#sage)借助代数与双曲结构信号显著提高长程推理的 Lean 验证通过率，[NAT-ARC](#nat-arc-arc)展示自然图像预训练先验向抽象视觉推理迁移的潜力，[AlphaGo作者：LLM尚未掌握可审计的搜索式推理](#alphago-llm)则强调显式状态、搜索和证据更新。
- **自主科研出现可验证的算法发现案例**：[语言模型发现更快的分子几何弛豫算法 AutoSella](#autosella)通过自动改写优化器减少量子化学力评估次数，相比单纯生成研究文本，更接近“提出改进—执行验证—跨任务检验”的科研闭环。
- **多智能体扩展的收益边界与风险更加清晰**：[万级多智能体扩展：能力增益、协作机制与对齐风险](#item-7)指出群体收益主要来自并行测试时计算且通常次线性，而 [Raven](#raven-harness-harness)展示了通过模块化 Harness 编排专业智能体的另一条扩展路径。

## 对当前研究的启发
- **Awesome-RSI**：[RRSI](#rrsi-harness)与[自生成反馈破坏测试时训练的长期稳定性](#item-26)共同表明，RSI 闭环应同时加入复杂度正则和独立真实数据验证，不能仅依赖自生成反馈判断每轮改进。
- **HarnessEvolve**：[RRSI](#rrsi-harness)、[RSR](#rsr)与[EVISKILL](#eviskill)分别提供了防过拟合选择、跨脚手架轨迹重写和证据化技能沉淀机制，可组合成“生成—筛选—验证—复用”的 Harness 演化流水线。
- **EvolveLLM**：[RSR](#rsr)说明可将脚手架探索产生的成功轨迹转化为模型训练数据，而[自生成反馈破坏测试时训练的长期稳定性](#item-26)提示更新前必须引入独立分布验证以避免长期闭环退化。
- **EvolveLRM**：[SAGE](#sage)表明将可计算的任务结构直接注入探索与过程监督，可能比单纯扩大采样预算更有效地改善长程推理信用分配。
- **LogicEvolve**：[NAT-ARC](#nat-arc-arc)提示可把视觉预训练先验作为抽象推理的初始化来源，而可审计搜索观点进一步要求用显式状态和验证器区分结构迁移与模式匹配。
- **MemoryEvolve**：[超越记忆：用显式信念状态驱动长时程智能体](#item-41)与[RealCompanion](#realcompanion)提示记忆系统应把“事实存储”和“当前信念状态”分离，并重点评测远程证据相关性及无依据人格推断。
- **EvalEvolve**：[AutoSciBench](#autoscibench)展示了以失败轨迹和评判反馈驱动任务生成、难度校准与基准持续更新的直接实现路径。
- **EnvironmentEvolve**：[HERA](#hera)和[MiniCorp](#minicorp-ai)说明环境演化不仅要调节任务难度，还应同步演化不确定性、外部动态及可回放反事实验证机制。
- **SwarmEvolve**：[万级多智能体扩展](#item-7)与[Raven](#raven-harness-harness)共同提示，应把研究重点从盲目增加智能体数量转向通信成本、任务可并行性和模块编排结构的联合优化。
- **ResearchEvolve**：[AutoSella](#autosella)提供了自主科研系统的高价值模板，即围绕可执行对象自动提出算法修改，并以收敛性、成本和跨实例泛化作为机器可验证反馈。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-08/  

