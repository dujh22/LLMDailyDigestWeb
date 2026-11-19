# 2026-11-19 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **智能体进化**
  - [SEED](#seed)：把成功轨迹提炼成持续更新的技能，为长程智能体提供比最终成败更细的训练信号。
  - [认知共生体](#item-1)：将用户关系与记忆保存在模型之外，使个人智能体更换设备或模型后仍能延续。
  - [VideoNexus](#videonexus)：让独立感知智能体把长视频压成带时间定位的证据，避免细节挤占规划上下文。
- **模型架构**
  - [MBT](#mbt)：用并行计算分支共享注意力缓存，同时提高语言建模质量并降低长文本解码成本。
  - [权重空间编程](#transformer)：用可读可改的稀疏事实表承载大模型直接编写的权重，参数减少约1800倍。
- **具身智能**
  - [ForceHarness](#forceharness)：把高频力觉反馈封装成自主闭环动作，使冻结模型的真机接触操作成功率从3.3%升至90.0%。
  - [TCP4D](#tcp4d-tcp)：以机器人末端工具为统一坐标，从普通视频恢复动作并跨机器人生成训练示范。
  - [Heave-Ho](#heave-ho)：用局部控制与语音口令同步，让无网络连接的人形机器人团队从2台扩展到10台。
- **热点延伸**：[FastFrames](#fastframes)、[π⁴](#item-10)、[Breath-Dx](#breath-dx)

## 对当前研究的启发
- **AgentTrainEvolve**
  - 迁移｜从 [SEED](#seed) 把轨迹后验技能用到长程工具调用训练：按步骤重打分，与仅用终局奖励比较成功率和收敛速度。
- **PersonalEvolve**
  - 迁移｜从 [认知共生体](#item-1) 把模型外关系层用到个人画像：跨模型复用同一记忆库，测试偏好保持率与错误记忆率。
  - 延续｜[认知共生体](#item-1) 留下谄媚和思想数据泄露风险：加入防篡改日志，对比不同权限等级的操纵率与泄露率。
- **CacheEvolve**
  - 迁移｜从 [MBT](#mbt) 把跨分支共享KV用到固定预算缓存：对比独立缓存的显存、吞吐和长文本困惑度。
  - 迁移｜从 [VideoNexus](#videonexus) 把带时间定位的证据压缩用于智能体上下文：测压缩率、答案准确率和证据召回率。
- **PhysicalEvolve**
  - 迁移｜从 [ForceHarness](#forceharness) 把高频反馈下沉为自治原语：让冻结模型只接收物理摘要，测成功率、时延和过载次数。
- **RobotEvolve**
  - 迁移｜从 [TCP4D](#tcp4d-tcp) 把工具中心点作为跨本体接口：由单目视频合成示范，对比同本体数据量和迁移成功率。
- **SwarmEvolve**
  - 迁移｜从 [Heave-Ho](#heave-ho) 把语音领从同步用于无网络协作：从2台扩至10台，测完成率、失同步次数和规模退化。
- **NewModel**
  - 延续｜[权重空间编程](#transformer) 尚未超过预训练模型：在生成任务中对比稀疏表与小型Transformer的准确率、参数量和可编辑性。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-19/  

