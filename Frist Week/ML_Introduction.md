# ML Introduction

## What is Machine Learning?

combine another course [MIT Mathematics of Big Data and Machine Learning](https://ocw.mit.edu/resources/res-ll-005-mathematics-of-big-data-and-machine-learning-january-iap-2020/class-videos/index.htm) to make a summary.

数据是描述ML的一个根本，抛开数学去进行ML会云里雾里，程序的设计最后都是为了实现某一个公式，这也是ML的学习脱离不开数学的缘由。

ML Deep Neural Network: Neural → language → vision → game

「What」There are two definitions:

1. "the field of study that gives computers the ability to learn without being explicitly programmed."——Arthur Samuel
2. "A computer program is said to learn from experience E with respect to some class of tasks T and performance measure P, if its performance at tasks in T, as measured by P, improves with experience E."——Tom Mitchell

The first definition is older, informal, but the other one is more modern, It's a little hard to understand. 

By that example: Input more E -> Performance of T rise up

> E = Watching you label emails as spam or not spam
>
> T = Classifying emails as spam or not spam
>
> P = The number of emails correctly classified as spam/ not spam

In general, any machine learning problem can be assigned to one of two broad classifications:

**Supervised learning** and **Unsupervised learning**.（监督学习和非监督学习，ML算法的两大类型）

- Supervised learning: teach the computer how to do something(参数/非参数算法，支持向量机，核函数，神经网络)
- Unsupervised learning: let it learn by itself(聚类，降维，推荐系统，深入学习推荐)

 Others: Reinforcement learning, recommender systems（RL，[强化学习](https://zh.wikipedia.org/wiki/%E5%BC%BA%E5%8C%96%E5%AD%A6%E4%B9%A0)ML的一个分支）

### Supervised Learning

 **Regression problem(linearity):** predict the sort of continuous values attribute.

**Classification problem(discreteness):** predict a discrete value output zero or one(more than two results, just can describe a state)

Example：

1. Regression - Given a picture of a person, we have to predict their age on the basis of the given picture
2. Classification - Given a patient with a tumor, we have to predict whether the tumor is malignant or benign. 

### Unsupervised Learning

> Unsupervised learning allows us to approach problems with little or no idea what our results should look like. We can derive structure from data where we don't necessarily know the effect of the variables.

In Unsupervised learning, The data set have not any labels or that has same label or really no labels. We should derive this structure by clustering the data based on relationships among the variables in the data.

Example: Market segmentation, group your customers into different market segments so that you can efficiently sell or market.

Python can use less lines of code, this is why ML use Python to program. 
