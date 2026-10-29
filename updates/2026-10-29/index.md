# 2026-10-29 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **基础模型与产品能力继续下沉**：多款模型围绕低成本长程智能体、端侧多模态与交互世界展开，其中 [OpenAI 发布 GPT-6.1 Terra：电脑操作能力比肩 Astra，成本降至十分之一](#openai-gpt-6-1-terra-astra) 以约十分之一成本逼近旗舰电脑操作能力，显示高阶 Agent 能力正快速商品化。
- **递归自我改进从模型扩展至 Harness、评判器与真实系统**：[The Trinity：能力驱动的多模态智能体递归自我改进](#the-trinity) 以能力树、可验证环境和可复用 Harness 构成闭环，[RuHarness：评判准则与智能体脚手架协同演化](#ruharness) 则进一步让评判准则与脚手架共同迭代。
- **Agent 训练转向可控环境合成与高价值交互**：[Trajectory2Gym：面向工具使用智能体的决策驱动交互合成](#trajectory2gym) 强调决策依据与依赖覆盖，[可控环境合成揭示工具使用智能体缩放定律](#item-58) 则给出了环境多样性与泛化能力之间的可预测关系。
- **持续学习与记忆研究开始核算“净收益”**：[DeepMind：自演化智能体能否持续学习？](#deepmind) 系统揭示稳定性、可塑性与遗忘矛盾，[Memory Tax：剖析智能体记忆的净价值](#memory-tax) 发现复杂记忆系统常不如朴素 RAG，而 [TTME：测试时记忆演化以更低成本助力科学发现](#ttme) 展示了冻结权重、只演化外部记忆的有效路径。
- **AI 科研进入“大规模产出—形式化验证—外部审验”阶段**：[数十个 AI Agent 24 天形式化有限单群分类定理](#ai-agent-24) 展示群体 Agent 与 Lean 的规模化结合，[OpenAI 邀外部专家与 Lean 核查 AI 科学证明](#openai-lean-ai) 则凸显重大主张必须经过独立复核；与此同时，[Ai2 发布新颖性评判基准，揭示 LLM 裁判高度不稳定](#ai2-llm) 对自动科研评审的可靠性提出警示。
- **热点延伸集中于主动式 AI 与多模态生成评测**：低相关性条目包括 [主动式 AI 如何走向超级智能体：6A 框架综述](#ai-6a)、[WorldCast：大角度相机控制下的世界一致角色视频生成](#worldcast) 与 [AV-FABLE：长视频视听篡改取证基准](#av-fable)，反映主动服务、生成一致性和内容取证仍是当日热点。

## 对当前研究的启发
- **Awesome-RSI**：[The Trinity：能力驱动的多模态智能体递归自我改进](#the-trinity) 与 [RuHarness：评判准则与智能体脚手架协同演化](#ruharness) 表明 RSI 闭环应同时演化环境、能力结构、评判准则和 Harness，而不能只优化模型输出。
- **AgentEvolve**：[TTME：测试时记忆演化以更低成本助力科学发现](#ttme) 证明冻结参数、持续改写外部记忆也能超过测试时训练，可作为部署后经验学习的低成本基线。
- **AgentTrainEvolve**：[Trajectory2Gym：面向工具使用智能体的决策驱动交互合成](#trajectory2gym) 与 [可控环境合成揭示工具使用智能体缩放定律](#item-58) 提供了从交互覆盖标准到数据规模预测的完整训练环境设计思路。
- **MemoryEvolve**：[Memory Tax：剖析智能体记忆的净价值](#memory-tax) 提示所有新记忆架构都应以原始历史检索或朴素 RAG 为强基线，并显式报告处理成本后的净收益。
- **HarnessEvolve**：[智能体接口的决策几何：策略如何内化 Harness 偏好](#harness) 说明模型会适配训练时接口，因此跨 Harness 比较必须区分接口能力上限与策略—接口匹配程度。
- **Groom**：[TraceTrial-Bench：智能体运行框架可靠性与故障归因基准](#tracetrial-bench) 的轨迹、多源证据和机制链归因可直接用于扩展过程级 token 归因，使成本分析同时落到具体故障与恢复环节。
- **InfraEvolve**：[ForgeKernel 登顶华为与英伟达算子评测榜](#forgekernel) 证明真实硬件反馈驱动的生成—验证—迭代闭环已具备跨硬件迁移能力，可作为基础设施自进化的重点工程范式。
- **ResearchEvolve**：[数十个 AI Agent 24 天形式化有限单群分类定理](#ai-agent-24) 与 [OpenAI 邀外部专家与 Lean 核查 AI 科学证明](#openai-lean-ai) 表明自主科研系统应把机器可检验证明、原稿一致性检查和外部专家审验设为默认交付链。
- **EvalEvolve**：[Ai2 发布新颖性评判基准，揭示 LLM 裁判高度不稳定](#ai2-llm) 说明科研新颖性不能依赖单次 LLM 打分，评测协议需纳入跨提示、跨模型方差及人工校准。
- **RobotEvolve**：[智元 Genie Master 在便利店跑通具身递归自我改进](#genie-master) 展示了真实业务中“失败诊断—自主练习—策略更新”的双路径闭环，可用于设计 sim-to-real 之外的现场持续改进机制。
- **HumanEvolve**：[Anthropic实验：AI建议显著影响专家决策与自我归因](#anthropic-ai) 表明人机协同评测不仅要测任务增益，还应测立场诱导、影响觉察和用户对决策来源的错误归因。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-29/  

