---
layout:     post   				    # 使用的布局（不需要改）
title:      tensorflow常用函数 				# 标题 
subtitle:   tf学习 #副标题
date:       2020-02-20 				# 时间
author:     BY 黄梓林						# 作者
header-img: img/post-bg-2015.jpg 	#这篇文章标题背景图片
catalog: true 						# 是否归档
tags:								#标签
    - python
---

## TensorFlow
>代码中遇到的tf函数


tf.variable_scope<br>
tf.get_variable<br>
共享变量<br>
<br>
tf.Session()<br>
Session提供了Operation执行和Tensor求值的环境<br>
<br>
tf.nn.embedding_lookup<br>
主要是选取一个张量里面索引对应的元素<br>
<br>
tf.einsum<br>
进行矩阵运算<br>
<br>
tf.concat<br>
用来拼接张量<br>
<br>
tf.tile<br>
复制张量<br>
<br>
tf.layers.dense<br>
全连接层<br>
<br>
tf.layers.dropout<br>
dropout层<br>
<br>
tf.contrib.layers.layer_norm<br>
tf.nn.softmax<br>
