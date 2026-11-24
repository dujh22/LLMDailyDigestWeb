# 2026-11-24 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **递归改进**
  - [MetaRSI/RSI²](#metarsi-rsi)：用可演化的双轴调度同时改进数据、执行框架和模型，并以隔离验证与状态刷新防止自改进失控。
  - [RSI](#rsi)：用双循环把“改进方法本身”纳入反馈，解释固定优化流程为何封顶及可靠评估为何决定长期进步。
- **执行系统**
  - [HarnessDev](#harnessdev)：让模型先自主搭建执行框架再完成任务，联合检验循环管理、工具调用和错误恢复能力。
  - [HoH](#hoh)：以规划、开发、测试三智能体和双状态存储维持多日编码进度，最高性能达82.86%。
  - [SKILL.state](#skill-state)：用规则、状态和观察组成的可执行状态替代不断增长的对话，降低长任务延迟并支持故障恢复。
  - [Duopra](#duopra)：把后端委派与直接工具调用统一成可训练动作，使智能体边对话边执行时的成功率由4.7%升至44.7%。
- **模型与推理**
  - [Declarative Attention](#declarative-attention)：让模型在每步思考时声明需要查看的上下文范围，避免扫描全部缓存造成显存和延迟浪费。
  - [GLM-5.4](#glm-5-4)：用权重共享循环层增加推理深度，并以分层缓存控制循环计算成本，同时支持视觉操控专业软件。
- **科学闭环**
  - [MIM](#mim)：用代数变换消除密码攻击中的干扰项并自动生成代码，将多类攻击由小时级压缩至秒级。
  - [AI生物学](#item-4)：用模型、工具、湿实验和数据回流四层框架定位AI生物研发瓶颈，指出独有实验数据将比模型更稀缺。
- **具身智能**
  - [NoPeWorld](#nopeworld)：读取视频世界模型已有的隐藏状态，在执行前替换穿墙动作，将物理违规率从74%降至16%。
  - [ReSpaceBench](#respacebench)：显式标注房间重访和环境变化，检验智能体能否跨多次访问辨认地点并更新空间记忆。
- **热点延伸**：[Future-OPSD](#future-opsd)、[RTC](#rtc)、[StereoVLM](#stereovlm)

## 对当前研究的启发
- **Awesome-RSI**
  - 迁移｜从 [MetaRSI/RSI²](#metarsi-rsi) 把工件新鲜度合约用于RSI调度：每轮拒绝过期状态，并隔离候选算子与裁判。
  - 延续｜[RSI](#rsi) 留下评估噪声会筛错算子：注入分级噪声，对比单裁判与多裁判，测长期能力斜率和退化率。
- **HarnessEvolve**
  - 迁移｜从 [HarnessDev](#harnessdev) 把“先造框架、再执行”用于评测：统一任务环境，比较成功率、恢复率与配置复现率。
- **Groom**
  - 迁移｜从 [HarnessDev](#harnessdev) 把两阶段测试用于token归因：分开统计框架构建与运行，再细分规划、工具和恢复。
- **CacheEvolve**
  - 迁移｜从 [Declarative Attention](#declarative-attention) 把三档注意力声明用于缓存控制：训练逐步选档，测显存、延迟与准确率。
- **AutonomousAgentEvolve**
  - 迁移｜从 [HoH](#hoh) 把代码事实与任务决策分开持久化：每次运行后双通道存档，注入重启并测进度恢复率。
- **MemoryEvolve**
  - 迁移｜从 [SKILL.state](#skill-state) 把规则、状态、观察分离用于长期记忆：对比完整对话，测延迟、正确率与故障恢复率。
- **PhysicalEvolve**
  - 迁移｜从 [NoPeWorld](#nopeworld) 把隐状态安全预测头用于动作执行前检查：对比事后纠错，测违规率、误拦率和任务成功率。
- **AgentTrainEvolve**
  - 迁移｜从 [Duopra](#duopra) 把委派与直接调用统一为动作空间：联合训练对话控制和工具执行，测纠正响应与任务成功率。
- **ResearchEvolve**
  - 迁移｜从 [AI生物学](#item-4) 把实验数据回流用于科研闭环：串联模型、工具与湿实验，以命中率和迭代周期验收。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-24/  

