# 2026-10-20 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 具身智能自进化成为今日主线（5 条）：[SenseNova-RoboRSI：统一具身执行框架驱动机器人持续改进](#sensenova-roborsi)以执行反馈和经验沉淀实现冻结参数下的递归改进，[EVO-WAM：世界动作模型从自我想象中迭代进化](#evo-wam)则通过生成、验证并学习想象轨迹减少对专家示范和真实试错的依赖。
- 具身系统的能力边界与工程瓶颈进一步清晰：[HexaShell：探索 VLM 机器人编程智能体能力边界的轻量框架](#hexashell-vlm)显示代码化工具控制可提升双臂操作表现，而[GPT-6-Astra具身智能评测：具备能力但尚未达到实用门槛](#gpt-6-astra)指出状态验证、执行效率和长程恢复仍是落地障碍。
- 智能体基础设施开始围绕记忆与动态路由优化：[MemT 1.0：近300B参数记忆原生模型补齐RSI记忆拼图](#memt-1-0-300b-rsi)验证了可训练原生记忆的规模化潜力，[HiRoute：基于 Jev 的智能模型路由实践](#hiroute-jev)则用任务复杂度和阶段胜任度在长程工作流中动态控制模型成本。
- 智能体评测从最终结果转向过程证据：[BizAgentBench：现实商业场景中的长时程智能体评测](#bizagentbench)揭示成功结果可能掩盖违规执行与高额调用成本，[LiveMACE：演化市场中的智能体过程感知评估](#livemace)也显示金融收益与智能体真实机制能力并不一致。
- 自主科研仍面临明显可靠性上限：[Into the Unknown：开放式科学研究智能体基准](#into-the-unknown)中九种前沿智能体的提交均未满足全部要求，突出证据约束、研究声明可信度和开放式任务评测的缺口。

## 对当前研究的启发
- **RobotEvolve**：[SenseNova-RoboRSI](#sensenova-roborsi)的执行反馈闭环与[EVO-WAM](#evo-wam)的自生成、自验证想象轨迹，可分别作为推理时经验积累和训练时数据回灌两条具身自进化路径。
- **AgentEvolve**：[SenseNova-RoboRSI](#sensenova-roborsi)证明无需修改核心模型参数也能通过统一 Harness、反馈修正和已验证经验沉淀持续提升执行能力。
- **MemoryEvolve**：[MemT 1.0](#memt-1-0-300b-rsi)把长期经验读写内化为可训练记忆分支，为研究参数化记忆与上下文记忆协同及其规模效应提供了直接样本。
- **JevEvolve**：[HiRoute](#hiroute-jev)展示了依据任务复杂度与上一阶段胜任度学习快慢模型切换边界，可直接用于长程 Agent 的低成本动态路由。
- **Groom**：[BizAgentBench](#bizagentbench)与[LiveMACE](#livemace)共同说明最终成功率或收益不足以代表能力，过程违规、工具成本和完整决策轨迹应纳入 token 利用归因。
- **HarnessEvolve**：[HexaShell](#hexashell-vlm)表明极简 Harness 及“编写—执行—修复工具程序”的接口设计本身即可显著改变 VLM 机器人的能力表现与瓶颈分布。
- **ResearchEvolve**：[Into the Unknown](#into-the-unknown)暴露了科研智能体在开放方向续写中缺乏证据支持的问题，提示基准需把论断溯源和全部要求满足度设为硬验证条件。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-20/  

