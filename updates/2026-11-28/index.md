# 2026-11-28 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **协同进化**
  - [CoEvo-RSI](#coevo-rsi)：跨代保留并重组模型与执行框架，避免各自升级后的接口错配，使9B模型在垂直任务上超过大型模型。
  - [RSI 2026](#rsi-2026)：用自主性分级、独立留出集和轨迹审计，区分真正跨任务提升与自我修改后的过拟合。
  - [AutoSFT](#autosft)：让执行、分析和合成智能体共同筛选、修复与生成微调数据，突破单智能体只能调整样本比例的限制。
  - [Kolpona](#kolpona)：直接编辑少数神经元并用仿真测试筛选结果，无需训练便将27B模型的RTL代码通过率提升至94.9%。

- **架构与记忆**
  - [Stable Gated DeltaNet-2](#stable-gated-deltanet-2)：用对称擦除约束循环状态的方向增益，避免线性注意力处理长文本时数值爆炸。
  - [定向监督激活线性注意力召回](#item-23)：用句子重复和重点加权训练，唤醒线性注意力在常规训练中未形成的远距离检索能力。
  - [BiDE-Mem](#bide-mem)：先拆出问题需要的证据类型再组织检索结果，解决记录相关却不足以完整作答的问题。

- **评测与接口**
  - [RAP](#rap)：先检查候选模型是否真正各有所长，再评测路由器，避免把偶然选对模型误判为普遍路由增益。
  - [置信度注入揭示自监控失效](#item-28)：用人为置信度信号分离发现错误与修复错误，证明模型能受疑虑驱动重想，却不会可靠识别自身错误。
  - [RUIBench](#ruibench)：统一比较机器人动作接口，发现仅改变动作表达与反馈方式就能把任务成功率从45%提高到81%。
  - [Memphis](#memphis)：从真实执行失败反向生成仿真任务，使评测复现现实决策瓶颈，而非只靠扩充人工题库。

- **安全约束**
  - [FORK](#fork)：让防护栏与自适应攻击者共同演化，同时优化拦截决策和拒绝措辞，避免泄露可用于绕过防线的线索。
  - [DAPO-V](#dapo-v)：把“错误是否容易被人发现”设为强化学习的独立风险预算，减少准确率提升后转为隐蔽幻觉的问题。

- **具身与视觉**
  - [Motubrain 2.0](#motubrain-2-0)：用统一动作表示连接视频经验、不同机器人本体和执行反馈，让20B模型能迁移经验并在失败后调整任务。
  - [Solve Vision with Code](#solve-vision-with-code)：让编码智能体写程序渲染答案视频，以可检查计算替代不稳定的逐像素生成，最高得分0.923。

- **热点延伸**：[ProxyGenBench](#proxygenbench)、[StateWeaver](#stateweaver)、[Boundary-Aware Policy Learning](#boundary-aware-policy-learning)、[JudiAct](#judiact)

## 对当前研究的启发
- **AgentEvolve**
  - 延续｜[CoEvo-RSI](#coevo-rsi) 尚未验证开放环境泛化：跨网页、数据库和桌面任务交换模型与脚手架，比较原配与重组成功率。

- **Awesome-RSI**
  - 迁移｜从 [RSI 2026](#rsi-2026) 把独立留出集与等计算预算用于每轮自改验证：同时报告新任务增益和原能力保持率。
  - 迁移｜从 [置信度注入揭示自监控失效](#item-28) 把检错与纠错拆开评测：注入真假疑虑信号，分别统计错误发现率和修复率。

- **DataEvolve**
  - 延续｜[AutoSFT](#autosft) 固定了训练器、模型和预算：做三因素交叉实验，以能力增益、零分任务数和API成本评价稳健性。

- **CacheEvolve**
  - 迁移｜从 [Stable Gated DeltaNet-2](#stable-gated-deltanet-2) 把非扩张约束用于循环缓存更新：监测长序列状态范数、召回率与吞吐。
  - 迁移｜从 [定向监督激活线性注意力召回](#item-23) 把句子重复训练用于固定预算记忆：对比常规训练的远距召回率和状态容量。

- **EvalEvolve**
  - 迁移｜从 [RAP](#rap) 把可路由性审计放到路由评测前：计算候选互补度、并列最优率及路由相对单模型的净增益。
  - 延续｜[Memphis](#memphis) 仅验证单个制造任务：从三类真实失败轨迹生成仿真题，比较人工题库与轨迹题的失效检出率。

- **MemoryEvolve**
  - 迁移｜从 [BiDE-Mem](#bide-mem) 把问题需求类型用于检索前规划：逐类检查证据覆盖率，再测多跳答案准确率与溯源率。

- **HarnessEvolve**
  - 延续｜[RUIBench](#ruibench) 缺少任务级验证：为动作轨迹增加环境终态检查，对比智能体自报成功率与真实完成率。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-28/  

