# 2026-11-24 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **自动科研**
  - [VP≠VNP](#vp-vnp)：把张量秩转成非正曲率空间距离并穷尽两类几何分支，声称解决任意域上的 VP 与 VNP 分离问题。
  - [量子算法智能体](#lean)：多智能体搜索量子电路、Lean 证明正确性，以形式验证替代昂贵实测，算术构件最高加速 290 倍。
  - [MIM](#mim)：用代数变换消除密码问题中的干扰项、压缩未知空间，将多种攻击从数小时缩短至数秒。
  - [MatHarness](#matharness)：以持久研究制品、执行审计和多智能体协作维持数周科研，使选题、实验、纠错与成稿形成可追溯闭环。
- **递归改进**
  - [MetaRSI/RSI²](#metarsi-rsi)：同时演化数据、脚手架与模型，并用工件新鲜度和固定验证边界解决只改权重、规则不更新的问题。
  - [Self-WSP](#self-wsp)：让模型直接读取并修改自身少量权重，无需外部编辑器便将 GSM8K 准确率从 11.8% 提至 62.2%。
  - [SRO](#sro)：用自奖励保真度识别反馈失真，再投影过滤危险更新方向，防止模型在反复自我训练中突然崩溃。
- **智能体评测**
  - [RDQA](#rdqa)：把原始文件访问和工具轨迹纳入成功条件，揭示“答案正确但没有真正查证”，最佳调整后准确率仅 24.0%。
  - [HarnessDev](#harnessdev)：要求模型先搭建执行框架再运行任务，同时测量循环控制、工具调用和故障恢复能力。
  - [MASSys](#massys)：在不同服务后端与负载下复跑相同多智能体任务，发现速度排名和有效质量会随运行环境逆转。
- **长程执行**
  - [RLM-27B](#rlm-27b)：用程序化脚手架递归拆分长任务，使短任务训练泛化到最长 64 倍的任务并降低上下文成本。
  - [STRIDE](#stride)：让全局策略常驻、局部战术按需加载并接受事件级反馈，解决扁平技能库检索和归因粗糙的问题。
- **推理记忆**
  - [Declarative Attention](#declarative-attention)：让模型在推理过程中声明当前要看的上下文范围，避免每步扫描全部历史并降低显存与延迟。
  - [Markovian Reasoning LLM](#markovian-reasoning-llm)：只传递足以决定下一步的结构化状态，将随推理链增长的 KV 缓存改成固定大小。
- **运行时防护**
  - [Shirudo](#shirudo-ebpf)：让智能体动态生成 eBPF 内核规则，不停服即可封堵漏洞利用路径，为正式补丁争取时间。
- **热点延伸**：[Future-OPSD](#future-opsd)、[RTC](#rtc)、[StereoVLM](#stereovlm)、[Uni3Sim](#uni3sim)、[PURE](#pure)

## 对当前研究的启发
- **Awesome-RSI**
  - 迁移｜从 [MetaRSI/RSI²](#metarsi-rsi) 把工件新鲜度合约用于改进闭环：每轮强制重验数据、脚手架和模型版本依赖。
  - 延续｜[Self-WSP](#self-wsp) 未证明模型理解权重编辑：对比定向编辑、随机编辑和梯度更新的增益复现率与机制预测率。
- **ResearchEvolve**
  - 迁移｜从 [量子算法智能体](#lean) 把形式证明用作实验反馈：为候选算法生成 Lean 规格，仅保留通过检查的方案。
  - 延续｜[MatHarness](#matharness) 仍需人工审批：对比固定检查点与风险触发审批，评估有效发现、成本和人工介入次数。
- **EvalEvolve**
  - 迁移｜从 [MASSys](#massys) 把服务环境纳入评测变量：跨后端与负载复跑任务，报告质量、延迟、成本和未交付率。
- **HarnessEvolve**
  - 迁移｜从 [HarnessDev](#harnessdev) 把“先造框架、再跑任务”用于模型选型：分别评分框架质量、任务成功和恢复率。
- **GeneralizeEvolve**
  - 迁移｜从 [RLM-27B](#rlm-27b) 把递归任务拆分用于长度泛化：只训练短任务，在 2至64 倍长度上测成功率与成本。
- **CacheEvolve**
  - 迁移｜从 [Markovian Reasoning LLM](#markovian-reasoning-llm) 把最小状态接口用于固定预算缓存：对比完整 KV、滑窗和状态缓存的准确率与漂移。
- **Groom**
  - 迁移｜从 [RDQA](#rdqa) 把原始证据访问纳入 token 有效性：仅将命中标注页码、单元格或时间段的检索计为有效。
- **LogicEvolve**
  - 延续｜[VP≠VNP](#vp-vnp) 的四个核心命题待独立核验：复跑 Lean 证明并由另一套形式系统检查关键引理。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-24/  

