# 2026-09-23 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归自我改进从概念框架走向可运行闭环**：今天多项工作贯通经验回流、后训练与自我改写，包括将 Harness 运行经验转为评测和训练信号的[基元律动](#条目agent)、以 75 万条智能体轨迹开展大规模 RL 的[MiMo-V2.6](#条目mimo-v2-6-rl-rsi)，以及迭代改写并筛选自身代码的科研智能体[AIDE²](#条目item-42)。
- **智能体基础设施聚焦规模、可靠性与可控执行**：[DSec](#条目deepseek-dsec-5000-agent)实现每秒创建 5000 余个训练沙盒，[FIRE](#条目fire)利用历史失败进行运行时干预，[Agensh](#条目agensh-1-024)与[MAGIC](#条目magic)则分别探索千智能体自组织协作和强化学习驱动的动态协作图；企业产品也开始采用统一 Harness、验收返工和执行前确认。
- **模型竞争由峰值能力转向长程任务的单位成本**：[GPT-6 Sol、Luna 与 Claude Opus 5.5](#条目gpt-6-sol-luna-claude-opus-5-5)将推理效率和规模化成本置于核心，[Grok 4.7](#条目grok-4-7-coding-agent)扩展至 50 万 Token，而[CliffCompaction](#条目cliffcompaction)通过保守上下文压缩在百万级词元任务中最高节省 50% 成本。
- **智能体评测进一步转向真实闭环并审计测量有效性**：[Brood War Bench](#条目brood-war-bench-19)显示实时任务的观察—决策—执行时延可压倒纯推理优势，[SWE-Serve](#条目swe-serve)以生产级推理服务变更检验工程正确性；同时，[漏洞修复指标审计](#条目llm)和[本地工具调用评测审计](#条目item-35)分别揭示代理指标与服务栈混杂造成的能力误判。
- **具身与世界模型以空间表征、视频经验和记忆支撑长程泛化**：[RoboDawn](#条目robodawn)用离散接口让 VLM 零任务训练控制机器人，[Grounded Action Model](#条目grounded-action-model-3d)构建对象中心 3D 表征，[Zeva-Ego](#条目zeva-ego)以第一视角视频和因果记忆实现部署期提升，[WorldCrafter](#条目worldcrafter)则借助隐式三维记忆保持长时多视角一致性。
- **训练与测试时优化更强调在策略数据、有效搜索和过程可观测性**：[onPanda](#条目onpanda)以首错令牌纠正低成本构建在策略数据，[类别感知迭代专家训练](#条目item-11)和[低比特在策略蒸馏](#条目item-33)改善专门化与量化模型能力，[学习推理搜索策略](#条目item-34)则用语义多样化概念提升固定预算下的 pass@k；隐藏思维链提取与无意义填充词实验进一步暴露过程监控挑战。

## 对当前研究的启发
- **Awesome-RSI**：[基元律动](#条目agent)、[MiMo-V2.6](#条目mimo-v2-6-rl-rsi)与[AIDE²](#条目item-42)分别提供“经验回流—大规模轨迹 RL—自我代码改写”三类 RSI 闭环实例，可用于补充自主性层级以及持续增益、退化和作弊风险的比较维度。
- **HarnessEvolve**：[DSec](#条目deepseek-dsec-5000-agent)的高吞吐隔离沙盒、[FIRE](#条目fire)的失败状态干预和[本地工具调用评测审计](#条目item-35)揭示的服务栈混杂，可共同转化为 Harness 的环境规范、故障反馈机制与配置披露要求。
- **EvolveLLM**：[MiMo-V2.6](#条目mimo-v2-6-rl-rsi)表明跨软件工程、多模态和长程执行的大规模多任务轨迹 RL 可作为通用模型自我改进路线，而[onPanda](#条目onpanda)提供了保持模型采样分布的低成本纠错数据构造方法。
- **EvolveLRM**：[超越重复采样：学习大模型推理搜索策略](#条目item-34)说明可训练轻量概念生成器来优化冻结模型的测试时探索分布，为研究固定 Token 预算下的搜索效率与能力增益提供直接方案。
- **EvalEvolve**：[SWE-Serve](#条目swe-serve)、[EquivSVA](#条目equivsva-rtl)和[漏洞修复评测审计](#条目llm)分别提供真实生产任务、等价行为变体和构念效度校验，可用于设计兼具动态性、实现无关性与执行证据的进化式代码评测。
- **Groom**：[Brood War Bench](#条目brood-war-bench-19)对实时闭环效率的发现与[CliffCompaction](#条目cliffcompaction)的低成本长上下文压缩，提示过程级 Token 归因应同时记录观察滞后、重复上下文、恢复开销及其对最终成功的边际贡献。
- **MemoryEvolve**：[SpeakerMem-R1](#条目speakermem-r1)的说话者中心双轨记忆和[Zeva-Ego](#条目zeva-ego)的因果动作记忆，分别给出长期对话状态重建与部署经验转化为能力的可验证记忆机制。
- **SwarmEvolve**：[Agensh](#条目agensh-1-024)证明无中心异步协作可扩展至 1,024 个智能体，[MAGIC](#条目magic)则展示用密集奖励动态选择单体或智能体组，可用于研究协作拓扑自动演化及性能—成本权衡。
- **ResearchEvolve**：[AI 科研智能体的递归自我改进](#条目item-42)通过代码改写、自动评测和候选筛选获得跨任务泛化，为自主科研系统建立“可执行产物—外部评测—版本选择”的连续改进闭环提供了具体模板。
- **DataEvolve**：[TransBERT](#条目transbert)证明纯合成翻译语料也能支撑低资源专业领域预训练，可进一步研究翻译数据的自动筛选、配比迭代及领域覆盖度如何影响数据飞轮。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-09-23/  

