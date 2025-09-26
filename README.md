# MICL
多模态上下文学习的一些研究、总结与心得


| 基本信息 | 主要内容 |
|:-------|:--------:|
| 1. Towards Multimodal In-Context Learning for Vision & Language Models, 2024, ECCV.   |  现有的 Vision-Language Models （VLMs）在零样本（zero-shot）任务上性能不错，但在 Few-Shot / In-Context Learning（ICL）任务上表现欠佳。为此提出了一个针对多模态 In-Context Learning（ICL）的指令调优（instruction tuning）方法，将输入构造成“多轮对话”的形式，每一轮包含若干图像+文本示例（shots）以及后续 query；在训练中混合不同数量的 shots（any-shot setting），确保模型能在 zero-shot、one-shot、few-shot 等情况下都能工作；同时混合 ICL 任务数据和普通 instruction-tuning 数据，避免模型遗忘零样本能力。  |
|2. What Factors Affect Multi-Modal In-Context Learning? An In-Depth Exploration, 2024, NeurIPS. | **主要还是调研性的论文**。系统地设计实验，控制并比较不同条件下 VLM 的 ICL 表现，例如 示例数量（shots）、示例与测试样本的语义相似性、模态一致性（是否图文对齐）、示例顺序 等因素，并在多个下游任务（如图文匹配、VQA、图文分类）上进行评估。主要发现：示例的语义相关性比数量更关键，高相关示例能显著提升 ICL 性能；模态对齐与一致性 对多模态 ICL 成功至关重要，错配会削弱模型推理能力；示例顺序对结果有非对称性影响，提示了提示工程（prompt design）的重要性；总体上，多模态 ICL 的效果仍然不稳定，模型对噪声和无关示例较为敏感。 |
