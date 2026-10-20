# 2026-10-20 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 具身智能自进化形成“执行反馈—想象数据—能力评测”主线（5 条）：[SenseNova-RoboRSI：统一具身执行框架驱动机器人持续改进](#sensenova-roborsi)以冻结参数的 Harness 闭环积累经验，[EVO-WAM：世界动作模型从自我想象中迭代进化](#evo-wam)则从自生成视频—动作轨迹中学习；[GPT-6-Astra具身智能评测：具备能力但尚未达到实用门槛](#gpt-6-astra)与[HexaShell：探索 VLM 机器人编程智能体能力边界的轻量框架](#hexashell-vlm)进一步暴露状态验证、长程恢复和精密接触操作瓶颈。
- 长时程智能体的系统优化转向记忆、上下文与模型路由协同：[MemT 1.0：近300B参数记忆原生模型补齐RSI记忆拼图](#memt-1-0-300b-rsi)探索模型内部原生记忆，[CarryOn：面向长时程智能体的对象化上下文运行时](#carryon)以任务对象压缩外部上下文，[HiRoute：基于 Jev 的智能模型路由实践](#hiroute-jev)则通过快决策动态控制模型成本。
- 智能体评测更强调真实动态环境与可审计过程（3 条）：[BizAgentBench：现实商业场景中的长时程智能体评测](#bizagentbench)揭示“结果正确”可能掩盖违规与浪费，[LiveMACE：演化市场中的智能体过程感知评估](#livemace)显示最终收益不等于真实能力，[Into the Unknown：开放式科学研究智能体基准](#into-the-unknown)则暴露科研智能体普遍缺乏证据支撑。
- 训练环境与经验生产继续规模化：[OpenMobile-2：以可扩展环境与原生工具训练移动智能体](#openmobile-2)结合可控应用环境和混合工具生成长程轨迹，[Scene-Designer：智能体驱动的 3D 室内场景生成](#scene-designer-3d)通过批评数据、强化学习与测试时反馈提升场景有效性。
- 热点延伸集中在生成系统优化：交互式视频生成开始用推测采样、预测缓存和增量交付兼顾大窗口质量与实时响应。

## 对当前研究的启发
- **RobotEvolve**：[SenseNova-RoboRSI](#sensenova-roborsi)与[EVO-WAM](#evo-wam)分别验证了冻结模型的执行经验沉淀和无需真实试错的想象轨迹学习，可组合为“真实反馈校验、世界模型扩增”的具身进化闭环。
- **AgentEvolve**：[SenseNova-RoboRSI](#sensenova-roborsi)的验证经验回写与[CarryOn](#carryon)的可复用任务对象表明，部署时进化应把成功执行压缩为可检索、可迁移的工作流单元，而非持续堆积原始历史。
- **MemoryEvolve**：[MemT 1.0](#memt-1-0-300b-rsi)和[CarryOn](#carryon)提供了参数化原生记忆与对象化外部记忆两条互补路线，适合研究二者在写入成本、长期复用和错误累积上的协同边界。
- **Awesome-RSI**：[SenseNova-RoboRSI](#sensenova-roborsi)与[MemT 1.0](#memt-1-0-300b-rsi)分别补充了执行闭环和记忆底座案例，可用于梳理“不改核心参数”与“训练记忆分支”两类 RSI 定义及其稳定性差异。
- **JevEvolve**：[HiRoute](#hiroute-jev)给出了以任务复杂度和阶段胜任度驱动快慢模型切换的直接原型，后续可利用真实执行日志持续校准升级阈值与成本—质量边界。
- **Groom**：[BizAgentBench](#bizagentbench)的确定性过程检查和[LiveMACE](#livemace)的完整决策轨迹，可直接扩展 token 在规划、工具调用、违规步骤和无效试错间的证据化归因。
- **EvalEvolve**：[LiveMACE](#livemace)说明动态真实环境能显著削弱静态结果指标的误导性，而[BizAgentBench](#bizagentbench)进一步提供了将过程合规与调用成本纳入演化评测的方法。
- **ResearchEvolve**：[Into the Unknown](#into-the-unknown)中所有前沿智能体均未满足完整要求，提示自主科研闭环应优先加入逐声明证据绑定、需求覆盖检查和可复现性验证。
- **EnvironmentEvolve**：[OpenMobile-2](#openmobile-2)展示了可控应用、原生工具与规模化轨迹的一体化环境设计，可作为构建“可执行、可验证、可扩展”长程 Agent 经验工厂的参考。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-20/  

