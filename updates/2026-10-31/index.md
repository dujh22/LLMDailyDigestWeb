# 2026-10-31 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进形成两条新路径：[RISE](#rise-rlvr) 以 RLVR 未来轨迹和在策略蒸馏构造动态教师，[A-RSI](#a-rsi) 则通过奖励波动驱动任务刷新，实现零外部数据的多模态自训练。
- 动态评测与自动出题进一步走向“可验证、可调难度”：‌[Few Shots](#few-shots-agent) 引入程序验证器与双 Agent 校验，[基准测试是难度分布的经验度量](#item-13) 用 BenchFill 补齐难度覆盖，[Co-Design Bench](#co-design-bench) 则将真实多模态编码协作纳入评测。
- Agent 自进化开始落到复杂可执行产物：[VibeGame](#vibegame-ai) 以专业化对抗 Agent 团队和免训练演化机制，从提示词端到端生成可玩 2D 游戏。
- 多模态模型兼顾统一能力、表征机制与效率：[Youtu-Parsing-Omni](#youtu-parsing-omni) 统一解析四类模态，[JEPA](#jepa) 为跨模态共同表征提供理论刻画，[LOWN](#lown) 将扩散视觉语言模型的平均解码 FLOPs 降至 35.3%。
- 热点延伸集中在生成架构：[L3G-World](#l3g-world-3d) 探索带 3D 高斯长期记忆的实时无限世界，[SpecSlot](#specslot-transformer) 则改进像素空间生成式 Transformer 的计算效率。

## 对当前研究的启发
- **Awesome-RSI**：[RISE](#rise-rlvr) 的“未来自身作为教师”与 [A-RSI](#a-rsi) 的自适应任务刷新，提供了两种无需固定外部教师的 RSI 闭环设计。
- **EvolveLLM**：[RISE](#rise-rlvr) 表明可直接蒸馏模型自身外推后的 RLVR 更新轨迹，从而减少自改进所需的额外教师与采样成本。
- **DataEvolve**：[A-RSI](#a-rsi) 可将奖励波动和准确率转化为合成数据刷新信号，使数据分布持续对准当前能力边界。
- **EvalEvolve**：[Few Shots](#few-shots-agent) 的可复现答案与双 Agent 校验可增强自动出题可信度，而 [BenchFill](#item-13) 提供了按难度分布缺口定向补题的方法。
- **ResearchEvolve**：[Few Shots](#few-shots-agent) 将科学问题提交、程序验证和纪录刷新组合成开放平台，可作为自主科研 Agent 生成与验证挑战的基础设施。
- **AgentEvolve**：[VibeGame](#vibegame-ai) 展示了冻结参数后通过角色化对抗、试玩反馈和经验复用持续改进复杂产物的可落地路径。
- **TaskEvolve**：[VibeGame](#vibegame-ai) 的可读写游戏引擎使“生成—运行—诊断—修复”闭环具备结构化状态与自动验收条件。
- **HarnessEvolve**：[Co-Design Bench](#co-design-bench) 的真实仓库编辑任务和“判定后反驳”协议，可用于增强编码 Agent harness 的无参考、抗误判评测。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-31/  

