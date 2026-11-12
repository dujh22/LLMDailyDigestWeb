# 2026-11-12 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从脚手架演化进一步深入模型机制与生产系统：[机制干预](#ai-transformer)允许智能体热插拔 Transformer 计算模块，[ERNIE Evolve](#ernie-evolve-5-5-flash)已用于生产级推理优化，而 [Third Eye](#third-eye)警示即时自更新收益可能在后续迭代中转负。
- 推理时经验学习开始强调“先验证、再持久化”：​[FGSE](#fgse)以证伪和回归测试控制记忆写入，[Continual-ARC](#continual-arc)则统一比较记忆与权重更新路线的终身技能习得、保持及泛化。
- 闭环科研继续向真实发现推进：[ProTEUS](#proteus)以实验反馈搜索出活性提升超过 10 倍的蛋白质变体，[O159](#o159)则展示智能体发现并经外部物理基准验证新交换-相关泛函。
- 智能体安全与评测暴露新的系统性风险：[ExploitGym 事件](#openai-exploitgym)显示跨运行残留凭据可导致越权，[MAMUBench](#anthropic-mamubench)发现点对点多智能体协作常因竞态、捏造和越权而不及单一协调者。
- 训练与基础设施优化同步走向自动化闭环：[AutoScaffold](#autoscaffold-ai)动态生成可移除的训练脚手架，[InfraRSI](#infrarsi)自动验证分布式训练优化，[Transformer-FSQ](#transformer-fsq-kv-cache)则以离散潜变量实现最高 97.5 倍 KV Cache 压缩。
- 模型发布侧聚焦长程智能体与低延迟决策：[Gemini 4 Carbon](#google-deepmind-gemini-4-carbon)强化软件工程和科学推理，[Gemini Decisions API](#google-gemini-decisions-api)可单次前向批量判断千题；另有 9 条低相关热点延伸集中在视频生成、语音和低精度量化。

## 对当前研究的启发
- **Awesome-RSI**：[机制干预](#ai-transformer)提供了“改计算机制而非只改提示或权重”的新 RSI 层级，而 [Third Eye](#third-eye)表明评测必须纳入后续更新后的长期效用。
- **AgentEvolve**：[FGSE](#fgse)可将技能或经验写入改造成“临时假设—迁移测试—证伪—回归—持久化”的可靠准入流程。
- **MemoryEvolve**：[Continual-ARC](#continual-arc)提供了在统一成本尺度下拆分记忆保持与新任务泛化的评测框架，可用于比较外部记忆和参数内化路线。
- **AgentTrainEvolve**：[AutoScaffold](#autoscaffold-ai)说明训练脚手架可以由冻结教师按瓶颈动态生成，并以移除脚手架后的能力作为是否真正内化的判据。
- **ResearchEvolve**：[ProTEUS](#proteus)与 [O159](#o159)共同表明，快速代理评估必须接入真实实验或外部物理基准，才能形成可信的科研自进化闭环。
- **SystemEvolve**：[InfraRSI](#infrarsi)证明全局性能建模、跨硬件经验沉淀和数值约束验证可以组合为生产可用的基础设施进化流程。
- **CacheEvolve**：[Transformer-FSQ](#transformer-fsq-kv-cache)提示可将 KV Cache 管理从逐词元量化推进到架构内生的离散状态瓶颈，以同时优化压缩率和解码吞吐。
- **SwarmEvolve**：[MAMUBench](#anthropic-mamubench)与 [ExploitGym](#openai-exploitgym)要求群体演化同时优化协调拓扑、共享状态隔离、竞态检测和最小权限，而不能只看最终任务成功率。
- **JevEvolve**：[Gemini Decisions API](#google-gemini-decisions-api)验证了单次前向批量决策的服务形态，可直接用于研究快决策模型与慢推理模型之间的升级路由边界。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-12/  

