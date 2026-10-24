# 2026-10-24 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- Agent 系统自进化成为今日主线：[HarnessPro](#harnesspro-agent-53)以无标签合成测试和帕累托优化协同演化多智能体脚手架，最高降低 53% 单任务成本；[从 Harness 到 Loop](#harness-loop-agent)则将生产级演进扩展为发现、归因、修复、验证和发布的持续闭环。
- 数据与训练自动化继续向“模型自主改进模型”推进：[AutoSFT](#autosft)让多智能体自主诊断能力短板、优化 SFT 数据并闭环评测，[EvolveLRM](#evolvelrm-k3v4)则探索个人可承担的低成本大模型训练路径。
- 真实环境评测与记忆机制均出现值得关注的结果：[OpenDS-World](#opends-world-web)显示前沿模型在开放 Web 深度搜索上的最佳准确率仅 39.0%，[Deep Fusion Memory](#deep-fusion-memory)则以分块级参数化记忆探索无需在线检索的知识融合。
- 新模型工作集中于多模态、效率与具身世界模型：[WeVisOne-VL](#wevisone-vl)统一物体级和像素级视觉任务，[Meta Expert](#meta-expert-moe)通过跨层专家共享压缩 MoE，[LaLa-World](#lala-world)与 [FRED](#fred)分别探索语言动作统一和未来视频表征自蒸馏。
- 应用侧竞争正转向用户关系、权限与治理：[Personal AI 入口争夺](#personal-ai-app)强调长期记忆及超级 App 权限壁垒，[DeepSeek 智能体涌入 B 站评论区](#deepseek-b)暴露自动互动的身份与社区治理问题；热点延伸还包括 [Skills 生态变化](#skills)、预算感知扩散特征适配和可复用 RGBA 图层编辑。

## 对当前研究的启发
- **HarnessEvolve**：[HarnessPro](#harnesspro-agent-53)表明可用合成测试和成本—通过率帕累托前沿自动筛选 Harness，而 [从 Harness 到 Loop](#harness-loop-agent)提示评测框架还应覆盖上线后的归因、修复与回归验证。
- **SystemEvolve**：[HarnessPro](#harnesspro-agent-53)提供了无需人工标签即可联合进化多智能体编排与脚手架的可复用系统优化范式。
- **SwarmEvolve**：[HarnessPro](#harnesspro-agent-53)说明多智能体协作结构可以通过合成反馈持续优化，并同时把群体能力和运行成本纳入选择目标。
- **DataEvolve**：[AutoSFT](#autosft)可作为“短板诊断—数据生成与改写—训练—评测”数据飞轮的具体实现参考，重点应补充多轮迭代中的偏差累积监测。
- **AgentTrainEvolve**：[AutoSFT](#autosft)展示了由多个 Agent 自主构造训练数据和课程的训练侧闭环，可进一步接入环境交互轨迹与可验证奖励。
- **EvalEvolve**：[OpenDS-World](#opends-world-web)以持续变化的真实 Web 和跨来源证据整合拉开模型差距，为动态、抗污染的长程 Agent 评测提供了任务模板。
- **Groom**：[HarnessPro](#harnesspro-agent-53)的成本—成功率联合优化可扩展为过程级 token 归因，以判断成本下降究竟来自更有效的规划、工具调用还是错误恢复。
- **MemoryEvolve**：[Deep Fusion Memory](#deep-fusion-memory)提示可将长期知识按块预测并门控注入隐藏状态，作为检索式记忆之外的参数化巩固路线。
- **RobotEvolve**：[LaLa-World](#lala-world)与 [FRED](#fred)分别提供跨数据源统一动作语义和自蒸馏未来表征的方法，可用于降低世界模型训练成本并增强跨环境、跨本体迁移。
- **PersonalEvolve**：[Personal AI 入口争夺](#personal-ai-app)表明个性化能力的落地瓶颈不只在画像与长期记忆，还在服务连接、操作授权及用户数据闭环的可获得性。
- **EvolveLRM**：[单人训练大模型，EvolveLRM 指标挑战 K3V4](#evolvelrm-k3v4)提示项目评测应同时报告能力提升、训练预算与人力投入，以识别真正可复现的低成本自进化路径。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-24/  

