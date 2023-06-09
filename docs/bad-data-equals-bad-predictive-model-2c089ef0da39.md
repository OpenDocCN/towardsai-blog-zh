# 坏数据等于坏预测模型

> 原文：<https://pub.towardsai.net/bad-data-equals-bad-predictive-model-2c089ef0da39?source=collection_archive---------2----------------------->

![](img/abce22979b79d6e97204d5781214bed7.png)

图片来源:Benjamin O. Tayo

## 在使用数据进行分析或建模之前，请始终质疑数据的来源和质量

D ata 是任何数据科学和机器学习任务的关键。数据有不同的形式，如数字数据、分类数据、文本数据、图像数据、声音数据和视频数据。 ***模型的预测能力取决于建立模型时使用的数据质量*** 。因此，在执行任何数据科学任务(如探索性数据分析或构建模型)之前，问自己以下重要问题非常重要:

# ***1。我的数据来源是什么？***

用于分析或建模的数据可以从几个来源获得:

a)从挖掘和存储数据的组织或公司购买原始数据

b)调查数据

c)来自实验的数据

d)来自传感器的数据

e)模拟数据

f)来自互联网

无论数据的来源是什么，了解数据是如何收集的非常重要。例如，从调查中收集的数据可能包含大量缺失数据和错误信息。参与调查的个人可能会提供虚假信息。如果数据是模拟的，那么与样本数据相比，模拟数据有多好？例如，模拟数据可能是在假设样本数据呈正态分布的情况下生成的，但实际情况可能并非如此。有时，数据科学家可能需要与工程师和其他人员密切合作，以获得理解数据来源和可靠性的指导。

# 2.我的数据质量如何？

有几个因素会影响数据的质量，例如:

## a)数据收集错误

数据收集会在不同层面产生错误。例如，调查可以设计为收集数据。然而，参与调查的个人可能并不总是提供正确的信息。例如，参与者可能输入关于他们的年龄、身高、婚姻状况、收入等的错误信息。当设计用于记录和收集数据的系统中存在错误时，也可能发生数据收集中的错误，例如温度计中的故障传感器可能导致温度计记录错误的温度数据。

## b)数据存储中的错误

存储数据可能会导致错误，因为一些数据可能会被错误地保存，或者部分数据可能会在存储过程中丢失。

## c)数据检索中的错误

检索数据也会产生错误，因为数据的某些部分可能会丢失或损坏。

## d)数据插补误差

通常，移除样本或删除整个特征列是不可行的，因为我们可能会丢失太多有价值的数据。在这种情况下，我们可以使用不同的插值技术来估计数据集中其他训练样本的缺失值。最常见的插值技术之一是**均值插补**，我们只需用整个特征列的平均值替换缺失值。用于输入缺失值的其他选项是中值或最**频繁(模式)**，其中后者用最频繁的值替换缺失值。这对于输入分类特征值很有用。另一种可以使用的插补技术是**中位数插补**。无论您在模型中采用何种插补方法，您都必须记住，插补只是一种近似值，因此会在最终模型中产生误差。如果所提供的数据已经过预处理，那么您必须找出如何考虑缺失值。原始数据被丢弃的百分比是多少？使用什么插补方法来估计缺失值？

# 3.我的数据依赖于空间和时间吗？

了解数据的空间和时间依赖性非常重要。数据是在不同的地理位置收集的吗？数据是什么时候收集的？数据是否随时间变化？关于数据的空间和时间相关性的知识将有助于决定哪种模型适合于给定的数据。

# 案例研究:真实世界的例子

我在一个行业从事数据科学项目。我不会在这里透露该项目的全部细节。但该项目涉及使用实时生成的数据来预测一个非常重要的设备运行中的异常。我的团队必须与包括机械工程师、电气工程师、系统工程师和现场技术人员在内的多学科团队合作，以便能够使用可用数据正确构建要解决的正确问题。由于缺乏领域知识，我们不得不依靠工程师和其他人员来帮助我们确定哪些特性是关键的，目标变量是什么。通过从不同角度查看数据并执行几个数据预处理任务，我们发现大量可用数据是从坏的传感器收集的。因此，在与工程师进行了几次会议和讨论后，他们能够生成一组新的可靠的无错误数据。从这次经历中得到的教训是，在建立任何模型之前，确保你非常了解你的数据。了解数据是如何收集的很重要，如果有必要，可以向收集数据的人问几个问题。这样，您可以确保数据是无错误的和高质量的。

在学术培训项目中，我们经常被提供一个没有错误的干净的数据集。在现实世界的数据科学项目中，必须仔细检查和评估数据，以确保来源可靠，数据无误且质量高。使用高质量数据进行分析或建模有 4 个主要优势:

# 高质量数据的优势

a)高质量的数据不太可能产生错误。

b)高质量的数据可以导致较低的泛化误差，即模型很容易捕捉真实生活的影响，并可以应用于预测目的的看不见的数据。

c)由于较小的不确定性，高质量的数据将产生可靠的结果，即数据捕捉真实的效果并且具有较小的随机噪声。

d)包含大量观察值的高质量数据将减少方差误差(方差误差根据 [C **熵极限定理**随样本量减少)。](https://towardsdatascience.com/proof-of-central-limit-theorem-using-monte-carlo-simulation-34925a7bc64a)

总之，我们已经讨论了为什么在使用数据进行进一步分析或建模之前充分理解数据是极其重要的。在使用数据进行进一步分析或建模之前，务必仔细检查和评估数据的可靠性和质量。请记住，坏数据会产生伪造的和不可靠的预测模型。

# 其他数据科学/机器学习资源

[数据科学课程](https://medium.com/towards-artificial-intelligence/data-science-curriculum-bf3bb6805576)

[机器学习的基本数学技能](https://medium.com/towards-artificial-intelligence/4-math-skills-for-machine-learning-12bfbc959c92)

[3 个最佳数据科学 MOOC 专业](https://medium.com/towards-artificial-intelligence/3-best-data-science-mooc-specializations-d58da382f628)

[进入数据科学的 5 个最佳学位](https://towardsdatascience.com/5-best-degrees-for-getting-into-data-science-c3eb067883b1)

[2020 年开始数据科学之旅的 5 个理由](https://towardsdatascience.com/5-reasons-why-you-should-begin-your-data-science-journey-in-2020-2b4a0a5e4239)

[数据科学的理论基础——我应该关心还是仅仅关注实践技能？](https://towardsdatascience.com/theoretical-foundations-of-data-science-should-i-care-or-simply-focus-on-hands-on-skills-c53fb0caba66)

[机器学习项目规划](https://towardsdatascience.com/machine-learning-project-planning-71bdb3a44349)

[如何组织你的数据科学项目](https://towardsdatascience.com/how-to-organize-your-data-science-project-dd6599cf000a)

[大型数据科学项目的生产力工具](https://medium.com/towards-artificial-intelligence/productivity-tools-for-large-scale-data-science-projects-64810dfbb971)

[数据科学作品集比简历更有价值](https://towardsdatascience.com/a-data-science-portfolio-is-more-valuable-than-a-resume-2d031d6ce518)

[使用协方差矩阵图进行特征选择和降维](https://medium.com/towards-artificial-intelligence/feature-selection-and-dimensionality-reduction-using-covariance-matrix-plot-b4c7498abd07)

[数据科学 101 —包含 R 和 Python 代码的中型平台短期课程](https://medium.com/towards-artificial-intelligence/data-science-101-a-short-course-on-medium-platform-with-r-and-python-code-included-3cdc9d489c6d)

***如有疑问，请发邮件给我***:benjaminobi@gmail.com