# Prompt2Act
Prompt2Act: Transforming Prompts into Sequence of Actions with Large Foundation Models
① 传统的方案只是借助已有的函数库，基于llm的方案xxx，很多动作不能完成的时候需要代码生成。To address this challenge, we introduce a novel approach called "Prompting Purpose into Sequence of Actions with Large Foundation Models" (Prompt2Act). This framework enables the generation of a sequence of actionable steps by leveraging existing action skills or adaptively generating executable code through a vision-language model (VLM). And to enhance vlm的grounding能力，我们引入了

General-purpose robotic system. We introduce a framework prommpt2Act that marrying robots with Large foundation models, our framework enables the generation of a sequence of actionable steps by leveraging existing action skills or adaptively generating executable code through a vision-language model (VLM)
Instruct2Act, that leverages the in-context learning ability of LLMs and multi-modality
instructions to generate middle-level decision-making actions from both natural language
and visual instructions.


策略、视觉增强、通用框架、多模态指令、sota效果
Contributions:
② It supports versatile multimodal prompts for purpose specification. It can effectively utilize not only text instructions but also a diverse of goal images, audios, and various combination of both text and visual information, to define purpose precisely. 
③ Through comprehensive evaluations in both real-world and simulated settings, Prompt2Act consistently surpasses existing LLM-based planners, showcasing its efficiency across various of open-world manipulation tasks. Moreover, our zero-shot approach outperforming several state-of-the-art learning-based strategies in various challenging scenarios.Our framework can be applied to real-world scenarios in a cost-effective and time-efficient manner, with the extensibility of the Prompt2Act framework allowing users to integrate additional foundation models for broader applications.
 
 a novel approach for long-horizon robotic planning that leverages vision-language models (VLMs) to generate a sequence of actionable steps.

 To address this challenge, we introduce a novel approach called "Prompting Purpose into Sequence of Actions with Large Foundation Models" (Prompt2Act). This framework enables the generation of a sequence of actionable steps by leveraging existing action skills or adaptively generating executable code through a vision-language model (VLM).

 开始画PPT画原理图 ，伪代码。









 
========================================================================================================================================================================
 Prompt2Act: Transforming Prompts into Sequence of Actions with Large Foundation Model
① 传统的反省自己做不了，基于llm的方案xxx，很多动作不能完成的时候需要代码生成。To deal with this, we introduce a novel approach "Prompting purpose into Sequence of Actions with Large Foundation"（Prompt2Act）,能够基于已有的动作skills或者自适应生成可执行代码来完成to generate a sequence of actionable steps by vlm.
② It supports versatile multimodal prompts for purpose specification. It can effectively utilize not only text instructions but also a diverse of goal images, and various combination of both text and visual information, to define purpose precisely. 
③ Through comprehensive evaluations in both real-world and simulated settings, Prompt2Act consistently surpasses existing LLM-based planners, showcasing its efficiency across various of open-world manipulation tasks. Moreover, our zero-shot approach outperforming several state-of-the-art learning-based strategies in various challenging scenarios.Our framework can be applied to real-world scenarios in a cost-effective and time-efficient manner, with the extensibility of the Prompt2Act framework allowing users to integrate additional foundation models for broader applications.
 
 a novel approach for long-horizon robotic planning that leverages vision-language models (VLMs) to generate a sequence of actionable steps.
