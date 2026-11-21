# 2026-11-21 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **评测可信**
  - [量表反转探针：审计评判方向偏差](#item-21)：用语义不变、数字方向相反的量表，揭示大模型评分常依赖数字先验而非真正理解规则。
  - [预算配对反事实审计](#item-24)：让视觉智能体基于同一证据继续作答，分离看错区域、观察不足与最终回答错误。
  - [Gemini 4 Hydrogen](#gemini-4-hydrogen-token)：将推理词元减少约52%，同时在两代ARC-AGI高难基准上保持或提高成绩。

- **经验与推理**
  - [StarTV-Agent](#startv-agent)：把成功轨迹沉淀为可复用工作流，遇到新情况再回退到慢推理，最高节省52.1%词元。
  - [Forward-Only Passes](#forward-only-passes)：用前向激活的几何集中程度筛选低秩权重，无需反向传播即可低成本适应在线任务。
  - [PAIR-MED](#pair-med)：交替更新推理策略与步骤评分器，避免固定评分器跟不上新推理轨迹。
  - [Space-X](#space-x)：让执行智能体与控制智能体共同检查并修补跨工具证据链，减少空间推理中的语义断裂。

- **可信执行**
  - [Tether](#tether)：在隔离沙箱中观察真实系统调用，并按跨步骤状态策略拦截攻击，良性误报低于5%。
  - [授权边界智能体：可审计实验执行](#item-26)：把仪器权限、结果验证与人工接管写成可审计边界，使实验智能体能安全执行物理操作。
  - [Claude](#claude-lean)：用theta提升绕开整数不可求导问题并生成黎曼猜想的Lean证明，但仍缺完整编译与独立数学核验。

- **科研环境**
  - [SiliconGym](#silicongym-eda)：提供跨EDA任务且保留工具状态的并行环境，使硬件智能体能够开展大规模强化学习。
  - [SailSearch](#sailsearch)：由人类引导两个智能体共同发明算法和可认证难例，首次纯CPU解出18个长期未解实例。

- **开放模型**
  - [Hy4](#hy4)：开放支持百万词元上下文的混合专家模型全系权重与商用许可，降低长文档模型私有部署门槛。

- **热点延伸**：[AGI之后是什么](#agi-asi)、[MC-Lens](#mc-lens)、[PMD](#pmd)、[EgoCaptioner](#egocaptioner)、[VODA](#voda)

## 对当前研究的启发
- **EvalEvolve**
  - 迁移｜从 [量表反转探针：审计评判方向偏差](#item-21) 把量表反转用于评判器审计：比较正反量表排名一致率与底线归一化分数
  - 迁移｜从 [预算配对反事实审计](#item-24) 把同证据续答用于过程评测：固定观察历史，分别增加观察预算与回答预算并归因误差

- **AgentEvolve**
  - 迁移｜从 [StarTV-Agent](#startv-agent) 把成功轨迹编译成参数化工作流：相似任务直接复用，低置信或执行失败时回退到ReAct

- **ReasoningEvolve**
  - 延续｜[Forward-Only Passes](#forward-only-passes) 尚未验证深层大模型扩展性：按层数和参数量测试适应增益、时延及显存
  - 迁移｜从 [PAIR-MED](#pair-med) 把策略与过程奖励交替更新用于推理训练：对比固定奖励器，评估准确率和奖励校准误差

- **MonitorEvolve**
  - 迁移｜从 [Tether](#tether) 把跨动作安全状态用于Agent运行时：沙箱预执行工具调用，按泄露率、拦截率和误报率评测
  - 迁移｜从 [授权边界智能体：可审计实验执行](#item-26) 把权限—验证—接管边界用于科研Agent：为每类仪器动作配置授权和回滚条件

- **AgentTrainEvolve**
  - 迁移｜从 [SiliconGym](#silicongym-eda) 把可保留工具状态的并行环境用于长程RL：对比重置环境，测成功率和训练吞吐

- **ResearchEvolve**
  - 迁移｜从 [SailSearch](#sailsearch) 把“算法与可认证难例共同生成”用于科研闭环：以最优性证书和未解实例数验收

- **LogicEvolve**
  - 延续｜[Claude](#claude-lean) 的证明尚未独立核验：复现Lean编译、审计依赖与题面一致性，并由专家抽查关键引理

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-21/  

