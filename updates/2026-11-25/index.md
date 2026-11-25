# 2026-11-25 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归改进**
  - [GLM-5.5](#glm-5-5-rsi)：提出用沙箱留痕、运行时版本隔离和独立评判，避免自改进系统自己判定自己成功。
  - [HarnessPro](#harnesspro)：同时优化任务准确率与执行成本，避免脚手架自优化以不断增加调用和延迟换取性能。
  - [Harness2](#harness2)：把每次任务后的框架调整提炼成经验库，使新任务无需重新搜索整套脚手架。
- **脚手架优化**
  - [HarnessMM](#harnessmm)：把已验证动作固化为可执行决策图，跳过重复模型调用，减少近90% Token并提升14.3%准确率。
  - [JevAgentHarness](#jevagentharness-jev)：将快速决策模型嵌入执行框架，低延迟处理工具路由和记忆管理等高频选择。
- **经验记忆**
  - [ReHarness](#reharness)：依据后续任务成败反向修正已调用经验，并保留原始轨迹，解决错误经验写入后长期累积的问题。
- **具身进化**
  - [RoboUniverse-10K](#robouniverse-10k)：把真实操作视频转换为万级可验证仿真环境，以任务去重和物理验证减少机器人背题与奖励作弊。
  - [Native LAM](#native-lam)：从无动作标注视频的世界模型中提炼跨机器人动作表征，省去重训动力学模型和人工动作标注。
- **模型训练**
  - [PMOPD](#pmopd)：保护不同教师对应的参数更新子空间，减少数学、推理和代码能力蒸馏到同一模型时的相互干扰。
- **代码修复**
  - [FGL](#fgl)：用冻结修复器对候选代码范围的补丁可行性打分，减少27.5%无效阅读并提升小模型修复率。
- **科研协作**
  - [HFM](#hfm)：以“专家命题—Agent实验—公开验证”组织全球攻关，让自主科研结果可复验、可接续。
- **热点延伸**：[ViDecide](#videcide)

## 对当前研究的启发
- **Groom**
  - 迁移｜从 [HarnessMM](#harnessmm) 把“免回调命中率”加入过程评测：标注被决策图替代的调用及其节省Token与正确率。
  - 迁移｜从 [HarnessPro](#harnesspro) 把准确率—成本联合目标用于横评：绘制各Harness的成功率、Token和延迟帕累托前沿。
- **HarnessEvolve**
  - 迁移｜从 [GLM-5.5](#glm-5-5-rsi) 把独立评判用于回归验收：隔离修改者与评测器，并版本化保存沙箱轨迹。
  - 迁移｜从 [JevAgentHarness](#jevagentharness-jev) 把快慢路由用于高频控制：让Jev处理工具与记忆选择，低置信度再调用大模型。
- **MemoryEvolve**
  - 迁移｜从 [ReHarness](#reharness) 把结果反向修正用于经验库：任务结束后仅重写实际检索过的经验，并链接原始轨迹。
- **EnvironmentEvolve**
  - 延续｜[RoboUniverse-10K](#robouniverse-10k) 仍难处理柔性物体与双臂协作：分层生成任务，以成功率和接触误差评测。
- **EvolveLRM**
  - 延续｜[PMOPD](#pmopd) 尚未验证多教师持续扩展：逐步增加教师，对比普通混合蒸馏的冲突率、遗忘率和训练成本。
- **RobotEvolve**
  - 迁移｜从 [Native LAM](#native-lam) 把无标注视频动作表征用于VLA预训练：对比人工动作标签下的跨本体迁移成功率。
- **ResearchEvolve**
  - 迁移｜从 [HFM](#hfm) 把公开科研闭环用于项目管理：统一发布命题、实验配置、失败轨迹和可复现实验结果。
- **CodeEvolve**
  - 延续｜[FGL](#fgl) 的4B智能体仍受循环与编辑质量限制：加入循环检测，对比修复率、重复调用数和八分钟超时率。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-25/  

