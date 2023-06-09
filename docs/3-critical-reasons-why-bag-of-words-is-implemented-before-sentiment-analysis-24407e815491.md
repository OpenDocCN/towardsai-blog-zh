# 为什么在情感分析之前实施单词包的 3 个关键原因

> 原文：<https://pub.towardsai.net/3-critical-reasons-why-bag-of-words-is-implemented-before-sentiment-analysis-24407e815491?source=collection_archive---------4----------------------->

## 如何为每一个 NLP 用例使用代码与 Python 集成单词包？

![](img/68773a2c029b10b2cc3212f2e5bf71dd.png)

米格尔·Á。来自 Pexels 的 padrián

单词包是文本的表示，其中每个单词由一个数字表示，这是一种从文本中提取信息的方式，而不必依赖于单词的顺序。这对于自然语言处理中的各种任务是很重要的，例如文本分类和主题建模。

1.  单词包很重要的第一个原因是它可以帮助减少需要处理的数据量。例如，考虑句子“我喜欢吃苹果和橘子。”如果我们想知道句子中提到了多少水果，我们可以数出单词“水果”出现的次数。然而，如果句子是“我喜欢吃橘子和苹果”，这就不行了在这种情况下，我们需要知道单词的顺序来确定提到的两种水果。有了一袋袋的单词，我们可以简单地看“苹果”和“橘子”对应的数字，就知道提到了两种水果，而不用担心顺序。
2.  单词包对于情感分析至关重要的另一个原因是，它可以帮助处理单词的不同形式。例如，考虑句子“我去了商店。”如果我们想知道说话者是否去了一家特定的商店，我们需要查看句子周围的上下文。但是，如果句子是“我去了商店”，我们就知道提到了多个商店，而不必看上下文(这是因为“商店”和“商店”在上下文中具有相同的含义；因此，它们将由一个单词包中的相同数字来表示。)
3.  一袋单词对于处理同义词也很重要，尤其是在进行情感分析的时候。例如，考虑句子“我喜欢喝咖啡和茶。”如果我们想知道说话者是否既喜欢咖啡又喜欢茶，我们可以简单地看看对应于“咖啡”和“茶”的数字，就知道它们都有积极的情绪。然而，如果句子是“我喜欢喝咖啡或茶”，我们需要看上下文来确定说话者是喜欢咖啡和茶，还是只喜欢其中一种。

![](img/c9f05e7f2200bf462c3040bda13ee7b2.png)

来自佩克斯的克里斯蒂娜·莫里路

# **深入词汇袋模型**

单词包模型是一个简单的统计语言模型，其中文本(句子或文档)被表示为其单词的包(多重集)，不考虑语法甚至词序，但保持多样性。该模型通常用在文档分类方法中，其中单个单词的标识被用作训练分类器的特征，并且这些模型可以通过添加 n 元语法作为特征而不是仅仅单个单词来扩展以考虑单词顺序。此外，该模型还被用作更复杂模型的一部分，例如潜在语义分析和潜在狄利克雷分配。

单词袋模型通常不单独使用，而是作为更大模型的一部分。术语“单词袋”本身有时用来指整个模型，包括它是其中一部分的更大的模型。该模型可以被认为是 n 元模型的一个特例，其中 n=1。

我将按照以下格式向大家介绍这篇文章的后续内容:

> ***1。简介
> 2。历史
> 3。型号
> 3.1 表示
> 3.2 分类
> 3.3 其他用途
> 4。参见
> 5。参考文献***

![](img/f8c6ec2222a408c4d50b270534880497.png)

来自 Pexels 的 Ivan Bertolazzi

# **简介**

词袋模型是一种统计语言模型，其中文本(句子或文档)被表示为其词的袋(多重集)，不考虑语法甚至词序，但保持多样性[1][2]。词袋模型在计算机视觉用例的实现中有一个反复出现的趋势[3]。

单词袋模型通常用于文档分类方法，其中每个单词的出现被用作训练分类器的特征[4][5]。这些模型可以通过添加 n 元语法作为特征而不仅仅是单个单词来扩展，以考虑词序。[6]

词袋模型也被用作更复杂模型的一部分，如潜在语义分析[7]和潜在狄利克雷分配[8][9]。

单词袋模型通常不单独使用，而是作为更大模型的一部分。术语“词袋”有时用来指整个模型，包括它所属的更大的模型。

单词袋模型可以被认为是 n-gram 模型的一个特例，其中 n=1。

# **历史**

词袋(BoW)是自然语言处理(NLP)中的一种流行技术，具有跨文本分类和文本聚类的历史用例，将文本表示为词的向量。虽然单词的顺序并不重要，但单词的频率才重要。基于单词表示的包来组织文本对于文本分类和文本聚类用例是有用的。

使用 Python 实现和计算单词包表示通常很简单:对于给定格式的文本(通过它我们可以导入文本进行分析)，我们只需计算每个单词在相应文本中被识别的次数。接下来，我们将讨论分类和聚类可以受益于 BoW 技术的用例。

分类是给文档分配标签的任务，例如“垃圾邮件”或“非垃圾邮件”我们可以使用标记文档的训练集来训练分类器来实现这一点。简单地说，训练集中的每个文档都表示为一个单词包向量。分类器然后可以学习哪些单词与每个标签相关联。例如，如果训练集包含许多标记为“垃圾邮件”的文档，那么分类器将了解到单词“免费”、“报价”和“获胜”与“垃圾邮件”标签相关联。当分类器得到一个新文档时，它可以使用单词包表示来决定该文档是“垃圾邮件”还是“非垃圾邮件”

文本聚类是一项基于文档内容将文档分组在一起的任务。例如，我们可能希望将所有关于“体育”或“政治”的文档组合在一起。为了达到这个分组级别，我们可以使用 k-means 之类的聚类算法:首先，我们需要计算所有文档对之间的相似性(为此，我们可以使用单词袋表示法。)然后，对于每个文档，我们计算与预期文本的每个其他文档的余弦相似性。文本源然后基于它们的相似性被聚类在一起。

![](img/2e9702db2c3b06fed0eed253582940a1.png)

Pexels 的 MESSALA CIULLA

# **文档表示**

单词袋模型将文本(句子或文档)表示为单词袋(多重集)，不考虑语法甚至词序，而是存储以保持多样性[1][2]。

例如，考虑下面两句话:

句子 1:约翰喜欢打篮球。

句子 2:简喜欢唱歌。

句子 1 的单词包表示如下:

**{约翰，喜欢，去，玩，篮球}，**

而句子 2 的单词包表示将如下:

**{简，喜欢，来，唱}。**

可以看出，没有考虑单词的顺序，句子 1 和句子 2 都被表示为每个 5 个单词的包。

# **文档分类**

单词袋模型通常用于文档分类方法[4][5]，其中可以基于单词在文本中的出现次数为其接收的特征建立训练模型。这些模型可以扩展到通过添加 n 元语法作为特征而不仅仅是单个单词来接收单词顺序的输入。

例如，考虑以下两个文档:

文件 1:约翰喜欢打篮球。简喜欢唱歌。

文件 2:约翰每天都打篮球。

文档 1 的单词包表示将是:

{约翰，喜欢，去，玩，篮球，简，喜欢，去，唱歌}，

而文档 2 的单词包表示将是:

约翰每天都打篮球。

从这个例子中可以看出，单词袋表示没有考虑词序。然而，这可以通过使用 n-grams 而不是单个单词作为特征来解决。例如，文档 1 的二元模型(2-grams)将是:

**{(约翰，喜欢)，(喜欢，去，(去，玩)，(玩，篮球)，(简，喜欢)，(喜欢，去，(去，唱歌)}，**

而文档 2 的二元模型将是:

**{(约翰，打球)，(打球，篮球)，(篮球，每)，(每，日)}。**

# **其他用途**

词袋模型也被用作更复杂模型的一部分，如潜在语义分析[7]和潜在狄利克雷分配[8][9]。

潜在语义分析是一种通过产生一组代表文档和术语的潜在因素来分析文档和它们所包含的术语之间的关系的技术[13]。它类似于单词袋模型，将文档表示为单词计数的向量。尽管如此，它还是有所不同，因为它也使用奇异值分解(SVD)来降低文档向量的维数。这种方法以特征选择的形式出现。

潜在狄利克雷分配是一种概率主题建模技术，类似于潜在语义分析，但它另外使用了潜在因素上的狄利克雷先验。这使得模型能够表现的主题更加灵活。

**参见:**

> n 元语法
> TF-IDF
> 潜在语义分析
> 潜在狄利克雷分配

就这样了，伙计们。我不喜欢提供冗长的介绍或冗长的结论来占据不必要的空间。如果你对这个话题有任何问题或建议，请和我分享你的想法。

*参考文献*

*1。罗森菲尔德，罗尼；伯恩哈德·普法林格；彼得·格伦瓦德(2006 年)。“通过校准概率估计的多标签分类”。在窦，史蒂夫；罗、辛；周，志华。人工智能的进展。计算机科学讲义。4303.斯普林格。第 417-430 页。doi:10.1007/11761157_32。高密度脂蛋白:1808/10864。*

*2。克里斯托弗·曼宁；拉格哈万，普拉巴卡尔；辛里奇·舒茨(2008 年)。信息检索导论(第 1 版。).剑桥大学出版社。ISBN 978–0–521–88523–7。*

*3。Dalal，Navneet 比尔·特里格斯(2005 年)。“用于人体检测的定向梯度直方图”。在莱昂·博图；Yann LeCun 约舒阿·本吉奥；帕特里克·哈夫纳；杰夫罗伊·e·辛顿(编辑。).计算机视觉-ECCV 2005。计算机科学讲义(人工智能讲义)3713。施普林格柏林海德堡。doi:10.1007/11564096_60。*

*4。塞巴斯蒂安尼，法布里齐奥(2002)。“自动文本分类中的机器学习”。美国计算机学会计算调查(CSUR)34(1):1–47。doi:10.1145/582415.582416。ISSN 0360–0300。S2CID 11951775X。*

*5。伊恩·威滕；弗兰克，艾贝(2005 年)。数据挖掘:实用机器学习工具和技术(第 2 版。).摩根·考夫曼。ISBN 978–0–12–088407–0。*

*6。词袋模型-维基百科。*[*https://en.wikipedia.org/wiki/Bag-of-words_model*](https://en.wikipedia.org/wiki/Bag-of-words_model)

*7。斯科特·迪尔韦斯特；苏珊·杜迈斯；乔治·w·富尔纳斯；托马斯·k·兰道尔；理查德·哈什曼(1990 年)。“通过潜在语义分析进行索引”。美国信息科学学会杂志 41(6):391–407。3.0.CO 的 doi:10.1002/(sici)1097–4571(199010)41:6❤91::aid-asi1；2–0.ISSN 1532–2882。*

*8。戴维·布莱；安德鲁·吴；迈克尔·乔丹(2003 年)。“潜在的狄利克雷分配”。机器学习研究杂志 3:993–1022。arXiv:cs/0005042。Bibcode:2003JMachLE..3..993B。doi:10.1016/s 0047–5481(03)00351–2。*

*9。汉娜·瓦拉赫；安德鲁·麦卡勒姆；彭、费；克里斯蒂娜·古铁雷斯·考尔德伍德；Nigam，Kamal (2006 年)。“反思 LDA:为什么先验很重要”。在布雷，大卫 m。约翰·拉弗蒂；史密斯，帕德赫拉克(编辑。).神经信息处理系统进展 19 (NIPS 2006)。麻省剑桥:麻省理工学院出版社。第 1973-1980 页。国际标准书号 0–262–19513–9。*