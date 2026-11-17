# 2026-11-17 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **系统自进化**
  - [HarnessDev](#harnessdev)：让智能体从种子框架自行创建并迭代执行系统，再用跨模型和未见任务测试揭示反馈优化造成的过拟合。
  - [RiseHarness](#riseharness)：对照成功与失败轨迹诊断执行流程，无需更新模型即可提高长程终端任务的重复成功率。
  - [HARNESS-ZERO](#harness-zero)：用审核智能体把专用执行规则改写成训练轨迹，移除脚手架后成功率仍从23.3%升至44.3%。
  - [Harness-of-Harness](#harness-of-harness)：以规划、开发、独立验收和版本证据闭环约束持续编码，三轮平均相对提升52.25%。
- **经验进化**
  - [SkillMaster](#skillmaster)：把技能创建、修订和保留纳入策略，并按其对后续任务的实际帮助训练可持续进化的技能库。
  - [DeLoop](#deloop)：从重复调用后的自发恢复动作自动构造偏好数据，让长程智能体学会停止空转而无需人工标注。
  - [MEM-SQL](#mem-sql)：分层保存并按需组合已验证查询，使文本转SQL复用历史证据，执行准确率从37.1%升至50.0%。
- **持续自治**
  - [持续在线个人智能](#item-1)：用感知、记忆、行动闭环及分级审查，让个人助手跨请求保持状态并安全修改自身行为。
- **模型与部署**
  - [Qwen4-Max](#qwen4-max)：以按需激活部分参数和压缩上下文降低长程编程、办公及多模态任务的实际调用成本。
  - [Mobile AI Factory](#mobile-ai-factory)：让智能体依据真机测量自动微调和量化端侧模型，配置搜索耗时降至穷举的1/19。
- **具身与空间**
  - [Agentic Robotics](#agentic-robotics)：用基础模型、具身执行层和双层评测统一开放世界机器人的闭环决策与安全验收。
  - [VibePrevisBench](#vibeprevisbench)：以242项任务分别检查场景代码事实和最终画面可见性，定位四维场景编程的真实失败原因。
- **热点延伸**：[Gamer](#gamer)、[DySENSE](#dysense)

## 对当前研究的启发
- **HarnessEvolve**
  - 迁移｜从 [HarnessDev](#harnessdev) 把“创建—迭代—未见任务测试”用于框架验收：跨模型复跑并报告迁移跌幅
  - 迁移｜从 [RiseHarness](#riseharness) 把成败双轨迹用于版本诊断：提取差异、生成修改并以重复成功率决定采纳
- **AgentEvolve**
  - 迁移｜从 [SkillMaster](#skillmaster) 把反事实技能效用用于技能淘汰：屏蔽候选技能，按后续任务收益决定保留
  - 延续｜[MEM-SQL](#mem-sql) 留下多条记忆组合准确率骤降：对比单条与多条复用的准确率、延迟和访问量
- **AutonomousAgentEvolve**
  - 迁移｜从 [持续在线个人智能](#item-1) 把感知—记忆—行动闭环用于唤醒周期：逐轮记录事件、状态、动作和审查结果
  - 延续｜[持续在线个人智能](#item-1) 留下长期记忆纠错与修改撤回问题：注入冲突记忆，测检出率和回滚成功率
- **AgentTrainEvolve**
  - 迁移｜从 [DeLoop](#deloop) 把“重复动作—恢复动作”用于DPO数据构造：比较循环率、成功率和交互步数
  - 延续｜[HARNESS-ZERO](#harness-zero) 留下强审核模型依赖和2.4倍延迟：对比逐轮、批量与终局审核的成本和成功率
- **CodeEvolve**
  - 迁移｜从 [Harness-of-Harness](#harness-of-harness) 把独立验收和版本证据用于持续开发：每轮回归并阻断无证据改动
- **InfraEvolve**
  - 迁移｜从 [Mobile AI Factory](#mobile-ai-factory) 把真机测量用于配置搜索：联合优化准确率、峰值内存和端到端延迟

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-17/  

