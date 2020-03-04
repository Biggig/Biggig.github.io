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
tf.gfile.ListDirectory<br>
罗列dirname目录下的所有文件并以列表形式返回，dirname必须是目录名。<br>
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
Layer Normalization 针对一个样本各个维度的输出值进行归一化<br>
经过归一化再输入激活函数，得到的值大部分会落入非线性函数的线性区，导数远离导数饱和区，避免了梯度消失，这样来加速训练收敛过程。<br>
<br>
tf.nn.softmax<br>
用于计算在多个分类上的概率,可以在不同的维度上进行softmax<br>
<br>
tf.train.BytesList等<br>
tf.train.Feature<br>
tf.train.Features<br>
tf.train.Example<br>
将数据转为二进制格式，bin文件<br>
<br>
