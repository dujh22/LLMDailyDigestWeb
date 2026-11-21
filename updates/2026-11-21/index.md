# 2026-11-21 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **在线适应**
  - [Forward-Only Passes](#forward-only-passes)：仅凭前向激活的方向集中度筛除低价值权重成分，让模型无需反向传播即可低成本适应在线任务。
- **具身闭环**
  - [TuringSpace](#turingspace)：用程序化交互验证码把空间判断绑定到点击、拖拽和纠错，使微调后任务成功率从1.6%升至33.1%。
  - [Mind2Act World](#mind2act-world)：把机器人任务拆成推理、动作和闭环组合测试，定位失败究竟来自想错、做错还是无法边做边修正。
- **多模态模型**
  - [WeMM-Video](#wemm-video)：统一处理声音与画面，并按任务切换快速回答或显式推理，补齐开源模型的跨模态视频理解短板。
  - [Depth Pro 2](#depth-pro-2)：用单一网络同时保持物体边界清晰和视频跨帧稳定，输出原始分辨率且尺度准确的深度图。
  - [HiUni](#hiuni)：让视觉理解与图像生成共享编码器和主干，仅在输出端分工，减少重复计算并保留细粒度空间信息。
- **热点延伸**：[AGI之后是什么](#agi-asi)、[MC-Lens](#mc-lens)、[PMD](#pmd)、[EgoCaptioner](#egocaptioner)

## 对当前研究的启发
- **ReasoningEvolve**
  - 迁移｜从 [Forward-Only Passes](#forward-only-passes) 把前向激活角度集中度用到在线适应：逐层裁剪低贡献成分，记录精度、时延与显存
  - 延续｜[Forward-Only Passes](#forward-only-passes) 留下深层LLM扩展性未验证：在7B与32B模型对比LoRA，测适应收益、吞吐和显存
- **EvalEvolve**
  - 迁移｜从 [Mind2Act World](#mind2act-world) 把能力拆分诊断用到具身评测：分别测推理、动作与闭环，并报告组合能力缺口
  - 延续｜[TuringSpace](#turingspace) 留下模型固守错误视觉判断的问题：对比强制重看与原流程，测信念纠正率和成功率
- **EnvironmentEvolve**
  - 迁移｜从 [TuringSpace](#turingspace) 把程序化交互验证码用到环境生成：按模型成功率调整布局难度，持续生成可验证任务
- **PhysicalEvolve**
  - 迁移｜从 [Depth Pro 2](#depth-pro-2) 把时序稳定的度量深度用到机器人感知：对比普通单目深度，测抓取成功率与位姿抖动
- **NewModel**
  - 迁移｜从 [WeMM-Video](#wemm-video) 把快答与显式推理双模式用到模型评测：对比固定模式和任务路由，测准确率与响应时延
  - 迁移｜从 [HiUni](#hiuni) 把共享视觉骨干用到统一模型消融：同算力对比分离骨干，测理解、生成质量与推理成本
- **RobotEvolve**
  - 延续｜[Mind2Act World](#mind2act-world) 留下单项能力难以组合的问题：加入逐步环境反馈训练，对比开环策略，测恢复率与完成率

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-21/  

