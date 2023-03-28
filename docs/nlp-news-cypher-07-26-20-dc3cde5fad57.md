# NLP 新闻密码| 07.26.20

> 原文：<https://pub.towardsai.net/nlp-news-cypher-07-26-20-dc3cde5fad57?source=collection_archive---------2----------------------->

![](img/d2d202c8594e24c08ad090fa94230c4d.png)

由[拍摄的照片将在](https://unsplash.com/@willy_teee?utm_source=medium&utm_medium=referral) [Unsplash](https://unsplash.com?utm_source=medium&utm_medium=referral) 上真实再现

## 自然语言处理每周时事通讯

## 首席主教

T 何[李伯骁勇](https://uncovering-cicada.fandom.com/wiki/Liber_Primus)至今未破。一本用[符文](https://en.wikipedia.org/wiki/Runes)写成的 58 页的书，其中令人困惑的加密技术继续困扰着全球的黑客枪手，他们只选择通过 IRCs(互联网中继聊天)交流和研究其内容。

这本神秘的书在 2010 年中期由现在非常流行但神秘的互联网组织 3301 带到了互联网上。虽然该团体的身份仍未公开，但据推测他们是“赛博朋克”激进主义运动(80 年代诞生于伯克利的某个地方)的残余。至少这是为数不多的进入秘密组织的已知黑客之一——马库斯·万纳给我们的最合理的解释。但是谁知道呢…

3301 的蝉项目始于 2012 年一个随机的 4chan 帖子，它带领许多寻求刺激的人和狂热的追随者，进行一场涵盖从隐写术到密码学的谜题搜索。虽然他们的大部分谜题最终都被解开了，但是最后一个谜题，Liber Primus，仍然(大部分)被加密了。3301 的最后一次已知通信是在 2017 年 4 月通过 Pastebin post 进行的。上面写着:

[](https://pastebin.com/yEiTHhvF) [## 来自 3301/蝉-Pastebin.com 的消息

### 还不是 Pastebin 的成员？注册吧，它解锁了很多很酷的功能！-开始 PGP 签名消息-小心虚假…

pastebin.com](https://pastebin.com/yEiTHhvF) 

仅供参考，所有 3301 帖子都有一个标准的 PGP(相当好的隐私)密钥。如果你看到一个没有他们 PGP 签名的 3301 在线帖子，不要相信它(会发现大量的 troll 帐户)。

**对于概要/时间表**:

[](https://uncovering-cicada.fandom.com/wiki/Uncovering_Cicada_Wiki) [## 揭秘蝉维基

### 新用户，请阅读这个常见问题，如果你不知道什么是 PGP 点击这里

uncovering-cicada.fandom.com](https://uncovering-cicada.fandom.com/wiki/Uncovering_Cicada_Wiki) 

如果你有兴趣了解他们如何破解之前的蝉谜题，请访问 Nox 的 YouTube 频道。

*同时回到牧场…*

我很幸运地找到了为适配器创建培训脚本的方法(在上周的博客中讨论了模块化插件)。该脚本适用于粘合数据集。将随时向所有人更新关于 [AdapterHub](https://adapterhub.ml/) 的新事件。我对这个新框架感到非常兴奋，再次感谢 Jonas 为我指明了正确的方向。

*呆若冰霜* ✌✌

# 本周

> SimpleTOD
> 
> 涡轮变压器
> 
> 自然语言处理和音频预训练模型
> 
> 网络
> 
> AllenNLP 库分步指南
> 
> 搜索引擎很难
> 
> 本周数据集:ODSQA

# SimpleTOD

以前的面向任务的对话，特别是那些我们梦想有一天能建立的聊天机器人，是使用标准的模块化管道(类似于 RASA 框架中的管道)建立的。然而，Salesforce Research 最近发布了一个名为 SimpleTOD 的单向语言模型，试图以端到端的方式解决所有的子任务。它是用 MultiWOZ 数据集上的转换器构建的。

**博客**:

[](https://blog.einstein.ai/simpletod/) [## SimpleTOD:面向任务对话的简单语言模型

### 我们建议将面向任务的对话重铸为简单的、因果的(单向的)语言建模任务。我们表明…

博客.爱因斯坦. ai](https://blog.einstein.ai/simpletod/) 

**论文**

[链接](https://arxiv.org/pdf/2005.00796.pdf)

**GitHub** :

[](https://github.com/salesforce/simpletod) [## 销售力量/简单托

### 作者:Ehsan Hosseini-Asl，布赖恩麦肯，钱-吴声，塞米赫亚武兹，和理查德索契面向任务的对话(TOD)…

github.com](https://github.com/salesforce/simpletod) 

# 涡轮变压器

最近一个用于推理的 transformer 运行时库 TurboTransformers 引起了我的注意。该库优化了每个人在生产中想要的东西，即更低的延迟。他们声称:

> 为微信 FAQ 服务带来 1.88 倍加速，为公有云舆情分析服务带来 2.11 倍加速，为 QQ 推荐系统带来 13.6 倍加速。

好处是它可以支持各种长度的输入序列，而无需预处理，这减少了计算开销。🧐

**GitHub** :

[](https://github.com/Tencent/TurboTransformers) [## 腾讯/涡轮变压器

### 通过给你的推理机增加一个涡轮使变形金刚快速服务！变压器是最重要的算法…

github.com](https://github.com/Tencent/TurboTransformers) 

# 自然语言处理和音频预训练模型

GitHub 上有一个很好的预训练模型库集合。这两个报告包括自然语言处理和语音建模。方便的是，模型由框架索引，并包括一个简短的描述。

**NLP**

[](https://github.com/balavenkatesh3322/NLP-pretrained-model) [## balavenkatesh 3322/NLP-预训练-模型

### 预训练模型是由其他人创建的用于解决类似问题的模型。而不是从…建立模型

github.com](https://github.com/balavenkatesh3322/NLP-pretrained-model) 

**语音/音频**

[](https://github.com/balavenkatesh3322/audio-pretrained-model) [## balavenkatesh 3322/音频-预训练-模型

### 预训练模型是由其他人创建的用于解决类似问题的模型。而不是从…建立模型

github.com](https://github.com/balavenkatesh3322/audio-pretrained-model) 

# 网络

令人敬畏的新 shell/python 脚本，它从纯文本中绘制了一个共现实体的网络！

它结合了斯坦福大学的 NER 用于模型，OpenRefine(用于处理数据规范化:即 B. Obama 和 Barrack 是同一个实体)和 NetworkX 用于图形创建。

博客:[http://brandontlocke . com/2020/07/22/announcing-ner twork . html](http://brandontlocke.com/2020/07/22/announcing-nertwork.html)

**GitHub(本周个人资料照片)**:

[](https://github.com/brandontlocke/NERtwork) [## brandontlocke 网络

### 网络是一个脚本的集合，帮助你使用开源软件创建一个共现命名实体的网络图…

github.com](https://github.com/brandontlocke/NERtwork) 

# AllenNLP 库分步指南

迄今为止最好的艾伦 LP 图书馆分步指南。冗长但值得沿途粘贴代码。演示是为了建立/训练一个 NER LSTM 模型。

**博客**:

[](https://jbarrow.ai/allennlp-the-hard-way-0/) [## 第 0 部分-设置

### 本系列是我的 AllenNLP 教程，从安装到构建一个最先进的(或几乎最先进的)名为…

jbarrow.ai](https://jbarrow.ai/allennlp-the-hard-way-0/) 

# 搜索引擎很难

来自 AI2 的研究科学家讨论了构建语义学者搜索引擎的困难，该引擎目前索引了 1.9 亿篇科学论文。👀

它使用两个模型架构:通过 Elasticsearch 的稀疏搜索和一个 ranker ML 模型。

该博客深入探讨了他们在构建搜索引擎时面临的挑战，如数据复杂性和评估问题。它提供了大量的细节，超出了我在这篇文章中所能处理的范围，所以如果你对搜索感兴趣的话，可以读一读。

[](https://medium.com/ai2-blog/building-a-better-search-engine-for-semantic-scholar-ea23a0b661e7) [## 为语义学者构建更好的搜索引擎

### 改善我们的学术搜索引擎的“告诉所有”帐户。

medium.com](https://medium.com/ai2-blog/building-a-better-search-engine-for-semantic-scholar-ea23a0b661e7) 

# 本周数据集:ODSQA

## 这是什么？

ODSQA 是一个用于口语问答的中文数据集(抽取式)。它包含 3，654 个问题答案对。

**论文**:[https://arxiv.org/pdf/1808.02280.pdf](https://arxiv.org/pdf/1808.02280.pdf)

## 它在哪里？

[](https://github.com/chiahsuan156/ODSQA) [## chiahsuan156/ODSQA

### 该存储库包含 IEEE SLT 2018 论文的数据集:ODSQA:开放域口语问答数据集…

github.com](https://github.com/chiahsuan156/ODSQA) 

> *每周日，我们都会对来自全球研究人员的 NLP 新闻和代码进行一次每周综述。*
> 
> *如果您喜欢这篇文章，请帮助我们并与朋友分享！*
> 
> *完整报道，关注我们的推特:*[*@ Quantum _ Stat*](http://twitter.com/Quantum_Stat)

![](img/0855224250b129b0d74502c9bfa60db3.png)

[www.quantumstat.com](http://www.quantumstat.com/)