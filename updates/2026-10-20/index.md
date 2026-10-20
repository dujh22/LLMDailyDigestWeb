# 2026-10-20 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进开始形成“执行反馈—经验沉淀—模型更新”的多层闭环：[SenseNova-RoboRSI](#sensenova-roborsi)以冻结参数的执行框架持续改善具身任务，[Personal AI](#personal-ai)则用 Personal LoRA 将个体经验转化为可迁移能力，[MemT 1.0](#memt-1-0-300b-rsi)进一步把长期经验读写纳入模型原生架构。
- 具身智能集中探索世界模型、编程式 Harness 与真实能力边界：[EVO-WAM](#evo-wam)从自想象轨迹中完成“生成—验证—学习”，[HexaShell](#hexashell-vlm)以工具程序控制机器人，而 [GPT-6-Astra具身智能评测](#gpt-6-astra)表明精细接触、状态验证和失败恢复仍是实用化瓶颈。
- 智能体评测从最终结果转向可审计过程：[BizAgentBench](#bizagentbench)暴露成功结果背后的违规执行与工具成本，[Into the Unknown](#into-the-unknown)则显示前沿科研智能体仍普遍缺乏证据充分、要求完备的研究产出。
- 长程智能体系统侧同时推进成本、上下文与可靠性优化：[HiRoute](#hiroute-jev)用 Jev 动态路由快慢模型，[CarryOn](#carryon)以任务对象替代完整历史，[Meta 薄编排器模式](#meta)通过确定性编排和上下文隔离限制故障扩散，[OpenMobile-2](#openmobile-2)则提供可扩展交互环境与训练轨迹。
- 热点延伸方面，今日另有一项交互式视频生成推理加速工作，重点是以缓存和推测采样兼顾生成质量与低延迟。

## 对当前研究的启发
- **Awesome-RSI**：[SenseNova-RoboRSI](#sensenova-roborsi)、[Personal AI](#personal-ai)与 [MemT 1.0](#memt-1-0-300b-rsi)分别覆盖免训练执行改进、参数化经验固化和原生记忆，可据此补充 RSI 系统跨时间尺度的分层分类。
- **RobotEvolve**：[EVO-WAM](#evo-wam)的自想象轨迹筛选与 [SenseNova-RoboRSI](#sensenova-roborsi)的真实执行反馈可以组合成“想象扩展数据—环境验证—经验蒸馏”的具身自进化闭环。
- **MemoryEvolve**：[MemT 1.0](#memt-1-0-300b-rsi)的可训练记忆分支与 [CarryOn](#carryon)的对象化外部记忆提供了参数内外记忆协同、按任务复用并控制上下文成本的具体架构参照。
- **JevEvolve**：[HiRoute](#hiroute-jev)证明 Jev 可利用任务复杂度和上一阶段胜任度动态决定模型升级，为从交互日志持续学习快慢模型路由边界提供了直接应用场景。
- **Groom**：[BizAgentBench](#bizagentbench)对确定性过程违规和工具开销的检查表明，Groom 可进一步把 token 消耗归因到合规执行、无效调用与错误恢复等可审计过程类别。
- **ResearchEvolve**：[Into the Unknown](#into-the-unknown)中所有前沿智能体均未完整达标且常出现无证据声明，说明科研智能体评测应把证据绑定、要求覆盖率与结论可追溯性设为硬门槛。
- **SystemEvolve**：[Meta 薄编排器模式](#meta)展示了将确定性可靠性检查留在小型编排层、将领域推理隔离到专项智能体，可作为降低系统自进化中故障扩散风险的基线架构。
- **EnvironmentEvolve**：[OpenMobile-2](#openmobile-2)的可控应用环境、原生工具和规模化交互轨迹说明，移动端环境可被构造成兼具可执行、可验证与跨应用课程扩展能力的经验生产设施。
- **CodeEvolve**：[Claude Code 以分层审查实现九成代码自产自审](#claude-code)将多智能体审查、风险分级、测试证据和人工审批串成质量闭环，可用于设计编码 Agent 自改进后的分级验证与发布门禁。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-20/  

