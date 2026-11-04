# 2026-11-04 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进走向开放世界与群体演化**：3 项代表工作分别从自动合成可验证任务、规模化经验飞轮和群体经验共享推进持续进化，包括 [CUA-Master：开放世界双循环递归改进计算机使用智能体](#cua-master)、[NorthCUA：以规模化经验加速计算机操作智能体](#northcua) 与 [Group-Evolving Agents：经验共享驱动的开放式群体自进化](#group-evolving-agents)。
- **Agent 训练的数据与轨迹闭环进一步工程化**：[HarnessSQL：面向真实数据库的长程交互 SQL Agent 训练框架](#harnesssql-sql-agent) 将执行沙盒、全轨迹 SFT 和强化学习打通，[SWE-Trail：历史引导的编码智能体轨迹收集](#swe-trail) 提升分支探索价值，[AutoSFT：多智能体自动配置 SFT 训练数据](#autosft-sft) 则把数据分析、修复、合成与配比纳入自动闭环。
- **Harness 与动态评测成为长程智能体的关键基础设施**：[uni-robot-agent：面向开源机器人智能体的统一 Harness](#uni-robot-agent-harness) 统一具身智能体的跨环境执行与后训练接口，[ReTrace：以目标导向动作重放评测计算机操作智能体恢复能力](#retrace) 和 [Storage Agent Family：可追溯的持续评测与改进实践](#storage-agent-family) 分别补足错误恢复评测与线上持续回归体系。
- **RSI 的关注点从能力增长转向验证边界**：[RSI 系统优化 Agent 的 Reward Hacking 与验证边界](#rsi-agent-reward-hacking) 指出搜索预算增加会放大目标偏差，[Awesome RSI：AI 自我进化研究目录与基准全景](#awesome-rsi-ai) 则提供覆盖方法、基准与系统的全景索引。
- **模型发布与热点延伸**：美团发布面向长程任务、结合原生多模态与真实代码环境强化学习的 [美团发布原生多模态模型 LongCat-2.5](#longcat-2-5)；低相关热点集中在实时流式视频生成、主动视频观察和可解释摄影构图应用。

## 对当前研究的启发
- **AgentEvolve**：[Group-Evolving Agents：经验共享驱动的开放式群体自进化](#group-evolving-agents) 表明可将单体反思与技能积累扩展为跨智能体共享的轨迹、工具和 Harness 改进经验。
- **AgentTrainEvolve**：[HarnessSQL：面向真实数据库的长程交互 SQL Agent 训练框架](#harnesssql-sql-agent) 与 [NorthCUA：以规模化经验加速计算机操作智能体](#northcua) 提供了“真实可执行环境—全轨迹监督—执行奖励 RL—经验回流”的可复用训练闭环。
- **DataEvolve**：[AutoSFT：多智能体自动配置 SFT 训练数据](#autosft-sft) 可用于验证由多角色 Agent 自动诊断数据缺口、生成修复样本并优化配比是否优于单一数据搜索器。
- **HarnessEvolve**：[uni-robot-agent：面向开源机器人智能体的统一 Harness](#uni-robot-agent-harness) 说明统一环境适配层不仅能提高评测可比性，还可直接承载后训练和持续学习。
- **EvalEvolve**：[ReTrace：以目标导向动作重放评测计算机操作智能体恢复能力](#retrace) 提供了以受控错误注入和结果等价状态衡量恢复能力的动态评测范式。
- **Awesome-RSI**：[RSI 系统优化 Agent 的 Reward Hacking 与验证边界](#rsi-agent-reward-hacking) 给出一条关键治理原则，即验证强度和独立性必须随自改进系统的搜索预算同步扩张。
- **RobotEvolve**：[uni-robot-agent：面向开源机器人智能体的统一 Harness](#uni-robot-agent-harness) 可作为连接仿真、真机、开放权重模型与持续后训练的工程底座，降低跨本体自进化实验成本。
- **CodeEvolve**：[SWE-Trail：历史引导的编码智能体轨迹收集](#swe-trail) 展示了利用历史轨迹选择高价值检查点、同时不向当前策略泄露建议的训练数据扩增机制。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-04/  

