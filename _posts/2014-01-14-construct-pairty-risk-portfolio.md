---
layout: post
title: 说说风险均摊投资组合的构建方法
comments: true
categories:
- life
tags:
- 风险均摊
- 投资组合
- R
---
 
我们在筛选出备选股票之后，要解决的另外一个问题是确定备选股票在投资组合中的权重向量：

$$ w=\( w_1,w_2,...,w_n \) $$

其中，$ 0<w_{i}< 1,i=1,2,...,n $。

权重的可选集是个无限集合，我们要选取其中最优的一个作为目标权重，怎么判断最优与否？那得首先确定一个判断最优与否的方法或者说函数。常用的方法是收益-风险法，即如果一个权重能够使投资组合的收益最大，风险最小，那么它就是好的。如果用标准差来刻画风险，那么，就有评价函数:

$$ U(R,\sigma) $$

其中，$ \frac{\partial U(\cdot )}{\partial R} > 0 $，$ \frac{\partial U(\cdot )}{\partial \sigma} < 0 $。

$ U(\cdot) $最简单的形式如下：

$$
U_p = aR_{p} + b \sigma \_{p}
$$

其中，$ a > 0 $，$ b < 0 $；$ R_p是组合的收益率，$\sigma \_{p} $是组合的标准差。显然：

$$
R_p = w'R 


\sigma \_p = w'Rw
$$

当然，也有其它理念，比如，这里说的风险均摊。它是指我们要选出来这样一个权重，这个权重确定的投资组合中，各个证券的风险占证券投资总的风险的比例是相同的。其原理如下：



