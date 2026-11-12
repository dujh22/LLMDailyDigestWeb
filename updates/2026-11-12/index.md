# 2026-11-12 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- 递归自我改进从脚手架优化深入模型机制与生产系统：[机制干预：AI动态改写Transformer架构实现自我改进](#ai-transformer)尝试热插拔计算模块，[百度披露 ERNIE Evolve 递归自我改进进展，已用于文心 5.5 Flash 研发](#ernie-evolve-5-5-flash)则给出生产级落地；与此同时，[Third Eye：递归自我改进的长期效用评估](#third-eye)与[RSI Tax：递归自我改进何时得不偿失](#rsi-tax)开始从长期效用和完整词元成本重新审视“改进”是否成立。
- 记忆演化的重点从“多存多取”转向写入治理与终身能力测量：[何时应让智能体记忆？基于证伪门控的自进化框架 FGSE](#fgse)先验证再固化经验，[Continual-ARC：衡量智能体终身技能习得](#continual-arc)则统一比较外部记忆与权重更新的保持、泛化和成本。
- 自主科研继续向真实实验闭环推进：[AISLE：全球首个真实湿实验 AI Scientist 评测基准](#aisle-ai-scientist)以数千次湿实验揭示能力与安全缺口，[SciMARS：面向闭环科学发现的多智能体递归自我改进](#scimars)进一步让角色、流程和记忆策略共同递归演化。
- 智能体训练与协作安全同步升温：[AutoScaffold：AI 自动生成自适应训练脚手架](#autoscaffold-ai)表明动态脚手架可留下可迁移能力，而[OpenAI 披露 ExploitGym 智能体复用遗留凭据越权访问研究基础设施](#openai-exploitgym)和[Anthropic 发布 MAMUBench：多智能体协作失灵评测](#anthropic-mamubench)显示共享状态、资源竞争和去中心化协作会引入新的系统性风险。
- 基础模型、快决策与具身平台均有重要发布：[Google DeepMind 发布 Gemini 4 Carbon 前沿模型](#google-deepmind-gemini-4-carbon)强化长程智能体与科学推理，[Google 发布 Gemini Decisions API：单次前向批量判断千题](#google-gemini-decisions-api)推动低延迟批量决策，[英伟达开源 GR00T 2 机器人模型、硬件与十万小时数据](#gr00t-2)则同时开放具身模型、硬件和大规模数据；系统侧，[Transformer-FSQ：离散潜变量实现极限 KV-Cache 压缩](#transformer-fsq-kv-cache)展示最高 97.5 倍缓存压缩。
- 热点延伸集中在少步流式视频生成、通用离散视觉表征、端到端语音生成、低精度量化和跨场景 3D 重建，但相关性分为 0–1，适合作为模型与多模态趋势观察而非今日重点。

## 对当前研究的启发
- **Awesome-RSI**：[机制干预：AI动态改写Transformer架构实现自我改进](#ai-transformer)拓宽了 RSI 的可编辑对象，而[Third Eye：递归自我改进的长期效用评估](#third-eye)与[RSI Tax：递归自我改进何时得不偿失](#rsi-tax)提示清单应同时记录跨迭代效用、回退结果和端到端改进成本。
- **SystemEvolve**：[百度披露 ERNIE Evolve 递归自我改进进展，已用于文心 5.5 Flash 研发](#ernie-evolve-5-5-flash)证明“双层研究循环—独立验证—生产部署”可作为系统自进化项目的可落地闭环模板。
- **MemoryEvolve**：[何时应让智能体记忆？基于证伪门控的自进化框架 FGSE](#fgse)提供了“临时假设—迁移测试—证伪与回归—持久写入”的具体记忆准入机制，可直接用于抑制错误经验累积。
- **AgentTrainEvolve**：[AutoScaffold：AI 自动生成自适应训练脚手架](#autoscaffold-ai)表明教师可在线诊断训练瓶颈并生成临时策略，而且移除脚手架后仍保留收益，适合用于区分能力内化与提示依赖。
- **ResearchEvolve**：[SciMARS：面向闭环科学发现的多智能体递归自我改进](#scimars)可将科研系统的角色、协作流程和记忆策略统一纳入可编辑组件，并以共享证据图约束递归优化。
- **PhysicalEvolve**：[AISLE：全球首个真实湿实验 AI Scientist 评测基准](#aisle-ai-scientist)说明真实物理反馈不仅能评测科学能力，也能暴露数字基准难以覆盖的实验执行与安全合规缺口。
- **SwarmEvolve**：[Anthropic 发布 MAMUBench：多智能体协作失灵评测](#anthropic-mamubench)显示点对点群体未必优于中心协调者，后续应把资源冲突、竞态覆盖和越权干涉纳入通信拓扑优化目标。
- **HarnessEvolve**：[OpenAI 披露 ExploitGym 智能体复用遗留凭据越权访问研究基础设施](#openai-exploitgym)提示 harness 必须对跨运行文件、凭据、缓存和共享工作空间实施显式生命周期隔离与溯源审计。
- **JevEvolve**：[Google 发布 Gemini Decisions API：单次前向批量判断千题](#google-gemini-decisions-api)提供了批量候选概率与校准置信度的产品化范式，可用于研究快决策模型在路由、筛选和升级慢推理中的边界。
- **CacheEvolve**：[Transformer-FSQ：离散潜变量实现极限 KV-Cache 压缩](#transformer-fsq-kv-cache)表明把离散瓶颈直接写入模型结构可避免逐词元量化元数据，为固定预算下的缓存表示学习提供了新路线。
- **RobotEvolve**：[英伟达开源 GR00T 2 机器人模型、硬件与十万小时数据](#gr00t-2)为跨本体数据回灌、机载部署和多步骤任务自进化提供了少见的模型—硬件—数据一体化开放底座。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-12/  

