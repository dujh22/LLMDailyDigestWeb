# 2026-11-21 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **推理时适应**
  - [Forward-Only Passes](#forward-only-passes)：以前向激活的角度集中度筛除低贡献权重分量，让模型无需反向传播即可低成本在线适配任务。
- **具身闭环**
  - [TuringSpace](#turingspace)：用程序化交互验证码把空间判断绑定到点击拖拽行动，微调后任务成功率从1.6%升至33.1%。
  - [Mind2Act World](#mind2act-world)：把机器人测试拆成推理、动作和闭环组合三类，定位单项能力正常但协同失败的瓶颈。
  - [ZeroVLN](#zerovln)：用语义工具接口连接视觉判断与连续控制，无需微调视觉语言模型即可通过闭环强化学习掌握导航。
  - [Depth Pro 2](#depth-pro-2)：以统一网络在原生分辨率生成深度图，同时解决单帧边界模糊和视频跨帧抖动。
- **多模态模型**
  - [WeMM-Video](#wemm-video)：统一训练音频与视觉，并按任务切换快速回答和显式推理，35B版本刷新开源音视频理解最佳成绩。
  - [HiUni](#hiuni)：让视觉理解与图像生成共享编码器和主干，仅在输出端恢复空间细节，减少任务专用计算。
- **可控生成**
  - [Coda-DaVinci](#coda-davinci)：由智能体按任务选择三维场景代理的粒度并仿真复核，同时控制视频结构、运动和长时一致性。
- **热点延伸**：[AGI之后是什么](#agi-asi)、[MC-Lens](#mc-lens)、[PMD](#pmd)、[EgoCaptioner](#egocaptioner)、[VODA](#voda)

## 对当前研究的启发
- **ReasoningEvolve**
  - 迁移｜从 [Forward-Only Passes](#forward-only-passes) 把角度集中度用于在线选秩：逐层裁剪SVD，测精度、时延和显存。
  - 延续｜[Forward-Only Passes](#forward-only-passes) 尚未验证深层LLM扩展性：对比逐层与全局选秩，测收益随层数的变化。
- **EvalEvolve**
  - 迁移｜从 [Mind2Act World](#mind2act-world) 把能力拆分诊断用于具身评测：分别报告推理、动作、闭环成功率及组合损失。
  - 延续｜[TuringSpace](#turingspace) 暴露模型固守错误视觉信念：注入截图误读，统计纠错率、幻觉辩护率和恢复步数。
- **EnvironmentEvolve**
  - 迁移｜从 [TuringSpace](#turingspace) 把程序化验证码用于自动课程：按成功率调节遮挡、几何关系和操作链长度。
- **RobotEvolve**
  - 延续｜[Mind2Act World](#mind2act-world) 留下推理与动作耦合问题：对比开环、定步重规划和反馈触发重规划，测成功率与恢复率。
- **AgentTrainEvolve**
  - 迁移｜从 [ZeroVLN](#zerovln) 把语义工具接口用于具身RL：冻结视觉语言模型，只训练工具选择器和连续动作专家。
- **NewModel**
  - 迁移｜从 [HiUni](#hiuni) 把共享骨干用于统一视觉模型：对比共享与分离骨干的理解、生成质量及训练成本。
- **NewApply**
  - 延续｜[Coda-DaVinci](#coda-davinci) 留下长视频转场不稳问题：对比固定与自适应代理，测转场一致性和场景遵循率。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-21/  

