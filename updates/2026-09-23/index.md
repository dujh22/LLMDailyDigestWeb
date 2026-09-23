# 2026-09-23 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从概念框架走向工程闭环（3 条）：[基元律动](#agent)将多模型调度、运行经验、评测与后训练串成反馈飞轮，[MiMo-V2.6](#mimo-v2-6-rl-rsi)以约 75 万条智能体轨迹开展大规模 RL，[9月四篇RSI论文](#9-rsi)则归纳自主性阶梯与数据—模型—脚手架联合演化。
- 模型竞争进一步转向长程 Agent 的单位任务效益：[Grok 4.7](#grok-4-7-coding-agent)强化编程智能体、50 万 Token 上下文和复杂任务执行，[GPT-6 Sol、Luna 与 Claude Opus 5.5](#gpt-6-sol-luna-claude-opus-5-5)则把焦点从峰值能力推向推理效率与规模化成本。
- 智能体训练呈现“在策略数据—专长路由—工具闭环”路线：[onPanda](#onpanda)以首错令牌纠正低成本构造在策略对齐数据，[类别感知迭代专家训练](#item-11)通过类别 RL 与多教师蒸馏改善软件工程任务的不均衡进展，[VideoGen-Agent](#videogen-agent)展示了可随工具升级持续受益的生成智能体。
- 具身与世界模型共同强化空间表征和长程一致性（3 条）：[RoboDawn](#robodawn)以离散接口和上下文学习迁移 VLM 智能，[Grounded Action Model](#grounded-action-model-3d)用对象中心的视觉—几何表示提升机器人泛化，[WorldCrafter](#worldcrafter)以可查询的隐式三维记忆维持多视角世界一致性。
- 数据与评测工程继续向低成本、可审计流程演进：[D-RAC](#d-rac)把异构企业文档规范化为检索优化分块，[OmniEdu](#omniedu-k-12)通过均衡教育数据提升多项 K-12 能力，[Deep Persona](#deep-persona)则以无参考评估和对抗压力测试检验长期人格一致性。

## 对当前研究的启发
- **Awesome-RSI**：[基元律动](#agent)、[MiMo-V2.6](#mimo-v2-6-rl-rsi)与[9月四篇RSI论文](#9-rsi)共同给出了从自主性分级到大规模轨迹 RL、再到模型—数据—脚手架联合演化的 RSI 路线图，可据此扩展资源分类与闭环稳定性观察维度。
- **HarnessEvolve**：[基元律动](#agent)表明 Harness 不应只作为固定执行外壳，而可把调度策略、运行轨迹和评测反馈一并纳入持续优化对象。
- **EvolveLLM**：[onPanda](#onpanda)的首错令牌定位、纠正与续写机制能在保留模型采样分布的同时降低对齐数据成本，可用于构建更稳定的迭代自纠正训练飞轮。
- **DataEvolve**：[onPanda](#onpanda)提供了比整段重写更细粒度的在策略数据进化单元，可围绕错误位置、修正价值和后续轨迹质量开展主动筛选与数据价值评估。
- **Groom**：[Grok 4.7](#grok-4-7-coding-agent)及新一轮“单位任务成本”竞争凸显仅比较 Token 总量已不足，需进一步归因长程任务中规划、工具反馈、恢复与有效交付各阶段的 Token 利用率。
- **MemoryEvolve**：[WorldCrafter](#worldcrafter)的视角可查询隐式三维记忆展示了“按任务查询而非完整回放”的空间记忆机制，可借鉴到长程智能体的结构化记忆检索与一致性评测中。
- **ResearchEvolve**：[Game-the-LLM-Reviewer](#game-the-llm-reviewer-ai-skill)把证据核对与语义等价检查嵌入论文改写流程，为自主科研系统降低迎合 AI 审稿偏差和夸大结论提供了可审计护栏。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-23/  

