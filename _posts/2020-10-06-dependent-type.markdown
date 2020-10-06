---
layout: post
title:  "Dependent Type 太难了"
categories: jekyll update
---

{% include latex.html %}

### SymbolType

一开始我是主张不需要类型的，Python 不需要指定类型。

随着系统的推进，符号类型(SymbolType)自然而然的出现了。

比如化简，$$a*b - b*a = 0$$，这里须有假设 $$a, b$$ 为标量，换成矩阵向量就错了。

所以，符号类型引入为好。

为什么 Python 不需要？区别在于我的系统引入了抽象，类型是对抽象的刻画。

### Propositions as Types

什么是类型？一种观点是命题即类型。

我之前也想过，类型和属性有没有区别。以这种观点，类型，命题，属性，是同一的。

目前我持保守的观点，类型是特殊的属性。能决定函数运算法则的属性称为类型。

比如标量，向量，矩阵，就能决定乘法的运算法则。

顺着这个思路，凡是函数的输入都需要有类型，从而函数也需要有类型。

### dependent type

函数有重载，类型不好刻画。

比如乘法，至少有 

$$\mathrm{Scalar}\times \mathrm{Scalar}\rightarrow \mathrm{Scalar}, \mathrm{Scalar}\times \mathrm{Vector}\rightarrow \mathrm{Vector}, \mathrm{Scalar}\times \mathrm{Matrix}\rightarrow \mathrm{Matrix}, \ldots$$

想要借助 dependent type，看不懂。进一步深入，一大堆名词涌入，lambda calculus, simply typed lambda calculus, lambda cube, Haskell, Idris...

### functional programming

没想到的是这些理论全是函数式编程的基础。

入行这么久，才稍微理解了面对象编程的妙处（即数据先于过程，对象先于方法，对应数学里定义先于陈述，概念先于定理），完全没想到函数式编程似乎和逻辑推理有更先天的联系。

越发觉得程序，逻辑和数学在本质上的同源。

### OOP + FP

嗯，本来看这些不熟悉的理论是很头疼的，一大堆定义和公式，不知道什么时候能弄懂，更不知道什么时候能为己所用。

这个时候，看到一条评论：

>
总算从 fortran 换到 C++ 写了好几个 class，“我正在使用 OOP 语言编程，真是棒极了”
>
在 javascript 里写了个高阶函数（比如 map），“我正在使用函数式编程”

笑哭，于是有了发状态的念头。

希望早日和这位仁兄一样，精通 OOP + FP.

