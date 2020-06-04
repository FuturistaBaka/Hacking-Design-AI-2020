# **Note** for *Let Me Choose: From Verbal Context to Font Selection*

## Overview

### Outline

本文提出一个有趣的任务：根据输入的文本选择最合适的字体。本文构建了一个小型的（文字-字体）标注数据集，使用各种模型进行训练，对不同内容的文字推荐合适的、好看的字体。

### Main contributions


### Archi

1. ** Input **
- We propose and formulate a new task: “font recommendation from written text.” 
- We introduce a new dataset, Short Text Font Dataset, containing a variety of text examples annotated with ten different representative fonts. 
- We show that emotional repre- sentations can be successfully used to capture the underlying characteristics of sentences to suggest proper fonts. 

2. ** Frame Selection  ** ( Font Dataset )
- Choice of Fonts：To narrow down the task, we had a font expert se- lect a set of 10 display fonts that cover a wide range of trending styles. 
- Annotation Process：1）We also needed to ensure workers selected fonts based on the compre- hension of the text . 
2) We decided to treat the first, second, and third choices differently as they represent the workers’ priorities . 3) we can observe that ‘formal’ fonts like F0, F2, and F5 are often selected in business contexts .

3. ** Model **
- GloVe - BiLSTM Model —We use GloVe embeddings as in- put and a BiLSTM layer to encode word sequence information in forward and backward directions. 
- NRC Model — we use the emotional representations of words from NRC Emotion, Intensity and Valence, Arousal, and Dominance (VAD) lex- icons as input to the model. 
- BERT Model
- Emoji Model 

4. ** Evaluation Settings **
- Font Recall (FR) : that measures the performance of models in learning individual labels 

5. ** Optimization ** ( Data Augmentation )

### Reflection

1.可以考虑文本输入时自动选择字体附上优先选择级满足使用者多重需求。
2.数据集后期如何更加有效迭代值得思考（利用字体间的相似性）

