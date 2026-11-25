# 2026-11-25 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **自改进闭环**
  - [Online Environment Repair](#online-environment-repair)：训练时异步修补被策略利用的验证漏洞，把奖励作弊率从36.9%降至0.06%。
  - [RecurSciBench](#recurscibench-rsi)：用独立、可执行的科学任务检验自我改进能否迁移，并同时暴露局部能力退化。
  - [Detection Gap](#detection-gap)：从正常运行轨迹学习故障模式，补上自改进智能体会修复却发现不了故障的盲区。
  - [DoppelVet](#doppelvet)：以证据完全相同的安全对照回放候选更新，在无安全标签时阻止有害记忆和技能持久化。
  - [SELFWRITE](#selfwrite)：让模型编程生成并递归合并自身的低秩权重修改，无需梯度即可持续提升数学能力。
- **智能体执行**
  - [HarnessMM](#harnessmm)：把已验证动作固化为可执行决策图，跳过重复模型调用并减少近90% Token。
  - [ReHarness](#reharness)：依据后续任务结果反向改写被调用的历史经验，让错误记忆能够持续纠正。
  - [RLVB](#rlvb)：用真实答案后验分别奖励取证与作答时机，减少证据不足时的提前猜答。
  - [Jev](#jev)：用专用快速模型处理有限动作路由，把内容生成留给大模型，成本最多降低49.6%。
- **具身学习**
  - [RoboUniverse-10K](#robouniverse-10k)：把真实操作视频转成万级可验证仿真环境，以任务去重和物理校验减少背题与奖励作弊。
  - [RynnVLA-Latent](#rynnvla-latent)：用三维几何约束的潜在动作，把3.01万小时无控制标签视频转成机器人预训练监督。
  - [预训练VLA持续学习](#vla)：用分布外测试和表征探针揭示经验回放只保住域内任务，预训练能力仍会因读出错位崩塌。
- **模型与系统**
  - [LoomKV](#loomkv-kv)：按注意力头进行三位无损编码，压缩GPU、内存和SSD中的KV缓存以扩大长请求并发。
  - [InstructReplay](#instructreplay)：回放初始模型自己的通用指令回答，把事实微调造成的能力平均降幅从28.1分压至2.4分。
- **形式化科研**
  - [VP≠VNP](#vp-vnp-ai-lean)：两套AI独立生成的Lean证明尝试解决47年难题，但形式验算仍不能替代定理表述的人类复核。
- **热点延伸**：[ViDecide](#videcide)

## 对当前研究的启发
- **Awesome-RSI**
  - 迁移｜从 [RecurSciBench](#recurscibench-rsi) 把独立任务迁移用于RSI验收：报告平均增益、退化任务数和跨域收益。
  - 迁移｜从 [DoppelVet](#doppelvet) 把证据匹配对照用于更新准入：持久化前回放新旧版本并比较有害行为率。
- **AgentEvolve**
  - 迁移｜从 [ReHarness](#reharness) 把结果反向修正用于经验库维护：任务结束后重评已检索经验并保留原轨迹。
  - 迁移｜从 [HarnessMM](#harnessmm) 把已验证动作图用于高频工具链：命中依赖条件时免调用模型并记录回退率。
- **AgentTrainEvolve**
  - 迁移｜从 [RLVB](#rlvb) 把“证据是否充足”用于长程RL奖励：分别奖励继续取证和提交，统计提前作答率。
  - 迁移｜从 [Online Environment Repair](#online-environment-repair) 把异步修补用于训练环境：检测作弊后修验证器并回放确认。
- **RobotEvolve**
  - 迁移｜从 [RynnVLA-Latent](#rynnvla-latent) 把几何潜动作用于视频预训练：先学状态变化，再用少量示教对齐控制。
  - 延续｜[预训练VLA持续学习](#vla) 留下表征可读性错位：对比旧头、新探针和骨干，测域外成功率与可恢复度。
- **CacheEvolve**
  - 迁移｜从 [LoomKV](#loomkv-kv) 把逐头无损编码用于分层缓存：接入vLLM后测压缩率、吞吐和首词延迟。
- **JevEvolve**
  - 迁移｜从 [Jev](#jev) 把有限动作专用路由用于工具选择：与通用模型对比成本、延迟、轨迹长度和成功率。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-25/  

