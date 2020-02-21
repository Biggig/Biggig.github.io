---
layout:     post   				    # 使用的布局（不需要改）
title:      attention is all you need阅读笔记 				# 标题 
subtitle:   attention is all you need #副标题
date:       2020-02-21 				# 时间
author:     BY 黄梓林						# 作者
header-img: img/post-bg-2015.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - 机器学习
    - 机器阅读理解
---

## transformer结构

![transformer](/img/a9fak-y4zyr.jpg)

transformer 由 encoder 以及 decoder 组成

### encoder

    encoder 由6层完全相同的结构组成，每层包括两部分：

a multi-head self-attention mechanism + positionwise fully connected feed-forward network

    因为每层的输出都要进行残差连接 (residual connection) ，所以每层最后的输出为 LayerNorm(x + Sublayer(x))，维度为512
