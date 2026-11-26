# 2026-11-26 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **经验自进化**
  - [SIM](#sim)：把每次修改的依据、预期和实测结果写入可续写记忆，使智能体能跨模型、跨数据集复用改进经验。
  - [Harness Learning](#harness-learning)：让小型提案模型依据执行反馈持续改写运行框架，使冻结模型跨任务平均超过大七倍的教师模型。
- **系统演化**
  - [EvolonAI](#evolonai)：把国产芯片上的真实运行结果变成训练信号，自动优化算子、缓存和调度，替代逐平台人工调优。
  - [AutoRLBench](#autorlbench-rl)：以真实强化学习训练事故检验诊断、归因和修复能力，揭示现有智能体整体通过率最高仅33.3%。
  - [NightWatch](#nightwatch)：用轻量监视器在主模型思考时持续追踪界面，避免智能体按过期截图误操作或空等。
- **具身智能**
  - [ACAP](#acap)：让常驻编码智能体异步控制不同机器人部件，仅在物理依赖出现时协调，使任务耗时降低28.2%。
  - [RoboDojo-Mirror](#robodojo-mirror)：用不改变任务的镜像场景暴露机器人混淆倒影与实体的问题，成功率最高下降62.5个百分点。
  - [S-Mind](#s-mind)：用受监督的空间令牌融合多视图并转换观察视角，让多模态模型在内部形成三维场景表示。
  - [PartAgent](#partagent)：融合三维区域和多视图证据，再由智能体检查并修正分区，解决一次性部件分割难以纠错的问题。
- **模型架构**
  - [LoomFormer](#loomformer)：按词元动态调整注意力头之间的信息路线，仅增加2%算力便提升不同规模模型的性能。
  - [Qwen-Image-HD](#qwen-image-hd)：只训练局部图块，生成时结合邻域与压缩全局历史，降低4K图像成本并抑制重复条纹。

## 对当前研究的启发
- **MemoryEvolve**
  - 迁移｜从 [SIM](#sim) 把“依据—预期—实测—结论”用到经验写入：按四字段存改动，检索时与代码共同返回
  - 延续｜[SIM](#sim) 未保存落选方案且检索成本未知：对比仅胜者与全候选记忆，测迁移成功率、token 和延迟
- **HarnessEvolve**
  - 迁移｜从 [Harness Learning](#harness-learning) 把执行反馈用到框架优化：冻结主模型，由小模型改写框架并按任务得分迭代
  - 迁移｜从 [NightWatch](#nightwatch) 把流式状态校验用到长程执行：对比快照、定时刷新和持续监视的误操作率与成本
- **InfraEvolve**
  - 迁移｜从 [EvolonAI](#evolonai) 把真实运行反馈用到推理栈搜索：联合优化算子、缓存和调度，按正确性、时延、吞吐择优
- **EvalEvolve**
  - 延续｜[AutoRLBench](#autorlbench-rl) 缺少无报错及后期故障：各新增20例，测根因定位率和修复通过率
  - 迁移｜从 [RoboDojo-Mirror](#robodojo-mirror) 把镜像变换用到动态评测：生成反射场景，统计成功率跌幅、误识别率和接触偏差
- **RobotEvolve**
  - 迁移｜从 [ACAP](#acap) 把部件级异步自治用到多臂控制：对比单智能体与固定分工，测成功率、碰撞和耗时
- **PhysicalEvolve**
  - 迁移｜从 [PartAgent](#partagent) 把证据驱动纠错用到场景解析：融合二维视图与三维区域后复检重分，测IoU和修正轮数
- **NewModel**
  - 迁移｜从 [LoomFormer](#loomformer) 把逐词元头间路由用到架构实验：同参数同算力对比标准注意力的困惑度与吞吐

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-26/  

