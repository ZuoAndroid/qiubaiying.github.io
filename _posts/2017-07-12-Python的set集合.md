---
layout:     post
title:      Python中的set集合
subtitle:   set操作
date:       2017-07-12
author:     Sasuke
header-img: img/post-bg-github-cup.jpg
catalog: 	 true
tags:
    - 集合
    - set
---

### **Python的set集合**

set集合，在Python中的书写方式的{}，集合与之前列表、元组类似，可以存储多个数据，但是这些数据是不重复的

集合对象还支持union(联合), intersection(交), difference(差)和sysmmetric_difference(对称差集)等数学运算.

#### **快速去除列表中的重复元素**

```Python
In [4]: a = [11,22,33,33,44,22,55]

In [5]: set(a)
Out[5]: {11, 22, 33, 44, 55}

```

#### **交集：共有的部分**

```python
In [7]: a = {11,22,33,44,55}

In [8]: b = {22,44,55,66,77}

In [9]: a&b
Out[9]: {22, 44, 55}

```

#### **并集：总共的部分**

```python
In [11]: a = {11,22,33,44,55}

In [12]: b = {22,44,55,66,77}

In [13]: a | b
Out[13]: {11, 22, 33, 44, 55, 66, 77}

```

#### **差集：另一个集合中没有的部分**

```python
In [15]: a = {11,22,33,44,55}

In [16]: b = {22,44,55,66,77}

In [17]: b - a
Out[17]: {66, 77}

```

#### 对称差集(在a或b中，但不会同时出现在二者中)

```python
In [19]: a = {11,22,33,44,55}

In [20]: b = {22,44,55,66,77}

In [21]: a ^ b
Out[21]: {11, 33, 66, 77}
```