# 2026-11-24 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归改进**
  - [MetaRSI/RSI²](#metarsi-rsi)：让数据、执行框架和模型共同演化，并以不可改写的验证边界防止自改进规则固化或失控。
  - [RSI](#rsi)：用“优化任务—优化改进器”双循环解释固定改进流程为何触顶，并把持续进步转化为评估可靠性问题。
- **执行系统**
  - [HarnessDev](#harnessdev)：把评测拆成“自主搭建执行框架”和“实际运行”，测出模型管理循环、工具与错误恢复的真实能力。
  - [HoH](#hoh)：以规划、开发、测试三智能体分别维护代码事实与任务决策，使编码代理连续运行数天仍不丢进度。
  - [SKILL.state](#skill-state)：用可执行的结构化状态替代不断增长的对话历史，同时降低长程任务延迟并支持故障恢复。
  - [Duopra](#duopra)：统一后台委派与直接工具调用并联合训练对话和执行，使全双工任务成功率从4.7%升至44.7%。
- **模型与推理**
  - [Declarative Attention](#declarative-attention)：让模型在每步思考时声明需要查看的上下文范围，避免反复扫描全部缓存。
  - [GLM-5.4](#glm-5-4)：以权重共享循环层增加推理深度，并用分层缓存避免计算轮数带动部署成本等比例增长。
  - [MIM](#mim)：先用代数变换消除密码攻击中的干扰变量，再生成可执行代码，将多类攻击从小时压缩到秒级。
- **科研闭环**
  - [AI生物学](#item-4)：用模型、工具、湿实验和数据回流四层框架定位研发瓶颈，揭示强模型时代实验能力反而更稀缺。
- **物理智能**
  - [NoPeWorld](#nopeworld)：直接从视频模型隐状态识别并替换穿墙动作，把物理违规率从74%降至16%。
  - [ReSpaceBench](#respacebench)：显式标注房间重访与环境变化，检验智能体能否长期辨认同一地点并更新空间记忆。
  - [AgentRoboCritic](#agentrobocritic)：把机器人轨迹逐动作对齐局部意图，定位仅看最终成败无法发现的执行与恢复故障。
- **热点延伸**：[Future-OPSD](#future-opsd)、[RTC](#rtc)、[StereoVLM](#stereovlm)、[Uni3Sim](#uni3sim)、[PURE](#pure)

## 对当前研究的启发
- **Awesome-RSI**
  - 迁移｜从 [MetaRSI/RSI²](#metarsi-rsi) 把双轴调度用于RSI编排：独立变异数据、框架和模型，过期工件强制复评
  - 延续｜[RSI](#rsi) 留下评估噪声会筛错改进器：设置多评委复核，统计长期增益、退化率与回滚率
- **HarnessEvolve**
  - 迁移｜从 [HarnessDev](#harnessdev) 把“先搭框架再运行”用于模型评测：比较固定与自建框架的成功率、耗时和恢复率
- **CacheEvolve**
  - 迁移｜从 [Declarative Attention](#declarative-attention) 把三档注意力范围用于缓存管理：训练范围标记并测显存、延迟和准确率
- **AutonomousAgentEvolve**
  - 迁移｜从 [HoH](#hoh) 把代码事实与任务决策双状态用于常驻运行：分别持久化并做跨日中断恢复测试
- **MemoryEvolve**
  - 迁移｜从 [SKILL.state](#skill-state) 把规则、状态、观察分离用于长期记忆：故障后重放并检查状态一致率
- **ResearchEvolve**
  - 迁移｜从 [AI生物学](#item-4) 把湿实验回流接入科研闭环：记录假设到验证的周期、命中率与新增数据价值
- **PhysicalEvolve**
  - 迁移｜从 [NoPeWorld](#nopeworld) 把隐状态安全预测头用于动作拦截：比较干预前后的违规率与任务成功率
  - 延续｜[AgentRoboCritic](#agentrobocritic) 留下抓取对齐和恢复不稳：按失败类型测试真机恢复率、步数与损伤
- **AgentTrainEvolve**
  - 迁移｜从 [Duopra](#duopra) 把委派纳入工具动作训练：联合优化对话控制，测任务成功率与纠错响应延迟

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-24/  

