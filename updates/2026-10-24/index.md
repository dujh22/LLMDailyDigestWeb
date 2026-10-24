# 2026-10-24 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **Agent 脚手架从静态编排走向成本—能力协同进化**：[HarnessPro：无标签多智能体进化将 Agent 成本降低 53%](#harnesspro-agent-53)以合成测试和帕累托优化自动改进多智能体系统，[从 Harness 到 Loop：Agent 的可靠交付与持续进化](#harness-loop-agent)则将生产闭环扩展至问题发现、归因、修复、验证与发布。
- **训练数据开始成为可由 Agent 自主优化的对象**：[清华 AutoSFT：多智能体自主优化训练数据](#autosft)串联短板诊断、数据优化和闭环评测，而[单人训练大模型，EvolveLRM 指标挑战 K3V4](#evolvelrm-k3v4)进一步突出低资源训练与成本优化路线。
- **真实环境评测与深层记忆揭示 Agent 的能力瓶颈**：[OpenDS-World：真实 Web 环境中的深度搜索评测](#opends-world-web)显示最佳前沿模型在开放 Web 长程搜索中准确率仅为 39.0%，[Deep Fusion Memory：分块级参数化记忆](#deep-fusion-memory)则探索冻结主干、无需在线检索的知识融合方式。
- **多模态与具身模型集中推进统一表征和跨域迁移**：[WeVisOne-VL：统一物体级与像素级视觉感知](#wevisone-vl)统一多类视觉任务，[LaLa-World：以自然语言动作扩展潜在世界模型](#lala-world)打通异构动作数据，[FRED：面向世界动作模型的自蒸馏未来视频表征](#fred)提升长程操控和人到机器人迁移。
- **个人智能体竞争延伸至入口、权限与社区治理**：[Personal AI 入口争夺：巨头押注与超级 App 权限壁垒](#personal-ai-app)表明竞争焦点正转向长期记忆、服务连接和操作权限；当日热点延伸还关注 Skills 生态变化及预算受限的视觉适配，但与核心研究方向关联较弱。

## 对当前研究的启发
- **HarnessEvolve**：[HarnessPro](#harnesspro-agent-53)表明可用合成测试和帕累托搜索联合优化通过率与调用成本，并由持续反馈 Loop 将一次性 harness 优化升级为生产期演进。
- **SystemEvolve**：[HarnessPro](#harnesspro-agent-53)提供了无需人工标签即可搜索多智能体结构的实例，可作为工作流、工具配置与成本约束联合自改进的实现参考。
- **DataEvolve**：[AutoSFT](#autosft)把能力短板分析、训练数据生成优化和效果评测闭合起来，可直接借鉴为数据价值驱动的自主策展飞轮。
- **AgentTrainEvolve**：[AutoSFT](#autosft)提示可让多智能体先定位 Agent 能力边界，再针对性构造 SFT 数据，为后续交互式强化学习提供自生成课程。
- **EvalEvolve**：[OpenDS-World](#opends-world-web)以持续变化的真实开放 Web、跨来源证据和浏览器交互构成高难评测，可用于研究比静态问答更抗饱和的动态 Agent 基准。
- **MemoryEvolve**：[Deep Fusion Memory](#deep-fusion-memory)展示了外部知识向隐藏状态深度融合的参数化记忆路线，可用于比较其与显式检索记忆在成本、更新性和遗忘方面的权衡。
- **RobotEvolve**：[LaLa-World](#lala-world)与[FRED](#fred)分别提供语言化动作统一和未来表征自蒸馏机制，可用于提高跨仿真、跨本体数据复用及 sim-to-real 泛化。
- **PersonalEvolve**：[Personal AI 入口争夺](#personal-ai-app)说明个性化能力必须与长期记忆、用户关系及可授权的应用操作权限共同设计，而不能只优化模型侧偏好学习。
- **Groom**：[HarnessPro](#harnesspro-agent-53)的质量—成本帕累托优化可进一步细化为过程级 token 归因，以判断 53% 成本下降来自有效压缩还是执行步骤缺失。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-24/  

