---
layout: post
title: Python 手记
---

# {{ page.title }}

## Bullet Points
- BIF是python的内置函数
- 模块是一个包含python代码的文本文件。
- with语句会自动处理所有已打开文件的关闭工作，即使出现异常也不例外，with语句也使用as关键字。
- 方法串链(method chaining)可以将多个方法连接到一起生成所需的结果，比如：`str.strip().split(',')`。
- 函数串链(function chaining)所做的事情和方法串联一样，只不过是从右向左读，比如：`print(sorted(list))`。
- 列表是一个数据集合，可以存放任意数据，而且数据可以是混合类型包括其他列表，可以随意伸缩，创建列表时，用中括号预添加数据。
- 列表推导可以减少将一个列表转换为另一个列表时所需要编写的代码，例如：

```python
new_list = []
for each_item in old_list:
    new_list.append(handler(each_item))
# 将上面的列表转换代码用列表推导来简化就是： 
new_list = [handler(each_item) for each_item in old_list]
```
- 集合也是一种列表数据结构，同样可以添加混合类型的数据项，特点是数据项是无序的，而且不允许重复，如果试图添加一个已经存在的数据项，将会被忽略，创建集合时，用大括号预添加数据，可以使用集合来剔除列表中的重复项，如: `new_list = set(old_list)`。

### BIF
- BIF的命名空间是 `__builtins__`。
- print(): 打印一个消息到屏幕，使用file参数可以把消息写入指定文件对象。
- len(): 提供某个数据对象的长度或者统计一个集合的项数。
- isinstance(): 检查一个标识符是否指示某个指定类型的数据对象。
- range(): 可以配合for使用，迭代指定次数。
- open(): 打开一个磁盘文件，创建一个迭代器从文件一次读取一行。
- str(): 访问任何数据对象的串表示。
- locals: 返回当前域中的变量集合。
- sort() / sorted(): 两个函数都是对数据进行排序，不同的是前者是原地排序(改变原数据)，后者是复制排序(复制原数据)。