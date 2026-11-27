# 2026-11-27 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **环境与任务**
  - [RepoFactory](#repofactory)：用代码规模与结构指标代替昂贵的智能体试做，低成本迭代长程编程训练环境。
  - [Play2Evolve](#play2evolve)：让智能体按趣味性反复试玩、诊断和修改游戏，补上“能运行但不好玩”的质量缺口。
  - [VibeVideoAgent](#vibevideoagent)：用短片段检查和音画分时钟反馈，在完整渲染前发现画面缺陷与不同步。
- **自主工程**
  - [TabbyML多智能体团队](#tabbyml)：用角色分工、实验契约和隔离验证组织20个智能体，使搜索查询总耗时降低31%。
  - [PyRUA-Dex](#pyrua-dex)：让编程智能体自主探索并组合双手操作程序，减少灵巧机器人对高质量示范的依赖。
- **模型效率**
  - [MoLT](#molt-kv)：把注意力缓存作为跨层循环记忆选择性复用，使循环模型最高获得1.7倍词元效率。
- **动态评测**
  - [EgoUseBench](#egousebench)：以持续变化的第一人称观察测试操作智能体，揭示动态场景成功率低26.3%。
  - [Real2SimLab](#real2simlab)：用统一程序接口连接不同仿真方法与原生评分器，免去跨基准重复适配。
- **热点延伸**：[I2VT](#i2vt)、[HOG-WAM](#hog-wam)、[PixelMatte](#pixelmatte)

## 对当前研究的启发
- **EnvironmentEvolve**
  - 迁移｜从 [RepoFactory](#repofactory) 把代码规模、实现范围和结构耦合度用于环境筛选：先按代理指标排序，再抽样运行智能体验证相关性
  - 延续｜[RepoFactory](#repofactory) 目前主要覆盖Python：补建Java与前端仓库，对比任务通过率、构建成功率和筛选成本
- **TaskEvolve**
  - 迁移｜从 [Play2Evolve](#play2evolve) 把趣味性拆成可诊断反馈用于作品演化：每轮试玩分别评估挑战、节奏和反馈，再定向改写
  - 迁移｜从 [VibeVideoAgent](#vibevideoagent) 把局部预览用于长程作品验收：按画面、音频和同步时钟分段检查，只回传缺陷证据
- **CodeEvolve**
  - 迁移｜从 [TabbyML多智能体团队](#tabbyml) 把实验契约用于代码优化：探索者提交假设与指标，验证者隔离复测后才允许合入
  - 延续｜[TabbyML多智能体团队](#tabbyml) 约350次实验仅6项获批：比较共享失败记录前后的重复实验率、通过率和总成本
- **CacheEvolve**
  - 迁移｜从 [MoLT](#molt-kv) 把KV缓存作为可选择读取的循环记忆：对比全量复用、门控复用与不复用的质量、时延和显存
- **EvalEvolve**
  - 迁移｜从 [EgoUseBench](#egousebench) 把观察与意图持续变化加入动态评测：中途改写任务条件，统计纠错时延、无效动作率和成功率
  - 迁移｜从 [Real2SimLab](#real2simlab) 把可执行程序定为统一评测契约：适配一次智能体接口，复用各基准原生评分器并核对分数一致性
- **RobotEvolve**
  - 迁移｜从 [PyRUA-Dex](#pyrua-dex) 把双手技能表示为可组合程序：由多智能体生成、试跑和精炼，再与示范学习比较成功率与迁移率

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-27/  

