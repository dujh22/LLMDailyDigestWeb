# 2026-11-06 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从概念走向可验证闭环：[Recursa](#recursa)尝试在无更强教师条件下持续适应新领域，[自递归软硬件脚手架驱动自主光学实验](#item-64)则把硬件、软件、模型与实验协议共同纳入物理反馈闭环。
- 智能体的记忆、脚手架与训练进一步融合：[千问 Personal Agent](#personal-agent)展示模型—长期记忆—Harness 协同架构，[StateGraph](#stategraph)用依赖图和反事实验证维护动态记忆，[TriGRPO](#trigrpo)则以树上后见信用分配利用稀缺成功轨迹。
- 自进化与后训练的“真实能力增长”受到更严格检验：[SelfImprove-Bench](#selfimprove-bench)建立跨场景泛化阶梯，[在策略蒸馏用于强化学习后能力巩固的泛化局限](#item-14)揭示分布外遗忘，而[RLVR只优化解题路径选择，未提升内在推理能力](#rlvr-4)进一步质疑 RLVR 是否真正扩展推理表征。
- 评测可靠性成为主线：[长程智能体失败归因需执行反事实](#item-46)要求用状态干预与回放证书验证归因，[静默评测工具错误导致智能体排行榜重排](#item-67)暴露工具链误差；科研侧的[验证器更强不等于发现质量更高](#item-66)表明优化提议池可能比继续增强评判器更重要。
- 推理基础设施与真实环境数据同步演进：[SpecPilot](#specpilot)用智能体自主发现部署相关的投机解码优化，[递归稀疏注意力](#item-22)以对数选择成本外推至百万词元，[PyRUA-DataFarm](#pyrua-datafarm-llm)则将 LLM 远程操作与仿真生成结合以规模化机器人数据。
- 新模型与热点延伸覆盖网络安全、开放权重、多模态生成、游戏世界模型及三维视觉，其中[OpenAI 发布 GPT-6 Cyber 网络安全模型](#openai-gpt-6-cyber)是较重要的垂直模型发布；低相关性热点主要集中于 GameVerse 长时程游戏数据、Solv3R 三维视觉和光学数据中心控制。

## 对当前研究的启发
- **Awesome-RSI**：[Recursa](#recursa)与[SelfImprove-Bench](#selfimprove-bench)可分别作为无强教师递归改进架构和跨分布能力增益评测框架，帮助区分持续适应与基准内自我强化。
- **ResearchEvolve**：[验证器更强不等于发现质量更高](#item-66)说明科研智能体应优先扩展并改善候选提议池，而不是默认把资源继续投入更强评判器。
- **AgentTrainEvolve**：[TriGRPO](#trigrpo)可将长程任务中的稀缺成功轨迹通过回滚树和后见信用分配转化为更密集的探索与训练信号。
- **MemoryEvolve**：[StateGraph](#stategraph)提供了依赖感知、可反事实验证的记忆失效机制，可用于避免上游事实变化后旧信念和行动继续污染长期状态。
- **HarnessEvolve**：[长程智能体失败归因需执行反事实](#item-46)提示评测 Harness 应保存可恢复状态并生成回放证书，避免仅凭事后轨迹文本归因。
- **EvalEvolve**：[静默评测工具错误导致智能体排行榜重排](#item-67)表明排行榜发布前需要对漏评分、成本核算、动作来源和评估器版本实施自动一致性审计。
- **GeneralizeEvolve**：[在策略蒸馏用于强化学习后能力巩固的泛化局限](#item-14)与[RLVR只优化解题路径选择，未提升内在推理能力](#rlvr-4)共同提示能力巩固评测必须加入 OOD 行为和内部表征变化，而不能只看分布内准确率。
- **CacheEvolve**：[递归稀疏注意力](#item-22)的树状 KV 缓存与分层候选选择，为固定预算下实现百万词元检索提供了可直接比较的新结构基线。
- **InfraEvolve**：[SpecPilot](#specpilot)证明成本模型、并行搜索、逐词元正确性验证与结构化经验记忆可以组成面向具体硬件的自主推理优化闭环。
- **RobotEvolve**：[PyRUA-DataFarm](#pyrua-datafarm-llm)展示了从一次真实标定自动生成仿真任务和精确动作数据的低成本数据飞轮，可用于扩展可部署机器人策略训练。
- **JevEvolve**：[StartLux-Decision](#startlux-decision)将概率校准直接用于决定何时升级到额外思考，可作为“快决策—慢推理”路由器的训练与评测方案。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-06/  

