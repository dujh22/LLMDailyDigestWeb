# 2026-11-15 科研追新


> 当日精选（由提交工具自动创建）。

<!-- daily-summary:start -->

## 今日概览
- **科研自进化**
  - [MolRSI](#molrsi)：用跨任务成败经验持续改写分子搜索策略，将抗菌湿实验命中率从 8.7% 提至 15.9%。
  - [AI4AI](#ai4ai)：用搜索方向、搜索空间和评价信号三类控制权，判断自动做实验的 AI 是否真正主导研究。
  - [SPU](#spu)：隐藏真实湿实验结果并允许自主检索计算，检验科研 AI 能否找到真正影响测量结果的证据。
- **系统与工具**
  - [Gemini 4 Hydrogen](#gemini-4-hydrogen)：用动态编排器按阶段切换规划型与执行型模型，同时降低智能体的延迟和成本。
  - [DeepSeek Harness](#deepseek-harness)：以对话把临时想法或 GitHub 项目封装成插件，使一次性操作沉淀为可复用个人工具。
- **训练与路线**
  - [RL训练](#item-1)：把训练前后既有能力的整体变化纳入评测，避免只看目标分数而忽略强化学习造成的能力损失。
  - [递归自我改进](#ai-ai)：用八讲课程统一梳理自我改进的技术、评测与安全路线，补足该领域缺少全景分类的问题。

## 对当前研究的启发
- **ResearchEvolve**
  - 迁移｜从 [AI4AI](#ai4ai) 把方向、空间、评价信号控制权用到科研系统审计：逐阶段标注人机决策归属
  - 延续｜[MolRSI](#molrsi) 尚未把湿实验反馈纳入策略循环：按轮回灌结果，对比纯计算搜索的命中率与样本效率
- **EvalEvolve**
  - 迁移｜从 [SPU](#spu) 把未公开实验结果用到动态科研评测：保留隐藏任务，记录预测误差、证据利用率和调用成本
  - 延续｜[AI4AI](#ai4ai) 的自生成评价器仍需独立验证：用隐藏测试与延迟真值测量偏差、排序稳定性和作弊率
- **Awesome-RSI**
  - 延续｜[AI4AI](#ai4ai) 缺少跨代因果证据：固定预算运行多代改进，对比回滚组并测未见任务增益与退化率
- **GeneralizeEvolve**
  - 迁移｜从 [RL训练](#item-1) 把能力漂移用到后训练评测：建立训练前后任务矩阵，统计新增、保持和遗忘能力
- **SystemEvolve**
  - 迁移｜从 [Gemini 4 Hydrogen](#gemini-4-hydrogen) 把分阶段动态路由用到智能体编排：分别路由规划与执行并测质量、时延和成本
- **PersonalEvolve**
  - 迁移｜从 [DeepSeek Harness](#deepseek-harness) 把对话生成插件用到个人技能沉淀：将重复操作封装、版本化并按使用反馈更新

<!-- daily-summary:end -->


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/updates/2026-11-15/  

