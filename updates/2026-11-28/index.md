# 2026-11-28 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **自进化方法**
  - [CoEvo-RSI](#coevo-rsi)：跨代保存并重组模型与执行脚手架，避免独立升级造成接口错配，使9B模型在垂直任务上超过更大模型。
  - [RSI 2026](#rsi-2026)：用自主性分级、独立留出集和轨迹审计，区分真正跨任务提升与自我修改后的过拟合。
  - [AutoSFT](#autosft)：让执行、分析和合成智能体协作筛选、修复及生成微调数据，突破单智能体只能调整样本比例的限制。
- **可审计推理**
  - [Solve Vision with Code](#solve-vision-with-code)：让编码智能体编程渲染答案视频，以可检查程序替代不稳定的直接像素生成，最高得分0.923。
  - [DAPO-V](#dapo-v)：把“错误是否容易被人发现”设为强化学习风险预算，避免准确率提升掩盖更隐蔽的多模态幻觉。
  - [置信度注入揭示自监控失效](#item-28)：注入反事实置信度令牌分离错误检测与修复，发现模型能按疑虑重思，却不能可靠发现自身错误。
  - [VeriLogic](#verilogic)：把中间判断和证明转成可形式检查的训练对象，定位并修复最终答案正确率无法暴露的错误推理。
- **长程状态**
  - [Stable Gated DeltaNet-2](#stable-gated-deltanet-2)：用对称擦除和受控写入约束循环状态增益，防止线性注意力在长上下文中数值爆炸。
  - [BiDE-Mem](#bide-mem)：按问题所需证据类型组织可溯源记忆，解决检索结果相关却不足以完整作答的问题，LongMemEval达91.80%。
- **具身系统**
  - [Motubrain 2.0](#motubrain-2-0)：以统一动作表征连接20B世界动作模型和反馈式脚手架，让机器人跨本体复用视频经验并从执行失败中恢复。
  - [RUIBench](#ruibench)：统一比较机器人动作接口，证明仅改变动作表达和反馈方式即可把执行成功率从45%提高到81%。
  - [sft-JEPA](#sft-jepa)：按误差持续时间分别进行回合内快速适应和跨回合慢速学习，使世界模型规划成功率最高提升22点。
- **评测审计**
  - [RAP](#rap)：先从候选模型得分矩阵判断基准是否存在路由空间，避免把偶然选中强模型误报为路由能力。
- **代码优化**
  - [Kolpona](#kolpona)：用闭式神经元编辑和仿真测试筛选替代训练，将27B模型的VerilogEval v2通过率提升至94.9%。
- **环境合成**
  - [GREMLIN](#gremlin)：用随机参数化神经环境生成训练经验，摆脱人工游戏设计，并让学习规则在26款游戏上超过未训练教师。
- **热点延伸**：[ProxyGenBench](#proxygenbench)、[StateWeaver](#stateweaver)、[Boundary-Aware Policy Learning](#boundary-aware-policy-learning)、[JudiAct](#judiact)

## 对当前研究的启发
- **AgentEvolve**
  - 迁移｜从 [CoEvo-RSI](#coevo-rsi) 把跨代版本重组用于脚手架迭代：保留模型与Harness快照，交叉配对后按任务分和接口失败率筛选。
- **DataEvolve**
  - 迁移｜从 [AutoSFT](#autosft) 把六类数据动作用于SFT数据闭环：按失败类型自动筛选、修复、重标和合成样本，再逐轮消融。
  - 延续｜[AutoSFT](#autosft) 尚未验证跨训练器和预算泛化：更换模型、训练器与预算，对比能力增益、耗时和API成本。
- **Awesome-RSI**
  - 迁移｜从 [RSI 2026](#rsi-2026) 把独立留出集和等算力审计用于RSI验收：逐轮测跨任务增益、能力保持率与轨迹违规率。
- **MonitorEvolve**
  - 迁移｜从 [DAPO-V](#dapo-v) 把可验证性风险预算用于安全训练：按人类漏检率自适应惩罚难核验错误，并与纯准确率奖励对比。
- **CacheEvolve**
  - 迁移｜从 [Stable Gated DeltaNet-2](#stable-gated-deltanet-2) 把非扩张状态更新用于循环缓存：监测状态范数、长程召回率和分块训练吞吐。
- **EvalEvolve**
  - 迁移｜从 [RAP](#rap) 把可路由性审计用于模型路由评测：先计算模型互补度和并列最优率，再报告路由器相对神谕的差距。
  - 延续｜[RUIBench](#ruibench) 缺少任务级验证：增加环境终态检查器，对比智能体自报与真实成功并统计误报率。
- **MemoryEvolve**
  - 迁移｜从 [BiDE-Mem](#bide-mem) 把类型化需求用于记忆检索：先拆出人物、时间和因果约束，再测证据覆盖率与答案准确率。
- **LogicEvolve**
  - 迁移｜从 [VeriLogic](#verilogic) 把可验证中间状态用于逻辑RL：逐步调用求解器打分，对比仅用最终答案奖励的正确率与修复率。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-28/  

