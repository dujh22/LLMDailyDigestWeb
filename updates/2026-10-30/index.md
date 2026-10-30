# 2026-10-30 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进正从概念验证走向可审计实验系统：[RSI-Master](#rsi-master) 以研究 DAG 管理自主后训练，[RSI Arena](#rsi-arena) 则揭示人类偏好提升不等于能力与安全同步改善，[Hermit](#cmu-hermit-harness-rsi) 进一步把持续进化闭环外置到统一 Harness 层。
- 环境与具身自进化加速规模化：[WorkRover](#workrover) 用执行反馈递归修复长程协同环境，[Gym-Anything](#gym-anything) 以创建—审计闭环生成 200 个机器人仿真环境，[CEL](#cel) 则在 96 台真机上验证群体经验共享与持续学习。
- 推理训练同时推进数据、探索与边界认知：[LongZero](#longzero) 实现零外部数据的长上下文任务自合成，[PSN-RLVR](#psn-rlvr) 以轨迹一致的参数扰动恢复探索，而 [RLVR 无免费午餐](#rlvr-pass-1-pass-k) 从理论上指出 pass@1 增益可能以 pass@k 和策略多样性为代价。
- 智能体评测明显转向过程证据与环境审计：[EnvOS](#envos) 区分智能体失误、环境变化和评分器错误，[VeriCUA](#vericua) 通过动态取证验证计算机操作结果，[PAPERBENCHX](#paperbenchx) 则暴露科研智能体生成可独立验证证据的能力缺口。
- 自主科研与持续学习出现更强闭环：[MoLRSI](#molrsi) 联合改进科研工作流、模型与持久记忆并获得湿实验验证，Google 的[“睡眠”机制](#google)则通过周期性知识巩固缓解持续学习中的灾难性遗忘。
- 新模型侧以开放权重和垂直能力为主，[Mistral Large 4](#mistral-1t-large-4) 开放 1T 参数多模态模型权重；热点延伸集中于流式音视频分离、全向视频生成、指令容量测量和模型失控风险评估，但相关性较低，不列入重点条目。

## 对当前研究的启发
- **Awesome-RSI**：[RSI-Master](#rsi-master)与[RSI Arena](#rsi-arena)表明 RSI 基准应同时记录实验谱系、作弊风险、通用能力和安全变化，不能以单一偏好分数判定“持续改进”。
- **HarnessEvolve**：[Hermit](#cmu-hermit-harness-rsi)提供了将训练、评估、部署和反馈学习统一到可插拔 Adapter 的实现路径，而[EnvOS](#envos)可补充环境认证与事后审计层。
- **EnvironmentEvolve**：[WorkRover](#workrover)的递归修复和[Gym-Anything](#gym-anything)的对抗式创建—审计可组合成“生成、执行、验错、修复、再验证”的环境进化流水线。
- **RobotEvolve**：[CEL](#cel)证明跨机器人共享失败与成功经验能够扩展到近百台真机，可将群体经验池纳入现有 sim-to-real 数据回灌闭环。
- **EvolveLRM**：[PSN-RLVR](#psn-rlvr)与[RLVR 无免费午餐](#rlvr-pass-1-pass-k)共同提示训练时应联合监控 pass@1、pass@k、策略熵和解法多样性，并以参数空间探索缓解能力集中化。
- **DataEvolve**：[LongZero](#longzero)展示了无需教师和外部语料的长上下文任务生成闭环，但“合成数据预预训练”的负结果提示必须做计算量对齐与验证筛选。
- **EvalEvolve**：[EnvOS](#envos)、[VeriCUA](#vericua)和[PAPERBENCHX](#paperbenchx)说明下一代动态评测应把环境状态认证、过程取证与独立复现实验作为统一 ground truth。
- **Groom**：[VeriCUA](#vericua)的 GUI—代码组合证据和 EnvOS 的错误归因机制可直接用于把 token 消耗关联到可验证的中间进展、恢复行为与最终证据。
- **ResearchEvolve**：[MoLRSI](#molrsi)证明工作流、架构和记忆联合 RSI 能产生实验成果，而[PAPERBENCHX](#paperbenchx)提示项目评测必须要求跨领域独立复现而非只审阅论文文本。
- **MemoryEvolve**：Google 的[“睡眠”机制](#google)可借鉴为记忆系统的周期性巩固阶段，用自生成回放、蒸馏和容量扩展协调新知识吸收与旧知识保持。
- **NewModel**：[Mistral Large 4](#mistral-1t-large-4)值得重点分析其 1T 稀疏多模态架构、低 Token 配方及限制 MaaS 转售的开放权重许可对部署生态的影响。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-30/  

