# 2026-11-24 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **形式化科研**
  - [量子算法智能体](#lean)：以多智能体搜索量子电路、Lean自动证明正确性，绕过昂贵实验验证，常用算术构件最高加速290倍。
  - [VP≠VNP](#vp-vnp)：把张量秩转成几何距离并穷尽两类分支，绕过关键结构难分类的问题，声称证明任意域上VP≠VNP。
  - [MIM](#mim)：用代数降维消除密码攻击中的干扰项并生成可执行代码，把多项攻击从数小时压到数秒。
- **递归改进**
  - [MetaRSI/RSI²](#metarsi-rsi)：让数据、脚手架和模型沿双轴共同演化，突破只改权重且改进规则固定的上限。
  - [Self-WSP](#self-wsp)：让模型直接读取并修改少量自身权重，无需外部编辑器，使GSM8K准确率从11.8%升至62.2%。
  - [SRO](#sro)：先诊断自奖励是否失真，再投影掉高风险更新方向，防止模型在反复自我训练中能力崩溃。
- **科研智能体**
  - [MatHarness](#matharness)：用持久研究制品、执行审计和多智能体协作维持数周科研状态，完成从选题到论文的材料研究。
  - [MLEvolver](#mlevolver)：保留可独立检索的完整尝试并删除闲置技能，避免摘要丢失证据和经验库无限膨胀。
- **可信评测**
  - [HarnessDev](#harnessdev)：先让模型自建执行框架再运行任务，补足传统评测只测模型、不测外部控制系统的缺口。
  - [RDQA](#rdqa)：把原始文件访问和解析轨迹纳入成功条件，揭示答案正确却没有真正查证的问题，最佳调整后准确率仅24%。
  - [MASSys](#massys)：在不同服务基底与负载下复跑同一多智能体任务，发现速度排名和有效质量会随执行环境逆转。
- **长程技能**
  - [STRIDE](#stride)：常驻全局策略、按需加载局部战术并给予事件级反馈，解决扁平技能池检索和信用分配粗糙的问题。
  - [ADAPT](#adapt)：联合训练小模型何时求助强模型及如何跨步执行建议，使长程任务成功率提高约32至53个百分点。
- **缓存推理**
  - [Markovian Reasoning LLM](#markovian-reasoning-llm)：只跨步骤传递未来所需的结构化状态，使长链推理缓存不再随历史持续增长。
  - [DisSparse](#dissparse-top-p)：用流水化Top-p选块和词元重排按需读取上下文，避免固定Top-k浪费带宽或漏掉信息，批量上限提升8倍。
- **热点延伸**：[Future-OPSD](#future-opsd)、[RTC](#rtc)、[StereoVLM](#stereovlm)、[Uni3Sim](#uni3sim)、[PURE](#pure)

## 对当前研究的启发
- **Awesome-RSI**
  - 迁移｜从 [MetaRSI/RSI²](#metarsi-rsi) 把工件新鲜度合约用于RSI循环：每轮刷新自我描述，过期依赖自动失效并回滚。
  - 延续｜[Self-WSP](#self-wsp) 留下权重编辑是否真正被模型理解的问题：对比随机搜索与模型编辑，评估增益、复现率和可解释性。
- **ResearchEvolve**
  - 迁移｜从 [量子算法智能体](#lean) 把形式证明作为科研搜索反馈：候选方案须通过Lean编译，再按正确率与优化幅度筛选。
  - 延续｜[MatHarness](#matharness) 留下晶面与覆盖度例外：扩展实验条件并与人工研究流程比较复现率、例外发现率和成本。
- **Groom**
  - 迁移｜从 [RDQA](#rdqa) 把原始证据访问设为有效token条件：区分答案正确但无证据与轨迹可核验两类成功。
  - 迁移｜从 [MASSys](#massys) 把服务基底纳入Harness评测：跨模型服务与负载复跑，报告排名翻转、交付率和单位有效token成本。
- **CacheEvolve**
  - 迁移｜从 [Markovian Reasoning LLM](#markovian-reasoning-llm) 把最小充分状态用于长链推理：固定状态预算，对比全历史KV的准确率、漂移和显存。
  - 迁移｜从 [DisSparse](#dissparse-top-p) 把可变Top-p读取用于缓存调度：对比固定Top-k的质量、带宽、批量上限和端到端延迟。
- **AgentEvolve**
  - 迁移｜从 [MLEvolver](#mlevolver) 把完整尝试独立存取与闲置技能删汰用于经验库：按复用次数淘汰并测后续任务收益。
- **AgentTrainEvolve**
  - 迁移｜从 [ADAPT](#adapt) 把求助时机与建议执行联合训练：对比固定路由和始终求助，评估成功率、顾问成本与执行遵循率。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-24/  

