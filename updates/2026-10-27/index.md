# 2026-10-27 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进进一步从概念走向可验证系统：[Infinity Machine](#infinity-machine)展示了可演化脚手架在真实科研问题上的突破与评分器利用风险，[RRSI](#rrsi)以正则化和成本感知选择抑制过拟合，[RSIHub](#rsihub)提供统一的演化算子与评测基础设施，[AREX-2](#arex-2)则验证了长程反思训练的跨任务迁移。
- Agent 训练侧聚焦“经验如何稳定转化为提升”：[ASCENT](#ascent)将单次在线成功轨迹自蒸馏进快权重，[面向长程 LLM 智能体的多尺度策略优化](#llm-3)结合轮次与词元级信用分配，[LegoFlow](#legoflow)进一步把数据构建、轨迹生成、训练和评测连成可自主编排的闭环。
- 自主科研开始强调可复用发现与机器可检验性：[Auto-Research Arena](#auto-research-arena)用统一环境评估多目标研究能力，[智能体算法设计：在 Lean 中提出、形式化并证明进化算法运行时界](#lean)则将算法发现推进到形式化证明运行时改进。
- 新模型与快决策架构同步演进：[OpenAI 发布 GPT-6.1 Terra](#openai-gpt-6-1-terra)强化低成本电脑操作，[NUS推出原生决策架构Jeva](#nus-jeva)探索非自回归候选决策，但[Jev 风格 System One 结构能否降低选择偏差？](#jev-system-one)表明整体准确率稳定并不等于对选项重排鲁棒。
- 长程系统优化覆盖控制、适应与资源核算：[EBench评测前沿智能体](#ebench)揭示直接控制与策略调用的切换瓶颈，[OpTTA](#optta)以乐观测试时适应改善分布偏移下的世界模型规划，而[编码智能体上下文的物理成本](#item-67)指出删减上下文可能因破坏前缀缓存而增加实际算力和能耗。
- 热点延伸方面，低相关条目主要是[TenetBench](#tenetbench)对俄语专业伦理准则遵循的条款锚定评测，反映多语言安全评估的持续扩展。

## 对当前研究的启发
- **Awesome-RSI**：[Infinity Machine](#infinity-machine)与[RRSI](#rrsi)共同表明，RSI 清单应把隔离执行、留出集验证、评分器防利用和成本感知选择列为判断真实改进的核心维度。
- **HarnessEvolve**：[RSIHub](#rsihub)的声明式可变资源和统一执行评估接口，可直接借鉴为可组合、可公平复现的 harness 演化实验层。
- **AgentTrainEvolve**：[ASCENT](#ascent)与[面向长程 LLM 智能体的多尺度策略优化](#llm-3)分别提供成功轨迹在线蒸馏和轮次—词元多尺度信用分配，可用于提升长程交互经验的参数化效率。
- **CodeEvolve**：[LegoFlow](#legoflow)可作为编码 Agent 自动构造任务、生成轨迹、训练并依据评测反馈迭代的端到端数据飞轮底座。
- **ResearchEvolve**：[Auto-Research Arena](#auto-research-arena)和 Lean 形式化算法设计工作说明，自主科研评测应同时检查发现能否复用以及结论能否被机器验证，而不只评价最终报告。
- **JevEvolve**：[Jev 风格 System One 结构能否降低选择偏差？](#jev-system-one)提示 Jev 类模型必须将候选置换、答案缺席和证据不足识别纳入基础评测，避免用平均准确率掩盖决策脆弱性。
- **RobotEvolve**：[EBench评测前沿智能体](#ebench)与[OpTTA](#optta)提示具身系统可联合学习“何时直接控制、何时调用专用策略”并在测试时针对当前规划目标适应世界模型。
- **Groom**：[编码智能体上下文的物理成本](#item-67)提供了可直接采用的质量门控资源核算方法，应把前缀缓存失效、预填充计算和能耗纳入过程级 token 利用评测。
- **MemoryEvolve**：[AMIE](#amie)将记忆内容与访问状态解耦，提供了一条只演化检索权重、无需重写记忆或重训宿主系统的轻量持续适应路径。
- **DataEvolve**：[AutoData](#autodata)与[LegoFlow](#legoflow)表明可把难度调节、提示优化和下游评测反馈统一进合成数据闭环，以持续对准模型能力边界。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-27/  

