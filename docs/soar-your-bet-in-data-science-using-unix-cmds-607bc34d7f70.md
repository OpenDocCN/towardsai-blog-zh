# 使用 Unix Cmds 在数据科学上大展身手

> 原文：<https://pub.towardsai.net/soar-your-bet-in-data-science-using-unix-cmds-607bc34d7f70?source=collection_archive---------2----------------------->

## [数据科学](https://towardsai.net/p/category/data-science)

当我问你，“你使用命令行/终端的目的是什么？”，您可能会告诉我“显然，要运行脚本！🙄".我知道我们用它来运行脚本，但是我们还能用它做什么呢？如果你是一个在编程领域工作了一段时间的人，你知道我要去哪里，但是如果你是一个新手，刚刚进入编码世界，你可能没有太多的想法。这完全不是问题。考虑到你是个新手，这很自然。

如果你不知道上述问题的答案，那么下面就是:

> 更好地控制操作系统或应用程序；更快地管理许多操作系统；能够存储脚本以自动执行常规任务；基本的**命令** - **线**接口知识，帮助排除故障，如网络连接问题。

![](img/a84412bdb7f9f52407aacb3a2999316c.png)

由 [Unsplash](https://unsplash.com/s/photos/files?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) 上的[Cup 先生/杨奇煜·巴拉](https://unsplash.com/@iammrcup?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)拍摄的照片

我们显然不会讨论故障排除，但是我们肯定会讨论文件管理和控制其他任务。如果你是一个有抱负的数据科学家或数据分析师，我想让你知道 Cmd 将会是一个非常重要、普遍和强大的工具💪用于管理文件和修改文件中数据的工具。

在这篇博客中，我不会讨论每一个可用的命令。我将讨论一些重要的命令和技术。

# 命令

![](img/71e5e5d41e948a0c0b96e2fcaf5309e2.png)

照片由 [Karina Vorozheeva](https://unsplash.com/@_k_arinn?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) 在 [Unsplash](https://unsplash.com/s/photos/cat?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) 上拍摄

## 猫:

这用于查看文件的内容。

> ***语法:*** 猫文件名
> 
> 例如:猫粮/汉堡. csv

它将让您查看 burger.csv 文件的内容。

![](img/316076faed561bbb083e71d86d30370a.png)

[K8](https://unsplash.com/@k8_iv?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) 在 [Unsplash](https://unsplash.com/s/photos/less?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) 上的照片

## 减去:

这是用来一次查看一个页面，我们可以用这个命令来使用多个文件。我们可以在这个命令中使用一些特殊的标志。

> ***语法:*** 文件名少文件名…

查看时，如果我们想向下翻页，请使用空格键。

*   :n 用于转到下一个/第二个文件。
*   :p 转到上一个文件。
*   :q 退出。

有时我们想查看文件的顶部或最后几项。我们也有处理这件事的命令。

![](img/2bcbabd038814591ea96f591296e5dec.png)

照片由[安德烈斯·埃雷拉](https://unsplash.com/@andresherrerapics?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)在 [Unsplash](https://unsplash.com/s/photos/head?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) 拍摄

## 头部:

这用于查看文件的前几项。

> ***语法:*** 头文件名

我们甚至可以用“-n”后跟您想要的行数来指定我们想要的行数。例如

> head -n 3 文件名

![](img/cf11faf5c3449d9db9918099309d022b.png)

[Jason Leung](https://unsplash.com/@ninjason?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) 在 [Unsplash](https://unsplash.com/s/photos/tail?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) 上的照片

## 尾巴:

现在应该很直观了，这选择了文件的最后几个元素。

> **语法**:尾部文件名

它可以做 head 命令所做的事情。

> tail -n 3 文件名

如果你想知道一个命令做什么，那么你所要做的就是使用这个名为“man”的命令

> ***语法*** : man cmd_name

head 和 tail 命令用于选择行，而“cut”命令用于选择列。

![](img/f7a25586363cd0838757bb7753a3ee98.png)

[品牌&人](https://unsplash.com/@brandsandpeople?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)在 [Unsplash](https://unsplash.com/s/photos/cut?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) 上拍照

## 剪切:

这用于按列选择数据。

它有一些标志，我们可以使用。

*   -c:要按字符剪切，请使用-c 选项。
*   -b:提取特定的字节。
*   -d: **cut** 使用**制表符**作为默认字段分隔符，但也可以通过使用 **-d** 选项使用其他分隔符。
*   -f:要按字段剪切，请使用-f 选项。

## 示例:

截 f 2–5，8 -d " "文件名. csv

在这里，我们从 2 到 5 和 8 中选择字段，并考虑将“”(空格)作为分隔符/分隔符。

考虑下面的情况，如果我们使用一个命令，它返回一个错误，因为我们在错误的目录。我们愿意找到正确的目录，但对键入我们之前编写的整个命令不感兴趣。我们用“！”重新运行命令。

## **重新运行(！)**:

## 示例:

> head roti.csv #抛出一个错误，因为我们在错误的目录中。
> 
> cd 食物#我们去正确的目录
> 
> ！head #重新运行上面的 head 命令。

当我们想要选择包含特定值的行时，我们使用命令“grep”。

![](img/02f4179b1e35f3297b970331ac5d0d61.png)

[S Migaj](https://unsplash.com/@simonmigaj?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) 在 [Unsplash](https://unsplash.com/s/photos/grab?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) 上的照片

## grep:

它接受一段文本，后跟一个或多个文件名，并打印这些文件中包含该文本的所有行。

## 示例:

> grep《妈妈咪呀！!"dosa.txt

有时候我们想存储命令的结果。我们很容易做到这一点。

![](img/0200b7fdc3eb3eb0c551f87172e5ed9b.png)

由 [Lars Kienle](https://unsplash.com/@larskienle?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) 在 [Unsplash](https://unsplash.com/s/photos/storing-data?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) 上拍摄

## 存储数据:

需要">"来存储数据。它的用法如下。

**语法**:

> head -n 5 food/idli.csv > top.csv

这将 idli.csv 的前 5 行存储在 top.csv 文件中。

![](img/1b6d22fcef5ca8221ed697c2ede409e6.png)

迈克尔·泽兹奇在 [Unsplash](https://unsplash.com/s/photos/combine?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) 上拍摄的照片

## 组合命令

这是非常重要的，因为我们在使用终端和 Unix 处理数据时一直在使用这种方法。

我们可以通过使用流水线方法来组合两个或更多的命令，从技术上来说，就是使用键盘上的“|”(管道)键。

## 示例:

> head-n 5 food/biriyani . CSV | tail-n 3 > top _ bottom . CSV

这是一个非常重要的概念，你应该记住。这是让你的生活更轻松的概念之一。

有些时候，我们想通过字符或单词，甚至通过行来计算记录。为此，我们将使用“wc”命令。

![](img/30dd386e7141fbcb95690503d8156e21.png)

在 [Unsplash](https://unsplash.com/s/photos/count?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) 上由[Towfiqu barb huya](https://unsplash.com/@towfiqu999999?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)拍摄的照片

## wc:

它用于记录计数。通过使用标志，您甚至可以指定要计数的内容。

*   -c:性格
*   -女:单词
*   -l:线条

**举例**:

> grep“2017–07”季节性/春季| wc -l

在上面的示例中，我选择了带有“2017–07”的所有内容，并按行计算出现的次数。

到目前为止，如果我们想选择多个文件，我们只需把它们打出来。我们可以通过使用通配符“*”来减少这种情况。

![](img/9137ff2c095aec47c2c7a783b951547e.png)

照片由[昆汀·雷伊](https://unsplash.com/@quentinreyphoto?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText)在 [Unsplash](https://unsplash.com/s/photos/joker-card?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText) 拍摄

## 通配符(*):

用于一次选择多个文件。

**示例**:

> cut -d，-f 1 季节性/*。战斗支援车

我从季节性目录的每个文件中获取第一个带分隔符的字段。

我们可以在管道中使用“>”，但它应该出现在最后。例如

> cut -d，-f 2 季节性/*。csv >牙齿专用. txt | grep -v 牙齿

在上面的例子中，所有的输出都存储到*tooth-only . txt*中，使得 grep 永远等待一些输入。相反，你可以这样做

> cut -d，-f 2 季节性/*。csv | grep -v tooth >牙齿专用. txt

这就是你应该如何使用管道重定向。

当您运行一个命令而没有任何反应，并且您无法运行另一个命令时，请按下 **Ctrl + C** 。

## 环境变量:

它们是用来存储数据的。一些常见的变量是头、用户

定义变量时使用大写字母。这是惯例。

您可以使用以下命令打印变量。

> echo $var_name

我们使用$是因为这允许 shell 区分文件名和变量名的值。

我们像在任何编程语言中一样使用“=”符号来存储数据。

**示例**:

> 培训=季节性/夏季. csv

## for 循环:

如果我们想重复命令一段时间，我们可以使用循环。我们特别使用“for 循环”。

**语法:**

> 为..定义变量..在..目录..；做..身体..；完成的

**例子**:

> 用于$@ #中的文件名，用于传递文件的特殊符号。
> 
> 做
> 
> head -n 2 $filename | tail -n 1
> 
> tail -n 1 $filename
> 
> 完成的

如果您想要更好的可读性，可以使用缩进。

我们可以用文件来存储命令。这些类型的文件称为脚本。

## **编辑脚本**:

您应该知道以下使用这些脚本的快捷方式。

编辑脚本，即使用“nano”命令进入脚本。

> 纳米文件名

在里面我们可以使用这些快捷方式。

Ctrl + K:删除一行。

取消删除一行。

Ctrl + O:保存文件(“O”表示输出)

Ctrl + X:退出编辑器。

正如我前面说过的，我们可以使用这些脚本来存储一些命令，并按照我们的意愿重用它们。为了便于你理解，我将向你展示一个例子。

> nano header.sh
> 
> # inside header.sh
> 
> grep -v“牙齿”季节性/春季. csv
> 
> 按 ctrl + o，然后按 enter。#保存内容。
> 
> 按 ctrl + x 退出文件。
> 
> bash header.sh #通过使用它，我们可以使用里面的命令。

## 将文件名传递给脚本:

在前面的 for 循环示例中，我使用了一个特殊字符“$@”。这用作文件名的占位符。

假设我们有" *unique-dish.sh"* ，其中包含以下命令。

> 排序$@ |排序

当我们奔跑时

> unique-dish.sh 食品/汉堡. csv

文件中的$@被替换为传递的文件名，即 burger.csv。我们可以一次给它多个文件名。

这些是我介绍过的 Unix 命令。请注意，这还不是全部。我刚刚提到了这些，因为它们对于数据科学非常重要。

其他大多数命令都类似于 windows 的命令行。所以你不需要担心。

# 结论

关键要点是

*   我们学习了一些重要的命令。
*   我们学到了一些重要的技术。
*   我们学习了如何通过例子来应用它们。

我希望这篇博客对你有所帮助。如果你喜欢这个博客，那么我建议你在[媒体](https://karthikbhandary2.medium.com/)和 [YouTube](https://www.youtube.com/channel/UCKplT0-YqAQdCq6Xajcq5Tw) 上关注我，了解更多关于生产力、自我提升、编码和技术的内容。

同时，你为什么不看看我最近的作品:

[](https://medium.datadriveninvestor.com/testing-can-skyrocket-your-data-science-game-c193ac3e39e6) [## 测试可以让你的数据科学游戏一飞冲天

### 使调试变得轻而易举

medium.datadriveninvestor.com](https://medium.datadriveninvestor.com/testing-can-skyrocket-your-data-science-game-c193ac3e39e6) [](https://medium.com/mlearning-ai/data-science-with-raspberry-pi-and-smart-sensors-1c32c34e5ee1) [## 利用 Raspberry Pi 和智能传感器进行数据科学

### 它如何改变一切

medium.com](https://medium.com/mlearning-ai/data-science-with-raspberry-pi-and-smart-sensors-1c32c34e5ee1)