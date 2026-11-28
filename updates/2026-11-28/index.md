# 2026-11-28 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **协同进化**
  - [CoEvo-RSI](#coevo-rsi)：跨代保存并重组模型与脚手架，避免独立升级造成接口错配，使9B模型在垂直任务上超过大型模型。
  - [MetaSkill](#metaskill)：在具体技能之上增加可复用解题方法层，让智能体能跨任务重组技能并在失败后改换方法。
  - [Motubrain 2.0](#motubrain-2-0)：用统一动作表示和可编辑执行框架，把视频经验迁移到机器人，并依据执行反馈规划、验证和纠错。
- **改进验证**
  - [RSI 2026](#rsi-2026)：用自主性分级、独立留出集和等算力审计，区分真实的持续自我改进与对评测题的过拟合。
  - [置信度注入揭示自监控失效](#item-28)：注入反事实置信度后发现模型能按疑虑重做，却不能可靠发现自身错误，定位了自我纠错的检测瓶颈。
  - [RAP](#rap)：先测量候选模型是否真的各有所长，再训练路由器，避免把偶然选对模型误判为可泛化的路由能力。
- **数据与训练**
  - [AutoSFT](#autosft)：让执行、分析和合成智能体协作筛选、修复与生成微调数据，突破单智能体只能调整样本比例的限制。
  - [SAEPO](#saepo)：用稀疏自编码器把最终成败拆成逐词奖惩，无需过程标注即可改善长推理的信用分配。
  - [Kolpona](#kolpona)：定位并闭式编辑少数失败相关神经元，再用仿真筛选改动，无需训练便将RTL代码通过率提升至94.9%。
- **长程状态**
  - [Stable Gated DeltaNet-2](#stable-gated-deltanet-2)：用对称擦除和受控写入限制循环状态放大，解决线性注意力处理长文本时状态爆炸的问题。
  - [定向监督激活线性注意力召回](#item-23)：用句子重复和上下文加权训练，激活线性注意力原本存在但常规训练未利用的远距离召回能力。
  - [BiDE-Mem](#bide-mem)：按问题所需的证据类型组织可追溯记忆，解决“检索内容相关却不足以回答”的问题，LongMemEval达91.80%。
- **接口与安全**
  - [RUIBench](#ruibench)：统一比较机器人动作接口，证明仅更换交互形式就能把智能体成功率从45%提高到81%。
  - [Conartist](#conartist)：根据安全审计反馈自适应调整两阶段提示注入，揭示防护流程本身也可能被利用，攻击成功率最高66.67%。
- **程序化视觉**
  - [Solve Vision with Code](#solve-vision-with-code)：让编码智能体编程计算并渲染答案视频，以可检查程序替代不稳定的直接像素生成，最高得分0.923。
- **热点延伸**：[ProxyGenBench](#proxygenbench)、[StateWeaver](#stateweaver)、[Boundary-Aware Policy Learning](#boundary-aware-policy-learning)、[JudiAct](#judiact)

## 对当前研究的启发
- **AgentEvolve**
  - 迁移｜从 [CoEvo-RSI](#coevo-rsi) 把历史模型与脚手架重配用于版本迭代：存档每版配置与得分，跨代搜索最佳组合。
  - 迁移｜从 [MetaSkill](#metaskill) 把抽象解题方法用于技能库编排：先选方法再排技能，失败后分别重选方法或修复流程。
- **Awesome-RSI**
  - 迁移｜从 [RSI 2026](#rsi-2026) 把独立验证用于自改进验收：固定算力，对比改进前后留出集、跨任务收益和能力保持率。
  - 延续｜[置信度注入揭示自监控失效](#item-28) 留下错误检测瓶颈：对比自报与外部置信信号，统计发现率、修复率和误改率。
- **DataEvolve**
  - 迁移｜从 [AutoSFT](#autosft) 把多角色数据动作用于数据飞轮：按失败类型执行筛选、修复、重标和合成，并记录单动作增益。
- **CacheEvolve**
  - 迁移｜从 [Stable Gated DeltaNet-2](#stable-gated-deltanet-2) 把非扩张状态更新用于循环缓存：约束状态增益并监测长序列范数与召回率。
  - 迁移｜从 [定向监督激活线性注意力召回](#item-23) 把重复句与加权损失用于长程训练：按距离分桶测复制和关联检索准确率。
- **HarnessEvolve**
  - 延续｜[RUIBench](#ruibench) 留下任务级执行验证缺口：加入多步终态检查，对比自报成功与真实成功，统计偏差和恢复率。
- **EvalEvolve**
  - 延续｜[RAP](#rap) 留下无法预审新模型组合的问题：逐批加入候选模型，以预测增益对比实测增益，报告相关性和误报率。
- **EvolveLRM**
  - 迁移｜从 [SAEPO](#saepo) 把语义概念级信用用于结果奖励训练：接入GRPO，对比原始奖励的样本效率与分布外准确率。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-28/  

