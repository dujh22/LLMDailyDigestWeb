# 开源框架


# 开源框架

## 学习素材

1. 2025-07-02 14:01:48 Wednesday 机器学习 Q 与 AI：30 个必备问答
2. 2025-06-30 16:37:19 Monday 盘一盘，2017年Transformer之后，LLM领域的重要论文 https://mp.weixin.qq.com/s/1lUSlc0tvEWLuOFOP0WkUA
3. 2025-06-19 19:47:17 Thursday ｜ 信息过载时代，如何真正「懂」LLM？从MIT分享的50个面试题开始 https://mp.weixin.qq.com/s/u7aIm6jP1Nblfjr2NvakLw
4. 新鲜出炉！斯坦福2025 CS336课程全公开：从零开始搓大模型 https://mp.weixin.qq.com/s/ehHSTpysn9NXW4-P4RjkuQ

斯坦福大学 2025 年春季的 CS336 课程「从头开始创造语言模型（Language Models from Scratch）」相关课程和材料现已在网上全面发布！

课程视频：https://www.youtube.com/watch?v=SQ3fZ1sAqXI&list=PLoROMvodv4rOY23Y0BoGoBGgQ1zmU_MT_

课程主页：https://stanford-cs336.github.io/spring2025/


#### LLM 主流架构

1. [硬核拆解大模型，从 DeepSeek-V3 到 Kimi K2 ，一文看懂 LLM 主流架构](https://mp.weixin.qq.com/s/_as8aCv325cAeJ6kMv9_aA)

   1. 尽管模型能力不断提升，但其整体架构在这七年中保持了高度一致。当然，细节上仍有不少演进。例如，位置编码从最初的绝对位置（Absolute Positional Encoding）发展为旋转位置编码（RoPE）；注意力机制也从标准的多头注意力（Multi-Head Attention）逐步过渡为更高效的分组查询注意力（Grouped-Query Attention）；而激活函数方面，则从 GELU 被更高效的 SwiGLU 所取代。
   2. DeepSeek V3

      1. 论文标题：DeepSeek-V3 Technical Report
      2. 论文链接：https://arxiv.org/abs/2412.19437
      3. 多头潜在注意力机制 (MLA):通过让多个 query 头共享一组 key 和 value，从而减少 key 和 value 的总数。
      4. Mixture-of-Experts (MoE):将 Transformer 中的每个前馈模块（FeedForward）替换为多个「专家层」（每个专家层本质上也是一个前馈网络）。
         1. 论文标题：DeepSeekMoE: Towards Ultimate Expert Specialization in Mixture-of-Experts Language Models 论文链接：https://arxiv.org/abs/2401.06066
   3. Allen Institute for AI 发布的 OLMo 系列模型

      1. 论文标题：2 OLMo 2 Furious
      2. 论文链接：https://arxiv.org/abs/2501.00656
      3. 归一化层位置选择
      4. QK-Norm:本质上是另一个 RMSNorm 层，它被放置在 多头注意力模块内部，在应用旋转位置编码（RoPE）之前，对 Query 和 Key 进行归一化处理。

         1. 论文标题：Scaling Vision Transformers 论文链接：https://arxiv.org/abs/2106.04560
   4. 谷歌的 Gemma

      1. 滑动窗口注意力（sliding window attention）。
      2. 论文标题：Gemma 3 Technical Report
      3. 论文链接：https://arxiv.org/abs/2503.19786
   5. Mistral Small 3.1
   6. Llama 4
   7. Qwen3
   8. SmolLM3

      1. 论文标题：The Impact of Positional Encoding on Length Generalization in Transformers
      2. 论文链接：https://arxiv.org/abs/2305.19466
   9. Kimi K2

## 预训练

## 微调

### LLaMA-Factory

https://github.com/hiyouga/LLaMA-Factory

项目学习：https://zread.ai/hiyouga/LLaMA-Factory

入门教程：https://zhuanlan.zhihu.com/p/695287607

https://blog.csdn.net/zt0612xd/article/details/147726799

中文教程：https://llamafactory.readthedocs.io/zh-cn/latest/getting_started/data_preparation.html#id4

报错：

LLaMA-Factory 模型合并 ImportError: cannot import name ‘DTensor‘ from ‘torch.distributed.tensor‘ 报错解决记录 https://blog.csdn.net/ygxdmss1412/article/details/148742597

### ms-swift

https://github.com/modelscope/ms-swift

ms-swift 是 ModelScope 社区提供的官方框架，用于大语言模型和多模态大模型的微调与部署。它目前支持 500+ 大模型和 200+ 多模态大模型的训练（预训练、微调、人类对齐）、推理、评估、量化和部署。这些大语言模型（LLMs）包括 Qwen3、Qwen3-MoE、Qwen2.5、InternLM3、GLM4、Mistral、DeepSeek-R1、Yi1.5、TeleChat2、Baichuan2 和 Gemma2 等模型。多模态 LLMs 包括 Qwen2.5-VL、Qwen2-Audio、Llama3.4、Llava、InternVL2.5、MiniCPM-V-2.6、GLM4v、Xcomposer2.5、Yi-VL、DeepSeek-VL2、Phi3.5-Vision 和 GOT-OCR2 等模型。

### Unsloth

## 强化学习

学习教程：从RLHF、PPO到GRPO再训练推理模型，这是你需要的强化学习入门指南 https://mp.weixin.qq.com/s/TZRqK8Waj3bt2VTeyZYjmg
原文地址：https://docs.unsloth.ai/basics/reinforcement-learning-guide

开源项目：https://github.com/unslothai/unsloth

### 🌈 OpenRLHF

github：https://github.com/OpenRLHF/OpenRLHF

支持比GRPO更稳定的REINFORCE++

#### 多模态二创：MM-EUREKA

https://github.com/ModalMinds/MM-EUREKA

### Open-R1

使用Open-R1框架在MATH数据集的训练集上进行训练。

### TinyZero

https://github.com/Jiayi-Pan/TinyZero

[TinyZero最详细复现笔记（一）](https://zhuanlan.zhihu.com/p/1903191617571125117)

1. TinyZero项目在尽可能小的模型、尽可能简单的实验设置下，复现了DeepSeek-R1-Zero模式的核心成果：仅通过基于规则的强化学习，就能让模型自发出现思维链，并显著提升推理能力。

[TinyZero最详细复现笔记（二）：VeRL框架与PPO训练细节](https://zhuanlan.zhihu.com/p/1903855264207200959)

### Roll

重磅！淘天联合爱橙开源强化学习训练框架ROLL，高效支持十亿到千亿参数大模型训练 https://mp.weixin.qq.com/s/4JaXQd_X_XheZuSILfE2Pw

1. 强化学习（Reinforcement Learning，RL）已成为大语言模型（Large Language Model，LLM）后训练阶段的关键技术。RL 不仅显著提升了模型的对齐能力，也拓展了其在推理增强、智能体交互等场景下的应用边界。围绕这一核心范式，研究社区不断演化出多种优化策略和算法变体，如 Agentic RL、RLAIF、GRPO、REINFORCE++ 等。

* 开源项目：https://github.com/alibaba/ROLL
* 论文标题：Reinforcement Learning Optimization for Large-Scale Learning: An Efficient and User-Friendly Scaling Library
* 论文地址：https://arxiv.org/pdf/2506.06122
* 

### R1-V

### TRL

link：https://zhuanlan.zhihu.com/p/693304721

TRL 是huggingface中的一个完整的库，用于微调和调整大型语言模型，包括 [Transformer 语言](https://zhida.zhihu.com/search?content_id=242198265&content_type=Article&match_order=1&q=Transformer+%E8%AF%AD%E8%A8%80&zhida_source=entity)和[扩散模型](https://zhida.zhihu.com/search?content_id=242198265&content_type=Article&match_order=1&q=%E6%89%A9%E6%95%A3%E6%A8%A1%E5%9E%8B&zhida_source=entity)。这个库支持多种方法，如[监督微调](https://zhida.zhihu.com/search?content_id=242198265&content_type=Article&match_order=1&q=%E7%9B%91%E7%9D%A3%E5%BE%AE%E8%B0%83&zhida_source=entity)（Supervised Fine-tuning, SFT）、[奖励建模](https://zhida.zhihu.com/search?content_id=242198265&content_type=Article&match_order=1&q=%E5%A5%96%E5%8A%B1%E5%BB%BA%E6%A8%A1&zhida_source=entity)（Reward Modeling, RM）、[邻近策略优化](https://zhida.zhihu.com/search?content_id=242198265&content_type=Article&match_order=1&q=%E9%82%BB%E8%BF%91%E7%AD%96%E7%95%A5%E4%BC%98%E5%8C%96&zhida_source=entity)（Proximal Policy Optimization, PPO）以及[直接偏好优化](https://zhida.zhihu.com/search?content_id=242198265&content_type=Article&match_order=1&q=%E7%9B%B4%E6%8E%A5%E5%81%8F%E5%A5%BD%E4%BC%98%E5%8C%96&zhida_source=entity)（Direct Preference Optimization, DPO）。

支持GRPO

### 🌈 veRL

link：https://www.volcengine.com/docs/6459/1463942

[veRL](https://github.com/volcengine/verl) 是火山引擎推出的用于大语言模型（LLM）的强化学习库，具有灵活性、高效性且适用于生产环境。

支持GRPO

sglang小组也在用

#### EasyR1

link：https://aws.amazon.com/cn/blogs/china/building-llm-model-hub-based-on-llamafactory-and-easyr1/

EasyR1 是基于火山引擎 veRL 框架开发的专为大语言模型 / 视觉语言模型（LLM / VLM）设计的高性能强化学习训练框架，支持 GRPO 等多种强化学习算法。

### Logic- RL

[LLM界的AlphaGo：DeepSeek R1 Zero保姆级复现教程来了！](https://zhuanlan.zhihu.com/p/22769760306)

https://github.com/Unakar/Logic-RL

## 部署

### vLLM

### SGLang

### TGI

## 未分类

### MoE部署

华为：推理超大规模MoE背后的架构、技术和代码 Omni-Infer https://mp.weixin.qq.com/s/sfC5l0wYGrrs0Kfrz3ZzyA

1. https://mp.weixin.qq.com/s/e5Nl__L5lty0XHkM6Qd8cQ
2. 推理 与 推理加速


---

> 作者: [LLM-DailyDigest](https://github.com/dujh22/LLM-DailyDigest)  
> URL: https://dujh22.github.io/LLMDailyDigestWeb/resources/%E5%BC%80%E6%BA%90%E6%A1%86%E6%9E%B6/  

