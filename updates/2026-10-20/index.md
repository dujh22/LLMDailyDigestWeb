# 2026-10-20 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 具身自进化形成“执行反馈—想象数据—工具编程”三条路径：[SenseNova-RoboRSI](#sensenova-roborsi)以冻结参数的统一 Harness 沉淀交互经验，[EVO-WAM](#evo-wam)从自生成视频—动作轨迹中学习，[HexaShell](#hexashell-vlm)则通过编写和修复工具程序提升机器人控制能力。
- 长程智能体的状态与成本优化进一步系统化：[MemT 1.0](#memt-1-0-300b-rsi)验证可训练原生记忆分支的规模化可行性，[CarryOn](#carryon)以对象化任务上下文替代完整历史，[HiRoute](#hiroute-jev)利用 Jev 动态切换模型以降低调用成本。
- 智能体评测从最终得分转向真实过程与动态环境：[BizAgentBench](#bizagentbench)检查商业任务中的违规步骤和工具开销，[LiveMACE](#livemace)用实时市场及完整轨迹揭示收益与能力的错位。
- 自主科研仍存在明显可靠性缺口：[Into the Unknown](#into-the-unknown)中九种前沿智能体的提交均未满足全部开放式科研要求，缺乏证据支持的研究声明尤为普遍。
- 训练环境继续向可扩展、可执行和原生工具融合演进，[OpenMobile-2](#openmobile-2)以可控移动应用环境和大规模交互轨迹训练跨应用长程智能体；热点延伸则关注交互式视频生成的推测采样与低延迟交付。

## 对当前研究的启发
- **RobotEvolve**：[SenseNova-RoboRSI](#sensenova-roborsi)与[EVO-WAM](#evo-wam)分别提供参数冻结的执行经验沉淀和无需真实试错的想象轨迹回灌，可组合为低成本具身持续改进闭环。
- **AgentEvolve**：[SenseNova-RoboRSI](#sensenova-roborsi)证明统一 Harness 可将验证后的交互经验递归复用，而[CarryOn](#carryon)给出了以任务对象承载这类经验、避免历史上下文无限膨胀的运行时设计。
- **MemoryEvolve**：[MemT 1.0](#memt-1-0-300b-rsi)的参数化原生记忆与[CarryOn](#carryon)的对象化外部记忆构成两种互补方案，可用于比较写入、复用、成本和遗忘特性。
- **JevEvolve**：[HiRoute](#hiroute-jev)直接验证了以任务复杂度和阶段胜任度为信号的快慢模型路由，可进一步利用执行日志持续校准升级边界。
- **Groom**：[BizAgentBench](#bizagentbench)与[LiveMACE](#livemace)表明最终成功率或收益会掩盖违规、冗余和偶然成功，可将其确定性过程检查与完整轨迹诊断纳入 token 利用归因。
- **ResearchEvolve**：[Into the Unknown](#into-the-unknown)揭示开放式科研智能体的核心短板并非论文形式生成，而是需求覆盖和证据支撑，适合据此设计声明—证据绑定的过程验证器。
- **EnvironmentEvolve**：[OpenMobile-2](#openmobile-2)展示了可控应用、原生工具和规模化轨迹的一体化环境方案，可作为构建可执行、可验证移动任务生成器的参考。
- **HarnessEvolve**：[HexaShell](#hexashell-vlm)说明极简的代码生成—执行—修复接口即可显著释放 VLM 具身能力，也提示评测必须披露 Harness 并单独度量其增益。
- **Awesome-RSI**：[SenseNova-RoboRSI](#sensenova-roborsi)和[MemT 1.0](#memt-1-0-300b-rsi)分别补充了外部执行闭环与内部可训练记忆两类 RSI 机制，值得纳入分类并比较长期迭代稳定性。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-20/  

