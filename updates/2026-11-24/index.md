# 2026-11-24 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **科学发现**
  - [量子算法智能体](#lean)：多智能体搜索量子电路并用 Lean 证明正确性，在无法实测时仍将部分算术构件加速 290 倍。
  - [VP≠VNP](#vp-vnp)：把张量秩转成几何距离并穷尽两类分支，声称证明 VP≠VNP，但核心命题仍待独立核验。
  - [MIM](#mim)：用代数变换消除密码攻击中的干扰变量，把多项原需数小时的攻击压缩到秒级。
  - [MatHarness](#matharness)：以持久研究制品、执行审计和多智能体协作支撑数周科研，避免长周期实验失去证据链。
- **递归改进**
  - [MetaRSI/RSI²](#metarsi-rsi)：让数据、脚手架和模型沿双轴共同演化，并用不可改写的验证边界防止改进规则自证成功。
  - [SRO](#sro)：监测自奖励信号何时失真，并投影过滤危险更新方向，避免迭代训练跨过阈值后突然崩溃。
- **智能体评测**
  - [HarnessDev](#harnessdev)：把“搭建执行框架”和“用框架完成任务”分开测试，识别模型管理工具循环与故障恢复的能力。
  - [RDQA](#rdqa)：要求智能体实际获取并解析原始文件，揭示答对不等于完成查证，最佳调整后准确率仅 24%。
  - [MASSys](#massys)：在不同服务平台和负载下复跑同一多智能体流程，发现速度排名与有效质量会随环境逆转。
  - [二维推理](#item-67)：把推理拆成语义依赖图，识别答案虽对但步骤隐瞒关键依赖或包含无效绕路的情况。
- **上下文计算**
  - [Markovian Reasoning LLM](#markovian-reasoning-llm)：只传递未来推理所需的固定大小状态，阻止长推理的 KV 缓存随步骤持续增长。
  - [Declarative Attention](#declarative-attention)：让模型逐步声明需要查看多少上下文，减少无关缓存读取、显存占用和延迟。
  - [RLM-27B](#rlm-27b)：用程序递归拆解长任务，使短任务训练可泛化到最长 64 倍的任务并降低推理成本。
- **能力编排**
  - [STRIDE](#stride)：把全局策略常驻、局部战术按需加载，并用事件级反馈解决扁平技能库的信用分配问题。
  - [GLM-5.4](#glm-5-4)：用共享权重循环层增加计算深度，并复用跨轮缓存控制参数量与部署成本。
- **热点延伸**：[Future-OPSD](#future-opsd)、[RTC](#rtc)、[StereoVLM](#stereovlm)、[Uni3Sim](#uni3sim)、[PURE](#pure)

## 对当前研究的启发
- **Awesome-RSI**
  - 迁移｜从 [MetaRSI/RSI²](#metarsi-rsi) 把不可改写验证器用于改进闭环：隔离提案与验收权限，拒绝过期工件
  - 迁移｜从 [SRO](#sro) 把自奖励保真度用于迭代监控：逐轮估计失真阈值，对比过滤更新前后的退化率
- **ResearchEvolve**
  - 迁移｜从 [量子算法智能体](#lean) 把形式证明作为昂贵实验的替代反馈：证明候选正确后再分配实测预算
  - 延续｜[MatHarness](#matharness) 留下跨材料泛化与人工审批依赖：扩展晶面和覆盖度，对比全自动与审批流程的错误率
- **EvalEvolve**
  - 延续｜[RDQA](#rdqa) 留下证据区域未核验问题：检查页码、单元格和时间段重合率，并与答案准确率联合报告
  - 迁移｜从 [MASSys](#massys) 把服务环境纳入评测变量：跨平台和负载复跑，比较交付率、质量、延迟与成本
- **CacheEvolve**
  - 迁移｜从 [Markovian Reasoning LLM](#markovian-reasoning-llm) 把固定状态接口用于长链推理：对比完整缓存的显存、准确率与长期漂移
  - 迁移｜从 [Declarative Attention](#declarative-attention) 把注意力范围声明用于缓存调度：记录读取比例、延迟及答案损失
- **Groom**
  - 迁移｜从 [二维推理](#item-67) 把语义依赖图用于 token 归因：标记有效路径与绕路，统计单位有效 token 成功率
- **AgentTrainEvolve**
  - 迁移｜从 [STRIDE](#stride) 把策略常驻、战术按需检索用于技能训练：按事件回传奖励，对比扁平技能池成功率

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-24/  

