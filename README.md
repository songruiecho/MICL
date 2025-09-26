# MICL
多模态上下文学习的一些研究、总结与心得


| 基本信息 | 主要内容 |
|:-------|:--------:|
| Towards Multimodal In-Context Learning for Vision & Language Models, 2024, ECCV.   |  现有的 Vision-Language Models （VLMs）在零样本（zero-shot）任务上性能不错，但在 Few-Shot / In-Context Learning（ICL）任务上表现欠佳。为此提出了一个针对多模态 In-Context Learning（ICL）的指令调优（instruction tuning）方法，将输入构造成“多轮对话”的形式，每一轮包含若干图像+文本示例（shots）以及后续 query；在训练中混合不同数量的 shots（any-shot setting），确保模型能在 zero-shot、one-shot、few-shot 等情况下都能工作；同时混合 ICL 任务数据和普通 instruction-tuning 数据，避免模型遗忘零样本能力。  |
