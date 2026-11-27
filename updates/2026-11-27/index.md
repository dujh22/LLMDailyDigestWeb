# 2026-11-27 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **环境演化**
  - [RepoFactory](#repofactory)：用代码规模与结构指标替代昂贵的智能体试跑，低成本迭代长程编程训练环境。
- **任务演化**
  - [Play2Evolve](#play2evolve)：让智能体按趣味维度反复试玩、诊断和修改游戏，补足“能运行但不好玩”的质量反馈。
  - [VibeVideoAgent](#vibevideoagent)：用短片段预览和多时间轴证据，在完整渲染前发现代码检查捕捉不到的画面与音画同步缺陷。
- **具身智能**
  - [PyRUA-Dex](#pyrua-dex)：让编程智能体探索、组合并精炼双手操作程序，在缺少高质量动作示范时生成机器人策略。
- **高效架构**
  - [MoLT](#molt-kv)：把注意力缓存变成跨层、跨循环可选择读取的记忆，减少循环模型的重复计算并提升最高1.7倍词元效率。
- **评测基建**
  - [EgoUseBench](#egousebench)：用持续变化的第一人称观察替代固定指令，揭示操作智能体在动态任务中的成功率下降26.3%。
  - [Real2SimLab](#real2simlab)：以统一程序接口连接不同仿真方法和原生评分器，免去每套方法逐个适配基准。
- **文档推理**
  - [DocSEAM](#docseam)：在视觉编码阶段双向融合相邻页面，修复分页造成的信息断裂并增强跨页问答。
- **热点延伸**：[I2VT](#i2vt)、[HOG-WAM](#hog-wam)、[PixelMatte](#pixelmatte)

## 对当前研究的启发
- **EnvironmentEvolve**
  - 迁移｜从 [RepoFactory](#repofactory) 把合理性、实现范围和结构耦合度用于环境筛选：按指标排序后抽样跑 Agent 验证相关性。
  - 延续｜[RepoFactory](#repofactory) 主要覆盖 Python 且首批环境未经进化：扩展到前端与 Java，对比进化前后成功率和迁移收益。
- **TaskEvolve**
  - 迁移｜从 [Play2Evolve](#play2evolve) 把趣味性拆成可诊断反馈用于作品迭代：每轮试玩逐项评分，仅修改最低分维度。
  - 迁移｜从 [VibeVideoAgent](#vibevideoagent) 把局部预览用于长程作品验收：分段检查画面、声音与时间轴，再决定是否完整渲染。
- **RobotEvolve**
  - 迁移｜从 [PyRUA-Dex](#pyrua-dex) 把动作技能表示为可组合程序：多智能体探索技能后蒸馏入库，再随机化参数验证迁移。
- **CacheEvolve**
  - 迁移｜从 [MoLT](#molt-kv) 把 KV 视为可选择读取的循环记忆：训练门控器决定复用层级，评测困惑度、延迟与显存。
- **EvalEvolve**
  - 延续｜[EgoUseBench](#egousebench) 暴露动态场景26.3%的成功率缺口：对比固定与增量观察，测重规划率、恢复时延和最终成功率。
- **HarnessEvolve**
  - 迁移｜从 [Real2SimLab](#real2simlab) 把可执行程序作为统一评测契约：封装 Agent 接口并保留各基准原生评分器。
- **ReasoningEvolve**
  - 迁移｜从 [DocSEAM](#docseam) 把相邻页双向融合用于长文档推理：对比逐页编码，测跨页证据召回率和答案准确率。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-27/  

