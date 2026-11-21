# 2026-11-21 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **推理与评测**
  - [Gemini 4 Hydrogen](#gemini-4-hydrogen-token)：把推理词元减少约52%，仍在两代ARC-AGI基准保持或提高成绩，证明高难推理可同时降本提效。
  - [Forward-Only Passes](#forward-only-passes)：只看前向激活方向的集中程度筛选低秩权重，无需反向传播即可低成本适应在线任务。
  - [PAIR-MED](#pair-med)：让推理模型与步骤评分器交替更新，避免固定评分器跟不上推理轨迹变化，提升12种语言的医疗推理。
  - [量表反转探针：审计评判方向偏差](#item-21)：反转评分数字方向后检查结论是否稳定，发现评判模型常依赖数字大小而非真正理解评分规则。
  - [预算配对反事实审计](#item-24)：在相同证据和预算下续接或停止观察，分离视觉智能体的取证错误与最终作答错误。
- **智能体系统**
  - [Tether](#tether)：在隔离沙箱中观察真实系统调用，并跨多步保留安全状态，拦截长链攻击且良性误报低于5%。
  - [StarTV-Agent](#startv-agent)：把成功轨迹沉淀为可复用工作流，遇到新任务再回退到慢推理，最高节省52.1%词元。
  - [SiliconGym](#silicongym-eda)：用可保留工具状态的统一环境并行训练硬件智能体，覆盖代码生成、验证、优化与仓库修复。
  - [Space-X](#space-x)：让执行智能体产出空间证据、控制智能体检查并修补断链，减少跨工具语义冲突和证据误判。
- **科研与验证**
  - [Claude](#claude-lean)：用theta提升绕过整数不可求导问题，生成黎曼猜想的Lean形式化证明，但完整编译与数学结论仍待独立核验。
  - [SailSearch](#sailsearch)：由人类引导两名智能体共同搜索算法并构造可认证难例，首次仅用CPU解出18个长期未解实例。
  - [FormalFixer](#formalfixer-rtl)：联合核对规格、验证断言和硬件代码的真实意图，避免把断言错误误修成实现改动。
- **开放模型**
  - [Hy4](#hy4)：开放支持百万词元上下文的混合专家模型全系权重与商用许可，降低长文档和多模态系统的私有部署门槛。
- **热点延伸**：[AGI之后是什么](#agi-asi)、[MC-Lens](#mc-lens)、[PMD](#pmd)、[EgoCaptioner](#egocaptioner)、[VODA](#voda)

## 对当前研究的启发
- **ReasoningEvolve**
  - 迁移｜从 [Forward-Only Passes](#forward-only-passes) 把激活角度集中度用到在线适应：仅跑前向搜索低秩分量，测时延、准确率与遗忘。
- **EvolveLRM**
  - 迁移｜从 [PAIR-MED](#pair-med) 把策略与过程奖励交替更新用于推理训练：对比冻结奖励模型，测准确率、校准误差和奖励作弊率。
- **AgentEvolve**
  - 迁移｜从 [StarTV-Agent](#startv-agent) 把成功轨迹参数化为工作流：相似任务直接复用，低置信度时回退ReAct，统计成功率与词元。
- **AgentTrainEvolve**
  - 迁移｜从 [SiliconGym](#silicongym-eda) 把持久工具状态用于多轮Agent RL：对比重置环境，测训练吞吐、任务成功率和跨工具迁移。
- **EvalEvolve**
  - 迁移｜从 [量表反转探针：审计评判方向偏差](#item-21) 把量表反转加入评测：双向评分后归一化，统计排名翻转率与一致性。
- **Groom**
  - 迁移｜从 [预算配对反事实审计](#item-24) 把同轨迹续接实验用于token归因：固定证据比较继续观察与直接作答，测边际收益。
- **MonitorEvolve**
  - 迁移｜从 [Tether](#tether) 把有状态副作用策略用于Agent运行时：沙箱预执行跨步调用，测攻击拦截率、误报率和额外时延。
- **ResearchEvolve**
  - 迁移｜从 [SailSearch](#sailsearch) 把算法搜索与可认证难例生成并行化：对比单智能体，测最优值、认证率与CPU时间。
- **CodeEvolve**
  - 迁移｜从 [FormalFixer](#formalfixer-rtl) 把规格—断言—代码联合归因用于修复：对比只改代码，测误修率、验证通过率和补丁规模。
- **LogicEvolve**
  - 延续｜[Claude](#claude-lean) 留下证明尚未独立核验：复现Lean编译并审计公理、依赖与题面，报告通过率和未验证缺口。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-21/  

