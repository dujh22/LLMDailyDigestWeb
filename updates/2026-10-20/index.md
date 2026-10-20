# 2026-10-20 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 具身自进化形成“执行反馈—想象数据—经验回灌”主线：[SenseNova-RoboRSI](#sensenova-roborsi)以冻结模型配合统一 Harness 持续改进执行，[EVO-WAM](#evo-wam)则用“想象—验证—学习”闭环提升未见任务能力。
- 长期记忆开始从外挂检索走向原生状态与参数化沉淀：[MemT 1.0](#memt-1-0-300b-rsi)把可训练记忆分支扩展至近 300B 参数，[通衍灵智 Personal AI](#personal-ai)则以 Personal LoRA 将业务反馈持续写入专属模型。
- 智能体评测更强调长程过程、证据与真实约束：[BizAgentBench](#bizagentbench)揭示结果正确会掩盖违规执行和工具成本，[Into the Unknown](#into-the-unknown)则显示前沿科研智能体仍普遍缺乏可靠证据支撑。
- 系统工程聚焦低成本路由、轻量 Harness 与职责隔离：[HiRoute](#hiroute-jev)以 Jev 动态切换模型，[HexaShell](#hexashell-vlm)通过程序生成与修复控制机器人，[Meta 薄编排器](#meta)则用确定性路由隔离专项子智能体。
- 热点延伸共 1 条，关注以推测采样、预测缓存和增量交付降低交互式视频生成延迟。

## 对当前研究的启发
- **RobotEvolve**：[EVO-WAM](#evo-wam)表明无需新增专家示范或真实环境试错，也可通过世界模型自生成并执行验证轨迹构造具身数据飞轮。
- **AgentEvolve**：[SenseNova-RoboRSI](#sensenova-roborsi)验证了冻结核心模型、仅沉淀执行反馈与成功交互经验即可持续提升部署后智能体能力。
- **MemoryEvolve**：[MemT 1.0](#memt-1-0-300b-rsi)提供了将动态矩阵状态、可训练记忆与多存储路由结合的原生记忆架构，可用于研究参数化与非参数化经验协同。
- **Awesome-RSI**：[SenseNova-RoboRSI](#sensenova-roborsi)与[MemT 1.0](#memt-1-0-300b-rsi)共同补齐了 RSI 中执行闭环和持久记忆两个关键组件，适合作为系统级案例纳入清单。
- **JevEvolve**：[HiRoute](#hiroute-jev)给出了以任务复杂度和阶段胜任度为信号的快慢模型路由实例，可进一步从真实工作流日志学习升级边界。
- **EvalEvolve**：[BizAgentBench](#bizagentbench)证明动态长程评测应同时设置确定性过程检查、规则合规性与工具成本指标，而不能只看最终成功率。
- **Groom**：[BizAgentBench](#bizagentbench)可直接借鉴其过程检查设计，将 token 和工具开销归因到违规步骤、无效尝试及重复调用。
- **ResearchEvolve**：[Into the Unknown](#into-the-unknown)显示科研智能体的核心瓶颈不是论文形式完整性，而是研究声明的证据覆盖与需求逐项满足，可据此设计过程门禁。
- **HarnessEvolve**：[HexaShell](#hexashell-vlm)说明极简 Harness 也能显著释放 VLM 的机器人编程能力，同时适合作为量化 Harness 对模型排名影响的对照框架。
- **SystemEvolve**：[Meta 薄编排器](#meta)提示生产系统可将确定性路由和可靠性检查固定在薄控制层，把可变推理封装进上下文隔离的专项智能体，以限制故障扩散。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-20/  

