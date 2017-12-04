# 【David Sliver强化学习公开课之四、五】Model-Free prediction and Control-学习笔记

本次笔记来记录两次课程学习的内容，这两次课讲解的都是强化学习中无模型的问题，第三节课中描述的是强化学习中有模型的情况下的planning如何用动态规划的思想去解决。我理解的是在现实生活中，大多数的时候我们碰到的都是无模型的情况。公开课中的第四、五讲分别就无模型情况下的prediction（策略评估），control（策略迭代）问题进行了总结。

## 1. 无模型下的策略评估

### 1.1 Monte-Carlo Learning

首先我们定义一个叫做episode的概念，在强化学习中，将从某个起始状态开始执行到终止状态的一次遍历$S_1, A_1, S_2, ... , S_k$ 称为episode。蒙特卡洛的思想就是通过无穷多次的尝试，认为每个状态的值函数是在无穷多次的尝试下得到的平均值。每次尝试都必须是一个episode，即从初始状态执行到终止状态。而平均的方式又可以分为两种：every-episode 和 every-visit。

### 1.2 Temporal-Difference Learning

## 2. 无模型下的策略迭代

这一节主要是在第四章介绍了Model-free的对策略的评估的基础上，来介绍在model-free的情况下如何对策略进行改进，将这种策略的改进分为两种方法：on-policy learning 以及 off-policy learning.这两种学习的主演区别在于