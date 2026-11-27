# 2026-11-27 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **环境演化**
  - [RepoFactory](#repofactory)：用代码规模与结构指标替代昂贵的智能体求解反馈，低成本筛选并演化长程编程训练环境。
- **任务演化**
  - [Play2Evolve](#play2evolve)：让智能体按趣味维度试玩、诊断和修改游戏，解决作品能运行却不好玩的问题。
  - [VibeVideoAgent](#vibevideoagent)：用局部预览和多时钟证据在完整渲染前发现代码执行无法暴露的画面与音画同步缺陷。
- **具身技能**
  - [PyRUA-Dex](#pyrua-dex)：让编程智能体探索、组合并精炼双手操作程序，在缺少高质量示范时自主生成控制策略。
- **高效架构**
  - [MoLT](#molt-kv)：选择性复用不同深度和循环中的KV记忆，减少循环模型的重复计算并实现最高1.7倍词元效率。
  - [DyLoMo-DiT](#dylomo-dit)：以共享循环权重和稀疏专家扩充生成能力，并按噪声阶段动态分配计算以降低存储成本。
- **多模态系统**
  - [DocSEAM](#docseam)：在视觉编码阶段双向融合相邻页面，消除分页造成的信息断裂并增强跨页问答。
  - [EgoUseBench](#egousebench)：用持续变化的第一人称观察检验操作智能体能否修正意图，揭示其成功率下降26.3%。
- **热点延伸**：[I2VT](#i2vt)、[HOG-WAM](#hog-wam)

## 对当前研究的启发
- **EnvironmentEvolve**
  - 迁移｜从 [RepoFactory](#repofactory) 把实现范围、结构耦合度用于环境预筛：排序后仅对高分仓库运行智能体求解。
  - 延续｜[RepoFactory](#repofactory) 主要覆盖Python且首批环境未进化：扩展至JavaScript，比较进化前后求解率与迁移收益。
- **TaskEvolve**
  - 迁移｜从 [Play2Evolve](#play2evolve) 把趣味拆成可诊断反馈用于作品验收：逐轮试玩、定位缺陷并验证修改增益。
  - 迁移｜从 [VibeVideoAgent](#vibevideoagent) 把局部预览用于长程任务验收：每个里程碑检查画面、声音和时间轴证据。
- **RobotEvolve**
  - 迁移｜从 [PyRUA-Dex](#pyrua-dex) 把技能表示为可组合程序用于双手策略生成：与示范学习比较成功率和跨物体泛化。
- **CacheEvolve**
  - 迁移｜从 [MoLT](#molt-kv) 把跨循环KV选择用于固定预算缓存：对比完整缓存和近期保留，测困惑度、延迟与显存。
- **NewModel**
  - 迁移｜从 [DyLoMo-DiT](#dylomo-dit) 把噪声感知计算分配用于高效DiT：分阶段调整循环次数，测画质、时延和参数量。
- **EvalEvolve**
  - 迁移｜从 [EgoUseBench](#egousebench) 把动态观察流用于操作评测：中途改变证据与意图，统计动作撤回率和最终成功率。
- **ReasoningEvolve**
  - 迁移｜从 [DocSEAM](#docseam) 把相邻页双向融合用于长文档推理：对比独立分页编码，测跨页定位与问答准确率。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-27/  

