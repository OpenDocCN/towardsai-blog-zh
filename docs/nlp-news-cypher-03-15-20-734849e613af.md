# NLP 新闻密码| 03.15.20

> 原文：<https://pub.towardsai.net/nlp-news-cypher-03-15-20-734849e613af?source=collection_archive---------0----------------------->

![](img/f9aeece44d67e004df8eafa3571d3328.png)

安德鲁·科埃略在 [Unsplash](https://unsplash.com?utm_source=medium&utm_medium=referral) 上的照片

## 自然语言处理每周时事通讯

## 继续前进

你这周过得怎么样？😷

我也是。

鉴于最近发生的事件，我们发布了一个 COVID 追踪器，以跟踪来自美国 50 个州的最新 COVID 新闻。除了每个州的卫生部门和其他权威机构，我们还链接了当地和全国的新闻来源。我们使用了 3 个不同的 API:一个来自 Datawrapper 的服务器，连接到约翰·霍普斯金 COVID 数据，Feedly 的新闻 API，和 Twitter 的流媒体 API。😋

看看这个:

[](https://covid.quantumstat.com/) [## 美国 COVID Tracker - Quantum Stat

### 目前，新冠肺炎疫情正在美国蔓延。在这种情况下，一个人必须知道如何…

covid.quantumstat.com](https://covid.quantumstat.com/) 

关于大坏 NLP 数据库，我们也增加了大约 90%的数据库的研究论文！特别感谢我们的研究员 Gabi Alexandru 所做的惊人的工作。😎

[](https://datasets.quantumstat.com/) [## 大坏 NLP 数据库-量子统计-量子统计

### 自然语言处理中各种任务的数据集

datasets.quantumstat.com](https://datasets.quantumstat.com/) 

仅供参考，待在室内！

鉴于缓慢的新闻周期，本周的时事通讯会比平时短，我想这与当前的疫情有关😌。

# 本周:

> *张量流量子*
> 
> 急忙
> 
> 伊莱克特感觉
> 
> 拥抱纸
> 
> 本周数据集:危险问题

# 张量流量子

Google 推出了量子 ML 模型快速原型的开源库！

为了理解量子模型，你需要熟悉两个概念:量子数据和混合量子经典模型(目前的方法)。

量子数据:(可以生成)*可以用于化学物质和量子物质的模拟，量子控制，量子通信网络，量子计量等等。*

混合量子经典模型:好吧剧透一下，这些量子模型还没有使用量子驱动的硬件(仍然太嘈杂)，所以我们只能使用 GPU。所以这就是为什么他们是“混血儿”。

这个库的好处是:如果我们现在可以习惯这些模型，到处理器准备就绪的时候，我们将能够使用量子原理处理海量数据。但是首先，我们需要尝试一下量子框架——这就是谷歌通过这个库为我们做的事情。

**博客**

[](https://www.tensorflow.org/quantum) [## 张量流量子

### TensorFlow Quantum 是一个用于混合量子经典机器学习的库。张量流量子(TFQ)是一种量子…

www.tensorflow.org](https://www.tensorflow.org/quantum) 

**论文**:

[链接](https://arxiv.org/pdf/2003.02989.pdf)

# 急忙

嘿记得 RNNs 吗？🤣。所以即使我们都想嫁给变形金刚一辈子，rnn 还是很有用的。为什么？因为大部分使用 AI 模型的公司还在用 RNNs 做顺序 NLP 数据。(他们需要几年时间才能赶上变形金刚)。

感谢纳纳瓦特先生创建了名为“急速”的 RNN 图书馆:

[](https://github.com/lmnt-com/haste) [## lmnt-com/haste

### Haste 是融合 LSTM、层规范化 LSTM 和 GRU 层的 CUDA 实现，内置 DropConnect 和…

github.com](https://github.com/lmnt-com/haste) 

# 伊莱克特感觉

伊莱克特拉变压器很酷。为什么？因为他们改变了表现模式。他们没有在预训练期间进行掩蔽，而是转而用假词替代单词，并让模型选择正确的单词。就像 GANs 但是是 NLP！

这种新的预训练技术允许 ELECTRA 在训练期间在相同的计算下胜过当前的 NLP 变压器！(v2 小队的 SOTA)

> “我们将 ELECTRA 与其他最先进的 NLP 模型进行了比较，发现在相同的计算预算下，它比以前的方法有了很大的改进，性能与 RoBERTa 和 XLNet 相当，而使用的计算资源不到 25%。”

在下游任务方面，ELECTRA 支持文本分类、问答和序列标记。

[](https://ai.googleblog.com/2020/03/more-efficient-nlp-model-pre-training.html) [## 使用 ELECTRA 进行更有效的 NLP 模型预训练

### 语言预训练的最新进展导致了自然语言处理领域的实质性进展…

ai.googleblog.com](https://ai.googleblog.com/2020/03/more-efficient-nlp-model-pre-training.html) 

**GitHub:**

[](https://github.com/google-research/electra) [## 谷歌研究/electra

### ELECTRA 是一种新的自监督语言表征学习方法。它可以用来预训练变压器…

github.com](https://github.com/google-research/electra) 

# 拥抱纸

拥抱脸与他们的社区分享他们最喜欢的 NLP 研究论文。在下面的链接中，你会找到他们最喜欢的研究论文以及未来论文讨论的时间表。他们要把我们拉进母体！吃蓝色药丸！

[](https://github.com/huggingface/awesome-papers) [## 拥抱脸/牛逼纸

### 每周，拥抱脸团队都有一个科学日，其中一名团队成员会展示一篇很棒的 NLP 论文。我们决定…

github.com](https://github.com/huggingface/awesome-papers) 

# 本周数据集:危险问题

**什么事？**

一个包含 216，930 个危险问题和答案的数据集，用于回答问题，你猜对了。

**样品:**

以下是元数据描述符:

*   '类别' :问题类别，例如“历史”
*   value' : $字符串形式的问题值，例如“$200”
*   注意:这是“无”的最终危险！和决胜局问题
*   “问题”:问题的文本
*   注意:这有时包含超链接和其他乱七八糟的文字，例如当有一个图片或视频问题
*   '答案' :答案的文本
*   “回合”:一个“危险！”，“双重危险！”，“最后的危险！”或“决胜局”
*   注意:决胜局问题确实存在，但非常罕见(比如每 20 年一次)
*   ' show_number ':演出编号的字符串，例如' 4680 '
*   '播出日期' :以 YYYY-MM-DD 格式显示播出日期

**在哪里？**

> 每周日，我们都会对来自世界各地研究人员的 NLP 新闻和代码进行一次每周综述。
> 
> *如果你喜欢这篇文章，请帮助我们并与朋友分享！*
> 
> *如需完整报道，请关注我们的推特:*[*@ Quantum _ Stat*](http://twitter.com/Quantum_Stat)

![](img/c87c1a18680c8525762318bd130054ee.png)

[www.quantumstat.com](http://www.quantumstat.com/)