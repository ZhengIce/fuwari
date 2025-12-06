---
title: Markdown 示例
published: 2023-10-01
description: 一篇简单的 Markdown 博客文章示例。
tags: [Markdown, 博客, 演示]
category: 示例
draft: true
---

# h1 标题

段落之间用空行分隔。

第二段。_斜体_，**粗体**，和 `等宽字体`。项目列表看起来像这样：

- 这一个
- 那一个
- 另一个

请注意，不考虑星号的话，实际文本内容从第 4 列开始。

> 块引用是
> 这样写的。
>
> 如果你愿意，它们可以跨多个段落。

使用 3 个破折号表示 em-dash（长破折号）。使用 2 个破折号表示范围（例如，"全部在第 12--14 章"）。三个点 ... 将被转换为省略号。支持 Unicode。☺

## h2 标题

这是一个编号列表：

1. 第一个项目
2. 第二个项目
3. 第三个项目

再次注意，实际文本如何从左侧 4 列（4 个字符）开始。这是一个代码示例：

    # 让我重申一下 ...
    for i in 1 .. 10 { do-something(i) }

正如你可能猜到的，缩进了 4 个空格。顺便说一下，你可以使用分隔块代替缩进块：

```
define foobar() {
    print "Welcome to flavor country!";
}
```

（这使得复制和粘贴更容易）。你可以选择标记分隔块，让 Pandoc 为其语法高亮：

```python
import time
# 快速，数到十！
for i in range(10):
    # （但不要太快）
    time.sleep(0.5)
    print i
```

### h3 标题

现在是嵌套列表：

1. 首先，准备这些食材：

    - 胡萝卜
    - 芹菜
    - 扁豆

2. 烧一些水。

3. 把所有东西倒进锅里，然后按照这个算法操作：

        找到木勺
        揭开锅盖
        搅拌
        盖上锅盖
        把木勺摇摇晃晃地放在锅柄上
        等待 10 分钟
        回到第一步（或完成时关火）

    不要撞到木勺，否则它会掉下来。

再次注意，文本总是在 4 个空格的缩进上对齐（包括上面第 3 项的最后一行）。

这是一个指向 [网站](http://foo.bar) 的链接，指向 [本地文档](local-doc.html)，以及指向当前文档中 [章节标题](#an-h2-header) 的链接。这是一个脚注 [^1]。

[^1]: 脚注文本在这里。

表格可以像这样：

size material color

---

9 leather brown
10 hemp canvas natural
11 glass transparent

Table: Shoes, their sizes, and what they're made of

（以上是表格的标题）。Pandoc 还支持多行表格：

---

keyword text

---

red Sunsets, apples, and
other red or reddish
things.

green Leaves, grass, frogs
and other things it's
not easy being.

---

下面是一条水平线。

---

这是一个定义列表：

apples
: 适合做苹果酱。
oranges
: 柑橘类水果！
tomatoes
: tomato 里没有 "e"。

同样，文本缩进 4 个空格。（在每个术语/定义对之间放一个空行可以使内容更分散。）

这是一个 "行块"：

| Line one
| Line too
| Line tree

图像可以这样指定：

[//]: # (![example image]&#40;./demo-banner.png "An exemplary image"&#41;)

内联数学公式是这样的：$\omega = d\phi / dt$。显示数学公式应该有自己的行，并放在双美元符号中：

$$I = \int \rho R^{2} dV$$

$$
\begin{equation*}
\pi
=3.1415926535
 \;8979323846\;2643383279\;5028841971\;6939937510\;5820974944
 \;5923078164\;0628620899\;8628034825\;3421170679\;\ldots
\end{equation*}
$$

请注意，你可以反斜杠转义任何你希望按字面显示的标点符号，例如：\`foo\`，\*bar\* 等。
