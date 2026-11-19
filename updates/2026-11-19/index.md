# 2026-11-19 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **智能体进化**
  - [SEED](#seed)：从当前策略的成功轨迹提炼可更新技能，为长程智能体补上稀疏成败奖励无法提供的逐步监督。
  - [认知共生体](#item-1)：把用户关系与长期记忆存到模型之外，使个人智能体跨设备、换模型后仍能延续服务。
- **模型架构**
  - [MBT](#mbt)：以并行 Transformer 分支共享注意力缓存，同时提高语言建模质量并降低长文本生成成本。
  - [权重空间编程](#transformer)：让大模型编写可读可改的稀疏事实表而非 Transformer 权重，以约 1/1800 参数取得更高准确率。
- **具身协作**
  - [ForceHarness](#forceharness)：把高频力觉反馈封装成自主闭环动作，使冻结多模态模型的真机接触操作成功率从 3.3% 升至 90.0%。
  - [TCP4D](#tcp4d-tcp)：用统一四维场景表示从普通视频恢复工具运动，并将动作示范迁移到不同机器人。
  - [Heave-Ho](#heave-ho)：结合局部观测控制与语音同步，让无网络的人形机器人团队完成长时全身协作并扩展至 10 台。
- **证据压缩**
  - [VideoNexus](#videonexus)：让独立感知智能体只回传带时间位置的关键视频证据，避免长视频细节挤占规划上下文。
- **热点延伸**：[FastFrames](#fastframes)、[π⁴](#item-10)

## 对当前研究的启发
- **AgentTrainEvolve**
  - 迁移｜从 [SEED](#seed) 把“轨迹后技能重打分”用于长程工具调用训练：对比结果奖励与混合奖励的成功率、信用分配和样本效率。
- **CacheEvolve**
  - 迁移｜从 [MBT](#mbt) 把跨分支共享 KV 用到固定缓存预算：扫描分支数与上下文长度，测困惑度、显存和解码吞吐。
  - 迁移｜从 [VideoNexus](#videonexus) 把带时间戳的证据包用于视频缓存压缩：固定 token 预算，对比均匀采样的准确率与成本。
- **PhysicalEvolve**
  - 迁移｜从 [ForceHarness](#forceharness) 把自终止力控原语用于冻结 VLM 控制：在插接和擦拭任务测成功率、峰值力与调用次数。
- **RobotEvolve**
  - 迁移｜从 [TCP4D](#tcp4d-tcp) 把工具中心点作为跨本体动作接口：用同一视频训练两类机械臂，测零样本迁移成功率。
- **SwarmEvolve**
  - 迁移｜从 [Heave-Ho](#heave-ho) 把语音领从同步用于断网协作：比较语音、无线通信和无同步在 2—10 台机器人上的完成率与延迟。
- **MemoryEvolve**
  - 延续｜[认知共生体](#item-1) 留下虚假记忆与关系操纵风险：注入冲突记忆，对比审计日志前后的误写率、纠错率和谄媚率。
- **NewModel**
  - 延续｜[权重空间编程](#transformer) 尚未胜过预训练大模型：在分类与生成任务对比稀疏表、同参数 Transformer 和预训练模型的精度与编辑成本。
- **Groom**
  - 迁移｜从 [VideoNexus](#videonexus) 把“单位证据 token 的答案贡献”用于过程评测：逐项删减证据，统计准确率下降与 token 节省。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-19/  

