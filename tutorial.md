# org-mode 简介

## 列表

常用快捷键：
-   M-RRT 插入同级列表项
-   M-S-RRT 插入有 checkbox的同级列表项
-   C-c C-c 改变 checkbox状态
-   M-left/right 改变列表项层级关系
-   M-up/dowm 上下移动列表项

-   [-] 任务1 <code>[33%]</code>
    1.  [ ] 子任务1
    
    2.  [X] 子任务2
    
    3.  [ ] 子任务3

-   [ ] 任务2

-   treeroot
    -   branch1
    
    -   branch2

## footnote

在中提到了脚注的用法，这个标签是可以点击的

## 表格

创建表格时，首先输入表头：

    input | Name        |  Phone | sub1 | sub2 | total |
    |-

然后按 tab，表格就会自动生成
也可以按 C-c | 然后输入表格大小即可
-   C-c C-c 对齐表格
-   tab 调到右边一个表格
-   enter 跳到下方的表格
-   M-up/right/left/right 上下左右移动行（列）
-   M-S-up/right/left/right 向上下左右插入行（列）
    如果要插入行和列，也可在表头添加一个标签或者新起一行，输入|再调整格式即可。

<table border="2" cellspacing="0" cellpadding="6" rules="groups" frame="hsides">


<colgroup>
<col  class="left" />

<col  class="left" />

<col  class="right" />

<col  class="right" />

<col  class="right" />
</colgroup>
<thead>
<tr>
<th scope="col" class="left">Name</th>
<th scope="col" class="left">Phone</th>
<th scope="col" class="right">sub1</th>
<th scope="col" class="right">sub2</th>
<th scope="col" class="right">total</th>
</tr>
</thead>

<tbody>
<tr>
<td class="left">maple</td>
<td class="left">134&#x2026;</td>
<td class="right">89</td>
<td class="right">98</td>
<td class="right">187</td>
</tr>


<tr>
<td class="left">wizard</td>
<td class="left">152&#x2026;</td>
<td class="right">78</td>
<td class="right">65</td>
<td class="right">143</td>
</tr>


<tr>
<td class="left">Hello World</td>
<td class="left">123&#x2026;</td>
<td class="right">76</td>
<td class="right">87</td>
<td class="right">163</td>
</tr>


<tr>
<td class="left">hehe</td>
<td class="left">157&#x2026;</td>
<td class="right">87</td>
<td class="right">78</td>
<td class="right">165</td>
</tr>
</tbody>
</table>

### 表格计算

在上表中total列中任一行输入 =$3+$4 ，然后按C-u C-c C-c 

## 链接

链接的格式是：

    [[链接地址][链接内容]]

link sample

[[grgguid.pdf](http://orgmode.org/orgguide.pdf)] 

[a picture](file://c:/home/maple/图片/test.jpg)

直接显示图片：

![img](https://i.linuxtoy.org/images/2010/04/emacs-video-thumb.png)

## 待办事项TODO

TODO 是一类标题，需要用\*开头
-   C-c C-t 变换TODO的状态
-   C-c / t 以树的形式展示所有的 TODO
-   C-c , 设置优先级（方括号里的ABC）
-   M-S-RET 插入同级TODO标签

### TODO 任务1

### TODO 任务2

### TODO 总任务 <code>[33%]</code>

1.  TODO 子任务1

2.  TODO 子任务2 <code>[0%]</code>

    -   [-] subsub1 <code>[1/2]</code>
        -   [ ] subsub2
        -   [X] subsub3

3.  DONE 一个已完成的任务

## 标签Tags

子标题的标签会继承父标题标签

### title     :work:learn:

-   C-c C-q 为标题添加标签
-   C-c / m 生成带标签的树

1.  stitle     :fly:plane:

2.  stitle2     :car:run:

## 时间

-   C-c . 插入时间

<span class="timestamp-wrapper"><span class="timestamp">&lt;2015-02-17 二&gt;</span></span>
时间前可以加DEADLINE:和SCHEDULED:表示时间的类型

一个常见的TODO标签：

### TODO 

一些待办事项

## 富文本导出

可以加一些说明符：

> Everything should be made as simple as possible,
> but not any simpler &#x2013; Albert Einstein

<div class="center">
Everything should be made as simple as possible,   
but not any simpler
</div>

    这里面的字符不会被转义

### 一些特殊格式：

**bold**
*italic*
<span class="underline">underlined</span>
`code`
`verbatim`
<del>strike-through</del>

注释的用法# this is comment


在导出后LaTeX能被正确解释

\begin{equation}
\nabla^2 x=\int\Omega \frac{a}{\log{a}h
} \sum^n_{i=1} a_i d\Omega 
\end{equation}

### 插入源代码

org mode的源代码可以直接求出运行结果，需要在.emacsu配置文件中设置加载的运行语言
-   C-c C-c 对当前代码块求值

(org-babel-do-load-languages
 'org-babel-load-languages
 '(
   (sh . t)
   (python . t)
   (R . t)
   (ruby . t)
   (ditaa . t)
   (dot . t)
   (octave . t)
   (sqlite . t)
   (perl . t)
   (C . t)
   ))

    (+ 1 2 3 4)

    a = 1+1
    print a

    int a=1;
    int b=1;
    printf("%d\n", a+b);

### css 文件

### 导出方式

-   C-c C-e 选择相应的导出格式

# 链接地址

<div id="footnotes">
<h2 class="footnotes">Footnotes: </h2>
<div id="text-footnotes">

<div class="footdef"><sup><a id="fn.1" name="fn.1" class="footnum" href="#fnr.1">1</a></sup> 本文参考自<http://orgmode.org/orgguide.pdf></div>


</div>
</div>