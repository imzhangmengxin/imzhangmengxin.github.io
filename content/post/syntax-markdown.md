---
title: "Syntax-Markdown"
date: 2017-03-04T21:57:45+08:00
lastmod: 2017-09-30T01:37:56+08:00
update: 2018-01-10T07:37:56+08:00
draft: false
tags: ["Markdown","Syntax"]
categories: ["Documents"]
hiddenFromHomePage: false
---



## 1.标题

# H1
## H2
### H3
#### H4
##### H5
###### H6

## 2. 段落

使用单星号 `*` 或者单下划线 `_` 标记 *斜体强调* 或者 _斜体强调_

使用两个星号 `**` 或者两个下划线 `__` 标记 **加粗强调** 或者 __加粗强调__

引号和下划线可叠加使用 → **只是加粗 _斜体并加粗_**

使用两个波浪线 `~~` 标记 ~~已删除文字~~

行内代码使用反引号: \` 标记 →`print("hello world")`

填充文字暂无 `Markdown` 标记，直接使用 `HTML` 标签 `<ins></ins>` 标记 <ins>填充文字</ins>

使用`<sup></sup>` 上标 X<sup>2</sup> /  `<sub></sub>` 下标 X<sub>2</sub>

使用`<kbd></kbd>`按键 <kbd>Alt</kbd>

外链 [I'm ZMX Blog](https://www.imzmx.win)

页面内段落 [引用](#section-05)

*Notice：你可以通过 `{#section-id}` 方式自定义段落锚点*

参考资料 <sup>[[1]](#ref01)</sup><sup>[[2]](#ref02)</sup>

## 3. 列表

以下的无序、有序和任务列表均支持二级嵌套，不建议使用二级以上嵌套。

### 3.1 无序列表

* 无序列表
  - 嵌套的无序列表
  - 嵌套的无序列表
  - 嵌套的无序列表
* 无序列表
  1. 嵌套的有序列表
  1. 嵌套的有序列表
  1. 嵌套的有序列表
* 无序列表
  + 嵌套的无序列表
  + 嵌套的无序列表
  + 嵌套的无序列表

### 3.2 有序列表

1. 有序列表
  1. 嵌套的有序列表
  1. 嵌套的有序列表
  1. 嵌套的有序列表
1. 有序列表
  - 嵌套的无序列表
  - 嵌套的无序列表
  - 嵌套的无序列表
1. 有序列表
  + 嵌套的无序列表
  + 嵌套的无序列表
  + 嵌套的无序列表

### 3.3 定义列表

CSS
: 层叠样式表

### 3.4 任务列表

- [ ] 个人blog迁移
  - [x] blog引擎选择
  - [x] 主题选择
  - [x] 框架适配
  - [ ] 一些错误修正
  - [ ] 主要博文转换迁移
  - [ ] 其他迁移
- [ ] 六月学习计划
  - [ ] 概率论数理统计基础回顾
  - [ ] 数据处理语言工具熟悉
  - [x] 相关工具安装

## 4. 引用 {#section-05}

> 苟日新，日日新，又日新。
>
> <cite>-- 商成汤《盘铭》</cite>

## 5. 代码

以本站的一段 `python` 代码做演示。

```python
# -*- coding: utf-8 -*-
#!/usr/bin/env python
def triangles():
    L = [1]
    while True:
        yield L
        L.append(0)
        L = [L[i - 1] + L[i] for i in range(len(L))]
```

## 6. 分割线

---


## 7. 图片 

不带标题的图片，如下图👇

![数据架构图](https://static.oschina.net/uploads/space/2017/0917/230003_krQT_2421622.png "datauml.png")

带标题的图片，如下图👇

{{% figure class="center" src="https://static.oschina.net/uploads/space/2017/0917/230003_krQT_2421622.png" alt="datum" title="数据架构图" %}}

## 8. 表格

使用 `Markdown` 画的表格，如下表👇

| Tables        | Are           | Cool  |
| :------------ |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

## 9. 数学公式

主题使用了 [MathJax](https://www.mathjax.org/) 开源库来实现对数学公式的支持，使用 `$$` 标记。

$$ \sum_{i=1}^n \frac{1}{i^2} $$

## 10. 网易云音乐

主题文章中可以轻松插入 [网易云音乐](https://music.163.com/) 的指定音乐，你可以根据需要将音乐设置为自动播放，在主题目录 `layouts/shortcodes` 文件夹下的 `music.html` 对该标签进行定义。

{{% music "26883589" %}}

## 11. YouTube

由于不明原因可能无法播放。

{{% youtube "zz-H7G3Zi5c" %}}




## 参考资料

1. <a id="ref01">[Markdown wikipedia](https://en.wikipedia.org/wiki/Markdown)</a>
2. <a id="ref02">[Markdown 语法手册](https://daringfireball.net/projects/markdown/syntax)</a>