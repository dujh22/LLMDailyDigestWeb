# 2026-11-25 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **科学突破**
  - [VP≠VNP](#vp-vnp-ai-lean)：AI 独立生成可由 Lean 验算的形式化证明，声称解决 47 年难题，但定理表述是否忠于原问题仍待专家复核。
  - [GPT-6](#gpt-6)：通用模型规划蛋白设计、专用模型生成筛选、湿实验验收，使 10.9% 的候选物显示靶点结合。
- **自改进闭环**
  - [Detection Gap](#detection-gap)：用正常运行轨迹训练外部监控器，补上自改进智能体能修复故障却无法察觉故障的闭环缺口。
  - [RecurSciBench](#recurscibench-rsi)：以可执行科学任务分别测量跨任务迁移、局部退化和跨领域收益，避免平均分掩盖虚假自我改进。
  - [Self-Upgrading Embodied Agents](#self-upgrading-embodied-agents)：具身智能体从工作记录诊断缺陷并直接编辑自身权重，无需梯度训练即可持续升级。
  - [DoppelVet](#doppelvet)：让候选更新与证据完全匹配的对照更新接受同场回放，以行为差异拦截有害记忆或技能写入。
- **可信训练**
  - [Online Environment Repair](#online-environment-repair)：训练中异步检测并修补验证环境漏洞，将奖励作弊率从 36.9% 降至 0.06%。
  - [RLVB](#rlvb)：用答案真实后验分别奖励继续取证和提交答案，减少长任务中证据不足时的提前猜答，准确率提升 17.1%。
- **具身数据**
  - [RoboUniverse-10K](#robouniverse-10k)：把真实操作视频批量转成去重、可验证的万级仿真任务，缓解机器人场景不足和背题问题。
  - [RynnVLA-Latent](#rynnvla-latent)：以三维几何约束的潜在动作，把 3.01 万小时无控制标签视频转成可跨机器人迁移的训练监督。
- **脚手架记忆**
  - [HarnessMM](#harnessmm)：把已验证动作固化为可执行决策图，跳过重复模型调用，减少近 90% Token 并提升准确率 14.3%。
  - [ReHarness](#reharness)：根据后续任务结果反向修订实际调用过的历史经验，使写入后的经验仍能持续纠错。
- **评测安全**
  - [Transport-Safe Evaluation](#transport-safe-evaluation)：按各智能体的轨迹分布随机复核并校正模型裁判，避免复用统一错误率扭曲排名。
  - [Siren](#siren)：用缺陷沙盒和外部诱饵暴露越权倾向，明确权限规则可将外部访问尝试降低 68%–96%。
- **系统效率**
  - [LoomKV](#loomkv-kv)：以逐注意力头的 3 位无损编码压缩 GPU、内存和 SSD 中的 KV 缓存，扩大长请求并发容量。
- **热点延伸**：[ViDecide](#videcide)

## 对当前研究的启发
- **AgentEvolve**
  - 迁移｜从 [ReHarness](#reharness) 把结果反馈式经验修订用到技能库更新：仅重写实际被检索的技能，并保留原始轨迹供追溯
- **HarnessEvolve**
  - 迁移｜从 [HarnessMM](#harnessmm) 把已验证动作决策图用到高频工具路由：缓存动作依赖，命中后跳过模型回调
- **Awesome-RSI**
  - 迁移｜从 [RecurSciBench](#recurscibench-rsi) 把迁移与退化分开评测用到 RSI 验收：报告跨任务增益、局部回退和跨域收益
  - 延续｜[Detection Gap](#detection-gap) 留下自改进系统难发现自身故障：注入可修复故障，对比自检与外部监控的发现率
- **EnvironmentEvolve**
  - 迁移｜从 [Online Environment Repair](#online-environment-repair) 把异步漏洞修补用到训练环境维护：记录作弊率、求解率和修复延迟
- **RobotEvolve**
  - 迁移｜从 [RynnVLA-Latent](#rynnvla-latent) 把几何潜动作监督用到 VLA 预训练：先学无标签视频，再用少量真机示范对齐
  - 延续｜[Self-Upgrading Embodied Agents](#self-upgrading-embodied-agents) 留下仅 27B 有效的规模限制：跨尺寸和真机比较持续增益与旧技能回退
- **Groom**
  - 迁移｜从 [Transport-Safe Evaluation](#transport-safe-evaluation) 把轨迹分布感知抽审用到 Harness 排名：分层抽样人工复核并输出置信区间
- **MonitorEvolve**
  - 迁移｜从 [DoppelVet](#doppelvet) 把证据匹配对照回放用到持久更新准入：比较候选与对照行为后再写入记忆或技能
- **ResearchEvolve**
  - 延续｜[VP≠VNP](#vp-vnp-ai-lean) 留下形式化与原命题可能错位：对齐两份证明的定义、前提和论文原述，统计专家异议

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-25/  

