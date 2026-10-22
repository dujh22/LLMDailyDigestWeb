# 2026-10-22 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 长程智能体与递归自我改进成为今日主线：[RSIGame](#rsigame) 以“试玩—诊断—修改—验证”闭环同时迭代作品与开发能力，[CoEvo-RSI](#coevo-rsi) 则进一步让模型与执行框架协同演化，直面 RSI 中的“脑—身体”错配。
- Agent 系统的演化对象继续从模型扩展到脚手架与群体结构：[ScholarEvolve](#scholarevolve-agent-harness) 从科研文献中自动实现、组合和评估算法以持续演化 Harness，[Agensh](#agensh) 展示了最多 1024 个智能体无中心主管协作开发软件的可行性。
- 新模型与真实应用均在强化长程执行能力：[阶跃星辰开放 Step 5 Preview 权重，面向长程 Agent](#step-5-preview-agent) 将百万 token 上下文、上下文压缩训练与可验证环境结合；[S-Agent 2.0](#s-agent-2-0) 和 [FocusGUI](#focusgui-gui) 分别通过持久场景记忆与动态证据压缩改善空间、GUI 智能体的轨迹稳定性。
- 具身智能集中探索世界表征与运行时效率：[Ropedia W0](#ropedia-w0) 利用人类经验构建跨具身长程预测模型，[VPM](#vpm) 以点轨迹学习统一四维动态表征，[VLA-Rolling](#vla-rolling) 则在冻结模型时自适应复用动作尾部以降低控制延迟。
- 泛化与生成模型方面，[PAR](#par) 将状态跟踪泛化到训练长度的 16 倍，[SWIFT](#swift) 展示弱模型外推训练目标的弱到强扩散路线；热点延伸还涉及扩散纠错训练及 RSI、Agentic RL 人才与合作动态，但与核心研究的直接增量有限。

## 对当前研究的启发
- **Awesome-RSI**：[CoEvo-RSI](#coevo-rsi) 表明 RSI 评估不能只追踪模型能力，还应同步度量 Harness 版本、历史继承与检查点合并对长期稳定性的影响。
- **TaskEvolve**：[RSIGame](#rsigame) 提供了可直接借鉴的局部开发闭环与全局质量控制分层，可用于避免任务作品在连续局部修复中整体退化。
- **CodeEvolve**：[RSIGame](#rsigame) 将可执行作品迭代产生的开发经验回灌底层模型，为“代码产物进化—编码能力训练”的双重闭环提供了具体范式。
- **HarnessEvolve**：[ScholarEvolve](#scholarevolve-agent-harness) 展示了从论文检索到算法实现、组合评估的自动闭环，可用于把 Harness 改进从人工工程升级为有证据约束的持续搜索。
- **SwarmEvolve**：[Agensh](#agensh) 的共享仓库、通信系统与上下文看板为千智能体无中心协作提供了可复现实例，也提出了通信拓扑、冲突消解和规模收益的评测问题。
- **MemoryEvolve**：[S-Agent 2.0](#s-agent-2-0) 说明持久化场景记忆应与工具执行形成闭合证据循环，而非仅作为任务历史的被动存储。
- **RobotEvolve**：[Ropedia W0](#ropedia-w0) 与 [VPM](#vpm) 分别从跨本体人类经验和四维点轨迹切入，可为机器人跨具身迁移及世界模型驱动的想象训练补充统一表征。
- **GeneralizeEvolve**：[PAR](#par) 通过进度对齐和隐状态范数锚定实现 16 倍长度泛化，为判断循环模型是否学到可外推算法而非训练长度模式提供了新机制与测试样例。
- **NewModel**：[阶跃星辰开放 Step 5 Preview 权重，面向长程 Agent](#step-5-preview-agent) 将上下文压缩直接纳入端到端训练，值得重点检验其在百万 token 下的有效证据保留率与真实长程任务收益。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-22/  

