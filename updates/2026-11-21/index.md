# 2026-11-21 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **推理适应**
  - [Forward-Only Passes](#forward-only-passes)：按前向激活方向的一致程度筛选低秩权重，无需反向传播即可低成本适应在线任务。
  - [Gemini 4 Hydrogen](#gemini-4-hydrogen-token)：以减少约52%的推理词元保持或提高ARC-AGI成绩，把高难推理优化重点转向单位成本能力。
  - [PAIR-MED](#pair-med)：让推理策略与过程奖励模型交替更新，避免固定裁判因推理轨迹变化而失准。

- **智能体进化**
  - [StarTV-Agent](#startv-agent)：复用成功工作流处理熟悉任务、遇到异常再启用慢推理，最高节省52.1%词元。
  - [SiliconGym](#silicongym-eda)：以可保留工具状态的跨EDA工具链环境，支持硬件智能体并行强化学习与真实执行验证。
  - [Space-X](#space-x)：由执行与控制智能体协同修补跨工具证据链，纠正空间推理中的语义断裂和证据不足。

- **可信评测**
  - [Tether](#tether)：在隔离沙箱中观察真实系统调用并跨动作验证安全状态，可拦截多步攻击且良性误报低于5%。
  - [量表反转探针](#item-21)：通过颠倒评分数字方向检验评判模型是否理解规则，揭示其普遍依赖数字大小先验。
  - [预算配对反事实审计](#item-24)：让视觉智能体在相同证据历史上分别继续观察或直接回答，拆分观察规划与作答失误。

- **科研验证**
  - [Claude](#claude-lean)：据称以theta提升绕过整数不可求导问题，生成黎曼猜想的Lean证明，但仍须编译、依赖和数学审查。
  - [SailSearch](#sailsearch)：由人类引导两个智能体共同设计算法和可认证难例，首次用纯CPU解出18个长期未解实例。
  - [FormalFixer](#formalfixer-rtl)：联合核对规格、断言与RTL意图，避免把断言错误或规格歧义误修成硬件实现缺陷。

- **模型发布**
  - [Hy4](#hy4)：开放支持百万词元上下文的混合专家模型全系权重与商用许可，降低长文档模型私有部署门槛。

- **具身闭环**
  - [TuringSpace](#turingspace)：用可程序生成的点击拖拽验证码训练空间行动闭环，使任务成功率从1.6%升至33.1%。
  - [Mind2Act World](#mind2act-world)：分别测试心智推理、动作执行及其闭环组合，定位机器人失败究竟来自哪一环。

- **热点延伸**：[AGI之后是什么](#agi-asi)、[MC-Lens](#mc-lens)、[PMD](#pmd)、[EgoCaptioner](#egocaptioner)、[VODA](#voda)

## 对当前研究的启发
- **ReasoningEvolve**
  - 迁移｜从 [Forward-Only Passes](#forward-only-passes) 把激活方向一致度用于在线适应：对比LoRA的准确率、时延和显存。

- **EvalEvolve**
  - 迁移｜从 [量表反转探针](#item-21) 把量表反转加入评判审计：双向评分同批答案，统计排序翻转率。
  - 迁移｜从 [预算配对反事实审计](#item-24) 把同证据分支用于过程归因：分别续看与作答，测规划和答案损失。

- **AgentEvolve**
  - 迁移｜从 [StarTV-Agent](#startv-agent) 把成功轨迹参数化为工作流：相似任务优先复用，失败时回退慢推理。
  - 迁移｜从 [Space-X](#space-x) 把证据链修补用于工具经验进化：记录语义断点并生成新检查步骤。

- **AgentTrainEvolve**
  - 迁移｜从 [SiliconGym](#silicongym-eda) 把持久工具状态用于多轮RL：跨回合保留工程状态并做跨工具配对评测。

- **EvolveLRM**
  - 迁移｜从 [PAIR-MED](#pair-med) 把策略与过程奖励交替更新用于RL：对比固定裁判的准确率和奖励漂移。

- **MonitorEvolve**
  - 迁移｜从 [Tether](#tether) 把跨动作安全状态用于常驻Agent：沙箱预执行工具调用并追踪信息流与权限变化。

- **ResearchEvolve**
  - 迁移｜从 [SailSearch](#sailsearch) 把“算法与可认证难例共创”用于科研闭环：以最优性证明和新解数量验收。

- **RobotEvolve**
  - 延续｜[Mind2Act World](#mind2act-world) 留下单项能力难迁移到闭环：对比分训、联训和反馈课程的成功率与恢复率。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-21/  

