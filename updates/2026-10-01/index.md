# 2026-10-01 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **智能体平台走向全天候运行与模块化基础设施**：OpenAI 发布全天候智能体及 Agents API 等平台能力（[OpenAI DevDay聚焦全天候智能体与开发者平台](#openai-devday)），DeepSeek 则公开大规模训练与评测沙盒 [DSec](#deepseek-v4-1-agent-dsec)，[Omni-IO Skills：让智能体原生支持全模态任务](#omni-io-skills)进一步以分层技能和统一接口扩展全模态执行。
- **具身与空间智能聚焦部署时泛化**：从[机器人上下文学习：方法与应用综述](#item-4)总结的免更新适应范式，到 [Simple-WAM：测试时未来建模提升世界动作模型泛化](#simple-wam)对高效未来表征的提炼，再到 [LEGO-Anything：以编程智能体重建可执行 3D 场景](#lego-anything-3d)将视觉理解转化为可执行、可编辑的场景程序。
- **后训练研究推进高效能力迁移与精细奖励**：两项在策略蒸馏工作分别揭示小专家促使大学生超越教师的缩放现象（[同系列在策略蒸馏的缩放特性](#item-5)），以及以最大耦合动态路由词元监督的高吞吐方案（[SAKI：最大耦合路由教师监督的在策略蒸馏](#saki)）；[Think Before You Score：用于视觉生成的思考型奖励模型](#think-before-you-score)则引入样例自适应评分标准以改善视觉偏好优化。
- **长上下文评测暴露模态记忆与压缩可靠性短板**：[VoxMem：大型音频语言模型多模态记忆评测基准](#voxmem)显示现有模型在 32K 跨会话音频记忆上仍不足 40%，而[分块 KV 缓存压缩存在周期性相位弱点](#item-10)发现仅窗口相位变化即可造成最高 40 个百分点的检索差异。

## 对当前研究的启发
- **EnvironmentEvolve**：[DeepSeek公开V4.1 Agent训练沙盒基础设施DSec](#deepseek-v4-1-agent-dsec)提供了环境即服务的具体工程参照，可将弹性供给、状态持久化、资源超卖和安全隔离纳入自进化环境基础设施设计。
- **HarnessEvolve**：[Omni-IO Skills：让智能体原生支持全模态任务](#omni-io-skills)表明可通过统一执行接口、依赖感知编排和持久化资产注册，在不改模型核心的前提下演进 harness 的模态与技能覆盖。
- **MemoryEvolve**：[VoxMem：大型音频语言模型多模态记忆评测基准](#voxmem)可为跨会话长期记忆增加语义、说话人、辅助语言线索和环境声音四类可分解评测维度。
- **EvalEvolve**：[分块 KV 缓存压缩存在周期性相位弱点](#item-10)说明长上下文评测应动态扰动窗口相位与目标位置，避免固定布局掩盖压缩系统的周期性失效。
- **EvolveLRM**：[同系列在策略蒸馏的缩放特性](#item-5)与 [SAKI：最大耦合路由教师监督的在策略蒸馏](#saki)提示可把小型 RL 专家、轨迹分布保持和词元级动态纠错结合起来，降低推理模型持续后训练的采样与监督成本。

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-10-01/  

