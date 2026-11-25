# 2026-11-25 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **自改进闭环**
  - [GLM-5.5](#glm-5-5-rsi)：用沙箱留痕、运行时版本化和独立评判验证系统自改是否真实增益，避免修改者操纵评测。
  - [HFM](#hfm)：以“专家命题—Agent 实验—公开验证”组织全球协作，让自主科研结果可复验、可接续。
- **脚手架演化**
  - [ReHarness](#reharness)：依据后续任务成败反向修正曾被调用的经验，解决错误记忆写入后长期固化的问题。
  - [HarnessMM](#harnessmm)：把验证过的动作固化为可执行决策图，跳过重复模型调用，减少近 90% Token。
  - [HarnessPro](#harnesspro)：联合优化任务准确率、成本与延迟，避免脚手架自优化以无限增加资源换取效果。
  - [JevAgentHarness](#jevagentharness-jev)：把低延迟决策模型嵌入工具路由和记忆管理，让高频控制无需反复生成文本。
  - [Harness2](#harness2)：每次任务后提炼脚手架优化经验并跨任务复用，避免为每个新任务重新搜索执行框架。
- **训练优化**
  - [PMOPD](#pmopd)：保护不同教师的参数更新子空间，减少数学、推理和代码能力合并时的相互干扰。
  - [智能体强化学习](#item-20)：分别缩放环境、任务和轨迹数量，以覆盖广度而非重复轨迹指导训练预算，成功率提升 8.4 个百分点。
  - [FGL](#fgl)：用修复器判断哪些代码范围最可能产生正确补丁，训练定位器少读 27.5% 代码并提高修复率。
- **具身学习**
  - [RoboUniverse-10K](#robouniverse-10k)：把真实操作视频转成万级可验证仿真任务，以去重和物理校验减少机器人训练背题。
  - [Native LAM](#native-lam)：从无动作标注视频的世界模型中提取跨机器人动作表征，免去重新训练动力学教师。
- **热点延伸**：[ViDecide](#videcide)

## 对当前研究的启发
- **Awesome-RSI**
  - 迁移｜从 [GLM-5.5](#glm-5-5-rsi) 把独立评判与运行时版本化用到 RSI 验证：隔离修改者，逐版回归收益与风险。
- **EnvironmentEvolve**
  - 延续｜[RoboUniverse-10K](#robouniverse-10k) 留下柔性物体与双臂操作瓶颈：合成对应环境，对比刚体任务的成功率与接触误差。
- **MemoryEvolve**
  - 迁移｜从 [ReHarness](#reharness) 把结果反向修正用到记忆维护：失败后定位已检索经验，保留原轨迹并生成修订版。
- **Groom**
  - 迁移｜从 [HarnessMM](#harnessmm) 把已验证动作免回调用到 Token 归因：比较原始与决策图执行的成本、成功率和重复调用率。
- **JevEvolve**
  - 迁移｜从 [JevAgentHarness](#jevagentharness-jev) 把快模型用于工具路由：对比大模型路由的准确率、端到端延迟与升级率。
- **AgentTrainEvolve**
  - 延续｜[智能体强化学习](#item-20) 尚未验证 32B 以上模型：分轴扩展环境、任务和轨迹，拟合成功率与单位成本曲线。
- **EvolveLRM**
  - 延续｜[PMOPD](#pmopd) 尚未验证多教师持续接入：逐步增加教师，对比子空间保护、损失加权与顺序蒸馏的遗忘率。
- **ResearchEvolve**
  - 迁移｜从 [HFM](#hfm) 把公开实验记录用到自主科研闭环：统一记录假设、代码、失败实验和同行复验结果。
- **RobotEvolve**
  - 迁移｜从 [Native LAM](#native-lam) 把无标注视频动作提炼用于 VLA 预训练：对比人工动作标注的跨本体迁移成功率。
- **CodeEvolve**
  - 延续｜[FGL](#fgl) 留下超时、重复循环和编辑质量问题：加入循环检测与时间预算，对比修复率、耗时和无效编辑数。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-25/  

