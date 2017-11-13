---
title: c++容器技术探究
date: 2017-11-13 09:31:44
tags:
	c++
categories:
	编程语言
---

为了更好的学习c++，搭建自己的知识树，所以决定开辟一个系列专门用来整理和总结自己学习到的知识点。这个系列将按我自己认为正确的方式来组织结构。

## 本章概述
本章主要讨论c++里面的容器技术，容器即一系列特定类型的集合。**顺序容器（sequential container）**提供了控制元素存储和访问顺序的能力。这种顺序不依赖于元素的值，而是与元素加入时的位置相对应。与之相反的是，**关联容器（associative container）**提供基于关键字的元素存储和访问。**容器适配器（container adapter）**是一个比较抽象的概念，提供了一个抽象层，用于封装底层容器的访问方式，做一个接口的转换。

## 顺序容器

容器名称 | 描述 | 实现方式
------|------| ------
vector | 可变大小数组 | 分配连续内存，重新分配时拷贝并销毁原来的内存存储
deque | 双端队列 | 分块的连续内存，性能介于vector和list之间
list | 双向列表 | 链表，内存不连续，插入性能最好，查询效率最差
forward_list | 单向列表 | 单向链表，和list实现一致，但只允许单向访问
array | 固定大小数则 | 连续内存，不支持增加、删除元素
string | 与vector类似，但只保存字符 | 和vector实现一致，只支持存储字符

## 关联容器

容器名称 | 描述 | 实现方式
------|------| ------
map | 映射 | 存储键-值对
set | 集合 | 值既是键值的map
multimap | 多重映射 | 键值可重复出现的map
multiset | 多重集合 | 键值可重复出现的set
unordered_map | 无序映射 | hash组织的map
unordered_set | 无序集合 | hash组织的set
unordered_multimap | 无序多重映射 | hash组织的map，键值可重复出现
unordered_multiset | 无序多重集合 | hash组织的set，键值可重复出现

## 容器适配器

容器名称 | 描述 | 实现方式
------|------| ------
stack | 栈 | 默认使用deque实现，后进先出，需要pop_back方法
queue | 队列 | 默认使用deque实现，先进先出，需要pop_front方法，因此不能使用vector
priority_queue | 优先级 | 默认使用vector，需要随机访问的能力，因此不能使用list


## 总结
未完待续...
