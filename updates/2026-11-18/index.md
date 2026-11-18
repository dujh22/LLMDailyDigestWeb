# 2026-11-18 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **快速决策**
  - [JevRSI](#jevrsi)：把耗时推理异步沉淀为可复用脚手架，避免智能体每次决策都重复慢思考。
  - [Karpo Decision](#karpo-decision)：一次并行评估所有候选动作，取代逐词生成，将31B模型决策延迟压至94毫秒。
- **训练验证**
  - [Axion 1.0](#axion-1-0-sft)：先分阶段教授检索与解题，再按可验证进度强化，简化科学智能体训练并在HLE达到59.0%。
  - [Optimistic Verifiers](#optimistic-verifiers)：用可执行规则充当精确裁判，定位会把错误行为误判为正确、进而诱发奖励作弊的验证器缺口。
  - [RepoFactory](#repofactory)：用可执行性、依赖强度和实现规模反馈自动改造代码仓库，批量生成长程编码训练环境。
- **系统自改进**
  - [自我改进分支混合](#item-5)：让搜索分支形成不同目标与经验，再按任务路由组合，缓解脚手架优化陷入单一路径。
  - [Self-Rewriting](#self-rewriting)：让27B模型自测后直接编辑自身权重，无需梯度训练便在未见题上提升6.6个百分点。
  - [DCPS](#dcps)：固定候选生成器后只搜索示例，证明复杂提示优化的部分收益其实来自多采样与筛选。
- **科研闭环**
  - [MatOS](#matos)：把实验步骤、证据和科研资产组织成可追溯图谱，使长程材料研究能纠偏并复用经验。
  - [SciWorkBench](#sciworkbench)：用四学科真实工作流统一评测科研智能体，揭示最佳系统平均得分仅57.38。
- **记忆可靠性**
  - [Remembered as Brief](#remembered-as-brief)：仅改变用户偏好记忆便测出关键警告被静默省略，最高96%的遗漏没有提示。
  - [BRIDGE](#bridge)：以极简检索作为强基线，再用对抗问题暴露“记得规则却不执行”的记忆缺口。
  - [Experience Rot](#experience-rot)：静默修改工具接口后，智能体会盲目复用旧经验，积累经验反而增加失败。
- **推理成本**
  - [Context Has a Price](#context-has-a-price)：把缓存价格和上下文变化引发的后续行为一起计费，证明提示更短未必让代码修复更便宜。
  - [Lost in a Few Heads](#lost-in-a-few-heads)：定位并单独修复少数检索失灵的注意力头，使64K多键检索准确率从54.1%升至97.5%。
- **热点延伸**：[AllocFlow](#allocflow)、[InclusionMed](#inclusionmed)、[SPILLWAY](#spillway)

## 对当前研究的启发
- **AgentTrainEvolve**
  - 迁移｜从 [Axion 1.0](#axion-1-0-sft) 把“两阶段SFT+阶段奖励”用到工具训练：先教证据检索，再按阶段结果做GRPO
  - 延续｜[Optimistic Verifiers](#optimistic-verifiers) 留下奖励作弊损害不稳定：跑5个随机种子，对比缺口方向、作弊率与任务收益
- **MemoryEvolve**
  - 迁移｜从 [BRIDGE](#bridge) 把“检索到但未执行”用到记忆评测：构造间接提问，分别统计召回率与规则执行率
  - 延续｜[Experience Rot](#experience-rot) 留下旧经验失效难题：静默变更工具版本，对比版本标记、自动作废与重验证
- **SystemEvolve**
  - 迁移｜从 [JevRSI](#jevrsi) 把异步慢推理用到在线决策：离线修订脚手架，线上只检索并执行已验证模块
  - 延续｜[自我改进分支混合](#item-5) 留下路由收益不稳定：扫描上下文和更新频率，报告质量、时延及搜索Token
- **ResearchEvolve**
  - 迁移｜从 [MatOS](#matos) 把证据资产图用到科研循环：每轮绑定假设、代码、结果、审查结论与复用条件
  - 延续｜[SciWorkBench](#sciworkbench) 留下流程化与跨模态纠错不足：分项移除工具反馈，评测流程完成率和纠错率
- **Groom**
  - 迁移｜从 [Context Has a Price](#context-has-a-price) 把缓存计费纳入Token归因：同时记录输入价格、后续轮数与总任务成本
- **Awesome-RSI**
  - 延续｜[Self-Rewriting](#self-rewriting) 留下小模型自损门槛：统一测试2B至27B，比较能力增益、回归率与编辑保留率

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-18/  

