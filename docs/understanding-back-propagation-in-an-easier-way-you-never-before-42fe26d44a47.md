# 了解反向传播算法

> 原文：<https://pub.towardsai.net/understanding-back-propagation-in-an-easier-way-you-never-before-42fe26d44a47?source=collection_archive---------0----------------------->

## 向人工智能反向传播介绍 101 |

## ***以前所未有的方式轻松理解反向传播算法！***

你可能正在学习一门关于深度学习的课程，在开始的时候，它对你来说似乎很容易，然后你遇到了“反向传播”，你会开始挠头，因为它太"*数学化*"

![](img/1f7b8fedf3d7833925fb976b093e72b2.png)

**“为什么我们需要理解反向传播算法？**
答案很简单。我们人类总是好奇想知道现实世界中的事情是如何发生的。
比如我们看到人呼吸的时候。从外面看，这只是吸入空气释放二氧化碳。但是，人类的好奇心让我们知道，在这短短的 1-2 秒内。全血首先被氧化，然后通过神经输送到我们身体的每一个细胞。最后，它缺氧了。

人类总是好奇的想知道，控制我们周围真实世界的机制是怎样的。
对于任何深度学习实践者来说，“我们的世界围绕着神经网络旋转”。
所以，为了消磨你的好奇心&给你一个神经网络是如何训练的概念。我给你看这篇文章。

**这篇文章的上下文是:-**
1。简单介绍一下神经网络。
2。尽量让你用更简单的方式理解反向传播。
3。最后，我们将通过一个具体的例子来讨论反向传播算法。

好吧！所以，先了解什么是神经网络。

我不知道你是否知道神经网络。那么让我们先来理解这个概念。

![](img/d54333e8b16c35157aa12679bcd87aa5.png)

*神经网络是一系列算法，通过模拟人脑运行方式的过程，努力识别一组数据中的潜在关系。
神经网络能适应变化的输入；因此，网络无需重新设计输出标准即可生成最佳结果。*

或者用简单的话来说，我们可以把神经网络描述为:-

-这只是一个计算机程序，它的学习和行为方式与人脑非常相似。

-或者，这只是计算机以类似人类的方式学习事物、识别模式和做出决策的一种方式。

或者，神经网络使计算机能够从给定的发送数据中学习。

-或者，(以一种更精细的方式)人工神经网络是对组成人脑的神经元网络的模拟，以便计算机能够以类似人类的方式学习和决策。

简单地说，反向传播是训练神经网络的核心机制。其中我们计算我们期望的目标输出值&的误差，然后我们调整权重以最小化该误差。我们从错误中学习的方式与人类相似。

试着想象一下这种情况。你正试图将足球踢入球门柱。
你随意用某个角度踢球。然后你测量从球门柱到你的足球第一次到达的地方
的距离。
然后，我们试图通过改变踢球的角度来缩短这一距离。最后，我们可以把足球踢到球门柱上。

现在，用一个神经网络来比较这种情况:-
1。我们随意踢了踢足球。
在神经网络中，我们随机初始化权重。

2.我们测量从球门柱到击球点的距离。
在神经网络中，这被称为测量总误差。

3.我们以这样的方式改变了角度，以最小化这个距离

在神经网络中，这被称为更新权重以获得期望的目标输出。

为了训练神经网络，反向传播算法是一种非常强大的算法。
功能强大到用在邮政编码识别(低级例子)、人脸识别(中级例子)到声纳目标识别(高级例子)。

我希望现在你已经理解了反向传播。所以，现在你已经准备好处理反向传播的数学问题了。

## 好了，现在让我们进入反向传播算法来理解它。

![](img/dc957b48e55bda7c93c25e00a8862c7b.png)

这是一个简单的神经网络图，它有两层，分别是输入层、隐藏层和输出层。每层有 2 个神经元。

![](img/52f297d0d7d6b6b976c70aacdaafb694.png)

总而言之，神经元的功能是所有与其权重相乘的输入&偏差。
输出之后是激活功能的操作。

## 让我们用一个例子来理解反向传播:

![](img/ec8173558a8190bfd35e33a8d04faf8e.png)![](img/848853469925d1abf2c6cde7dff3227e.png)

*这里，H1 是一个神经元，样本输入为 x1=0.05，x2=0.10，偏差为 b1=0.35 & b2=0.60。
目标值为 T1=0.01 & T2=0.22*

## 现在我们随机初始化权重，

![](img/e5985ba54e831fcea485f4daead0a0cf.png)

**注意:** *在整篇文章中，我们使用 SIGMOID 作为激活函数。*

![](img/6292d21b01548f011466a17bf9f2a4af.png)

## 让我们来计算 H1、H2 和 H1 的产量，H2 的产量。

![](img/2b41fe3c962680e849ef249ff0e3de96.png)

## 同样，我们可以计算 y1，y2，输出 y1 &输出 y2。

![](img/a086d5cb04e68a9a0a9ae323fceee9a4.png)

## 计算总误差

![](img/dd81153b1b1603a95db0ba95e9bf0331.png)

## 现在我们必须反向传播，以提升权重

*考虑 w5，w5 处的误差*

![](img/c5e4fa65349dde0576d991a5fd2502c5.png)

*但在 Etotal 的表达中不存在 w5 项。
所以我们要把它拆分&应用链式法则来部分区分它。*

## 剧烈的

![](img/7b25a3f9bbb48f9b8a4fabbf9e1e5a0c.png)

*逐个部分区分各个术语。*

![](img/4eb96d0a316daf57acce7a3ca51d653c.png)![](img/ee943ee856c9b95818d8408a11c840e8.png)![](img/d874af2fcb4bf1f6a52b6d0de3d31dc3.png)

## 计算误差 w5:-

![](img/c2d2559216087e81f75db4ce3f97d769.png)

## 现在更新 w5

![](img/11577d0e1e47f2d0f0fcc50fc9fd5b6d.png)

*新更新的权重，w5=0.3595 &同理 w6=0.4086，w7=0.511 & w8=0.561。*

## 现在在隐藏层，更新 w1，w2，w3 和 w4。
考虑 w1 处的 w1
误差

![](img/1bec9acbbe61cfbcc4340da0d1b72ae7.png)

*但在 Etotal 的表达中不存在 w1 项。
因此，为了做到这一点，我们进行了多次拆分。*

# 请注意，慢慢看！

*被圈起来的术语，我们无法直接区分。所以，我们必须把他们分开。*

![](img/1bec9acbbe61cfbcc4340da0d1b72ae7.png)

请参见圈出的术语。

## **考虑用橙色圈起来的术语&让我们分开&应用链式法则。**

![](img/3cb33eb75bd1b328e60d3577ccb2b749.png)

## 正在计算:

![](img/8626454c21ea8a328ea882f3b6e74c17.png)![](img/6fcc1c36379afe16b65496bab554574f.png)

## 我们计算了被圈起来的橙色项。

![](img/aa220c82a763e4c59dad503f82ec3ba7.png)

## 考虑用蓝色圈出的术语。

![](img/562f20c7964637977885f3d8ed1b442e.png)

## 考虑用黑色圈出的术语。

![](img/49010709158544b6796e188093a0a51a.png)

## 现在我们已经计算了所有被圈起来的项。
因此，w1 处的误差为:

![](img/0c13d2743fa21d89d06c10dff7dd1714.png)

## 更新 w1:

![](img/18f316eeea82e863aed4d7e21306bf65.png)

*现在，我们有了更新后的权重 w1，同样，我们可以计算 w2、w3 & w4。到目前为止，我们所做的是首先反向传播和更新 w5、w6、w7、w8，然后在这些的帮助下，我们进一步反向传播和更新权重 w1、w2、w3 & w4。*

所以有了这些更新的权重(w1，w2，w3 & w4)。我们必须再次计算 H1 和 H2。在计算了 H1 和 H2 之后，我们可以计算 y1 产量和 y2 产量。之后，我们可以像前面一样计算总误差，并再次借助这个新的总误差。我们反向传播并更新了权重。

![](img/eab7848297a6838d3bcda8d3f963847e.png)

## 并且再次使用我们向前传播的更新的权重。

![](img/5820fcf3e92ae54c1f9c5789dfc51746.png)

*我们必须在反向传播&和正向传播&之间反复迭代。*

![](img/eab7848297a6838d3bcda8d3f963847e.png)![](img/ea9c32fbbcf3962f00376b1194016746.png)![](img/5820fcf3e92ae54c1f9c5789dfc51746.png)

*直到总误差(成本函数)最小化，或者换句话说，我们的预测输出值更接近目标值。*

用一句话来说，我们可以将反向传播定义为*这是一种训练神经网络的常用方法，其中将初始系统输出与期望输出进行比较，并调整系统，直到两者之间的差异最小化。*

> 我们现在可以说，反向传播是训练任何神经网络的中心机制。

我希望你现在已经理解了什么是反向传播算法以及它是如何工作的。

恭喜你，你刚刚理解了机器学习中最难的"*数学"*话题之一。

别忘了给我们你的👏&跟我来！！！！！！！

![](img/61ee3c58d4b040be8643e984391dfde0.png)

请鼓掌并跟我来！！！！