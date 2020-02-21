---
layout:     post   				    # 使用的布局（不需要改）
title:      transformer-Xl阅读笔记 				# 标题 
subtitle:   transformer-Xl #副标题
date:       2020-02-21 				# 时间
author:     BY 黄梓林						# 作者
header-img: img/post-bg-2015.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - 机器学习
    - 机器阅读理解
---


## Model

In order to apply Transformer or self-attention tovlanguage modeling, the central problem is how to
train a Transformer to effectively encode an arbitrarily long context into a fixed size representation.

### Vanilla Transformer Language Models

做法： 

split the entire corpus into shorter segments of manageable sizes, 
and only train the model within each segment, 
ignoring all contextual information from previous segments. 

将文本分成大小相同的段，放进模型中训练，忽略上下文之间的联系

问题：

* the largest possible dependency length is upper bounded by the segment length, 
the vanilla model is not able to fully exploit this(transformer) optimization advantage. 

最长的可能依赖长度取决于段长，且无法发挥 transformer 的优化特长

* simply chunking a sequence into fixed-length segments will lead to the context fragmentation problem 

会导致上下文碎片化问题

* 评估阶段每次只预测一位，右移一位，

此过程可确保每个预测都利用训练过程中暴露的尽可能长的上下文，并且还可以缓解训练中遇到的上下文碎片问题。

但是代价过于昂贵
