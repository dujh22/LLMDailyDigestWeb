# 2026-11-26 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **自进化系统**
  - [SIM](#sim)：把每次程序修改的依据和实测结果写入可续写记忆，使智能体能跨模型、跨数据集复用改进经验。
  - [Harness Learning](#harness-learning)：让小模型依据执行反馈反复改写智能体框架，冻结主模型仍能跨任务提分并超过35B教师。
  - [EvolonAI](#evolonai)：把国产芯片上的真实运行性能作为机器反馈，自动迭代算子、缓存与调度，替代人工硬件适配。
  - [Agnes Harness](#agnes-harness)：让现场工程师连接业务与设备，再将验证过的流程封装成插件，解决企业智能体经验难复用的问题。
- **智能体可靠性**
  - [AutoRLBench](#autorlbench-rl)：用真实强化学习训练事故检验智能体能否定位并修复故障，最高整体通过率仅33.3%。
  - [NightWatch](#nightwatch)：以轻量监视器在主模型思考时持续追踪界面，避免动态网页和桌面操作因旧快照而误点或空等。
- **具身空间**
  - [ACAP](#acap)：让多个常驻编码智能体异步控制机器人部件，仅在物理依赖出现时协调，使任务耗时降低28.2%。
  - [S-Mind](#s-mind)：用受监督的空间令牌融合多视图并变换视角，使多模态模型无需外部几何工具也能进行三维推理。
  - [RoboDojo-Mirror](#robodojo-mirror)：用不改变任务的镜像场景暴露机器人混淆倒影与实体的问题，成功率最高下降62.5个百分点。
- **数据与生成**
  - [ThinkMorph-SSL](#thinkmorph-ssl)：用着色、去噪等视觉任务自动生成图文推理示范，缓解专项数据稀缺并使12项基准平均提升11.33点。
  - [Qwen-Image-HD](#qwen-image-hd)：以局部图块训练和分块自回归生成4K图像，降低整图训练成本并抑制重复条纹。

## 对当前研究的启发
- **MemoryEvolve**
  - 延续｜[SIM](#sim) 留下长期记忆成本与检索扩展性未验证：对比全量、摘要和因果记录，测收益、召回率与token成本。
- **SystemEvolve**
  - 迁移｜从 [Harness Learning](#harness-learning) 把“小模型提案—执行—反馈”用于工作流演化：冻结主模型，按验证集得分保留版本。
- **InfraEvolve**
  - 迁移｜从 [EvolonAI](#evolonai) 把真实硬件运行反馈用于推理栈搜索：联合优化算子、缓存和调度，按吞吐、时延、显存筛选。
- **AgentEvolve**
  - 迁移｜从 [NightWatch](#nightwatch) 把流式状态校验用于长程操作：主模型推理期间监测界面变化，动作前拒绝过期状态。
- **HarnessEvolve**
  - 迁移｜从 [Agnes Harness](#agnes-harness) 把验证过的现场流程用于插件库：记录版本、适用条件与回归测试，跨客户复用。
- **EvalEvolve**
  - 延续｜[AutoRLBench](#autorlbench-rl) 缺少隐性和后期故障：注入无报错、多组件耦合事故，评测归因率、修复率与训练恢复成本。
- **RobotEvolve**
  - 迁移｜从 [ACAP](#acap) 把部件级异步自治用于多臂控制：对比单体与固定分工，测成功率、耗时和协调调用次数。
- **PhysicalEvolve**
  - 迁移｜从 [S-Mind](#s-mind) 把空间令牌监督用于多视图状态建模：训练后移除专用令牌，测试三维推理保留率。
- **DataEvolve**
  - 迁移｜从 [ThinkMorph-SSL](#thinkmorph-ssl) 把视觉前置任务用于合成推理数据：按任务类型消融，测数据量、增益和错误传播率。
- **NewModel**
  - 迁移｜从 [Qwen-Image-HD](#qwen-image-hd) 把局部训练与压缩全局历史用于高清生成：对比整图训练，测显存、速度和全局一致性。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-26/  

