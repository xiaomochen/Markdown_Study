# Markdown 学习笔记

## 标题

-----

### 实现方法一：
```
使用 多个相连的 "="（最高阶标题） 或者 "-"（第二阶标题）

This is an H1
=============

This is an H2
-------------
```
This is an H1
=============

This is an H2
-------------

-----


### 实现方法二：

```
使用 1~6个＃ 来实现 H1~H6

# 这是 H1

## 这是 H2

###### 这是 H6
```

# 这是 H1

## 这是 H2

###### 这是 H6

-----

## 区块引用

> 使用 ">" 符号来表现

-----

### 标准的 每一行都加上 ">"：
```
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

```
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
> consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
> Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.
>
> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
> id sem consectetuer libero luctus adipiscing.

-----


### 偷懒的 在段落的第一段 加上 ">" ：
```

> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
id sem consectetuer libero luctus adipiscing.

```
> This is a blockquote with two paragraphs. Lorem ipsum dolor sit amet,
consectetuer adipiscing elit. Aliquam hendrerit mi posuere lectus.
Vestibulum enim wisi, viverra nec, fringilla in, laoreet vitae, risus.

> Donec sit amet nisl. Aliquam semper ipsum sit amet velit. Suspendisse
id sem consectetuer libero luctus adipiscing.

-----

### 区块引用可以嵌套（例如：引用内的引用），只要根据层次加上不同数量的 > ：
```
> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.

```

> This is the first level of quoting.
>
> > This is nested blockquote.
>
> Back to the first level.

-----

### 引用的区块内也可以使用其他的 Markdown 语法，包括标题、列表、代码区块等：

```
> ## 这是一个标题。
>
> 1.   这是第一行列表项。
> 2.   这是第二行列表项。
>
> 给出一些例子代码：
>
>     return shell_exec("echo $input | $markdown_script");
```

> ## 这是一个标题。
>
> 1.   这是第一行列表项。
> 2.   这是第二行列表项。
>
> 给出一些例子代码：
>
>     return shell_exec("echo $input | $markdown_script");

-----

## 列表
### 无序列表使用星号、加号或是减号作为列表标记：

```
*   Red
*   Green
*   Blue
```
*   Red
*   Green
*   Blue

#### 等同于：

```
+   Red
+   Green
+   Blue
```
+   Red
+   Green
+   Blue

#### 也等同于：

```
-   Red
-   Green
-   Blue
```
-   Red
-   Green
-   Blue

-----

### 有序列表则使用数字接着一个英文句点：
```
1.  Bird
2.  McHale
3.  Parish
```
1.  Bird
2.  McHale
3.  Parish

-----

#### 你输入的数字 不会影响 Markdown 的表现结果：
```
3. Bird
1. McHale
8. Parish
```
3. Bird
1. McHale
8. Parish

-----

#### 要让列表看起来更漂亮，你可以把内容用固定的缩进整理好：
```
*   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
*   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.
```

*   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
    Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
    viverra nec, fringilla in, laoreet vitae, risus.
*   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
    Suspendisse id sem consectetuer libero luctus adipiscing.

-----

#### 但是如果你懒，那也行：
```
*   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
viverra nec, fringilla in, laoreet vitae, risus.
*   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
Suspendisse id sem consectetuer libero luctus adipiscing.
```

*   Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
Aliquam hendrerit mi posuere lectus. Vestibulum enim wisi,
viverra nec, fringilla in, laoreet vitae, risus.
*   Donec sit amet nisl. Aliquam semper ipsum sit amet velit.
Suspendisse id sem consectetuer libero luctus adipiscing.
-----

#### 如果要在列表项目内放进引用，那 > 就需要缩进：
```
*   A list item with a blockquote:

    > This is a blockquote
    > inside a list item.
```
*   A list item with a blockquote:

    > This is a blockquote
    > inside a list item.

-----

#### 如果要放代码区块的话，该区块就需要缩进两次，也就是 8 个空格或是 2 个制表符：
```
*   一列表项包含一个列表区块：

        <代码写在这>
```
*   一列表项包含一个列表区块：

        Hello World


#### 当然，项目列表很可能会不小心产生，像是下面这样的写法：
```
1986. What a great season.
```
#### 换句话说，也就是在行首出现数字-句点-空白，要避免这样的状况，你可以在句点前面加上反斜杠。
```
1986\. What a great season.
```
-----


### 代码区块

#### 要在 Markdown 中建立代码区块很简单，只要简单地缩进 4 个空格或是 1 个制表符就可以，例如，下面的输入：
```
这是一个普通段落：

    这是一个代码区块。
```
这是一个普通段落：

    这是一个代码区块。
#### Markdown 会转换成：
```
<p>这是一个普通段落：</p>

<pre><code>这是一个代码区块。
</code></pre>
```

-----

### 分隔线

#### 你可以在一行中用三个以上的星号、减号、底线来建立一个分隔线，行内不能有其他东西。你也可以在星号或是减号中间插入空格。下面每种写法都可以建立分隔线：
```
* * *

***

*****

- - -

---------------------------------------
```

* * *

***

*****

- - -

---------------------------------------


## 链接

### 行内链接

#### 要建立一个行内式的链接，只要在方块括号后面紧接着圆括号并插入网址链接即可，如果你还想要加上链接的 title 文字，只要在网址后面，用双引号把 title 文字包起来即可，例如：
```
This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.
```

This is [an example](http://example.com/ "Title") inline link.

[This link](http://example.net/) has no title attribute.
-----


### 参考式链接
#### 链接的定义可以放在文件中的任何一个地方，我比较偏好直接放在链接出现段落的后面，你也可以把它放在文件最后面，就像是注解一样。
```
I get 10 times more traffic from [Google] [1] than from
[Yahoo] [2] or [MSN] [3].

  [1]: http://google.com/        "Google"
  [2]: http://search.yahoo.com/  "Yahoo Search"
  [3]: http://search.msn.com/    "MSN Search"
```
I get 10 times more traffic from [Google] [1] than from
[Yahoo] [2] or [MSN] [3].

  [1]: http://google.com/        "Google"
  [2]: http://search.yahoo.com/  "Yahoo Search"
  [3]: http://search.msn.com/    "MSN Search"

#### 如果改成用链接名称的方式写：
```
I get 10 times more traffic from [Google][] than from
[Yahoo][] or [MSN][].

  [google]: http://google.com/        "Google"
  [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
  [msn]:    http://search.msn.com/    "MSN Search"
```
I get 10 times more traffic from [Google][] than from
[Yahoo][] or [MSN][].

  [google]: http://google.com/        "Google"
  [yahoo]:  http://search.yahoo.com/  "Yahoo Search"
  [msn]:    http://search.msn.com/    "MSN Search"


-----

## 强调
> Markdown 使用星号（\*）和底线（\_）作为标记强调字词的符号，被 * 或 _ 包围的字词会被转成用 <em> 标签包围，用两个 * 或 _ 包起来的话，则会被转成 &lt;strong&gt;

```
*single asterisks*

_single underscores_

**double asterisks**

__double underscores__

```

*single asterisks*

_single underscores_

**double asterisks**

__double underscores__

-----

## 代码
### 使用 "\`" 包裹
```
Use the `printf()` function.
```
Use the `printf()` function.

-----


## 图片

### 详细叙述如下：
```
    一个惊叹号 !
    接着一个方括号，里面放上图片的替代文字
    接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上 选择性的 'title' 文字。
```


### 行内式

```
![Alt text](https://p.ssl.qhimg.com/dmsmty/148_148_100/t010ec017a8cce0e42e.jpg)

![Alt text](https://p.ssl.qhimg.com/dmsmty/148_148_100/t010ec017a8cce0e42e.jpg "Optional title")
```

![Alt text](https://p.ssl.qhimg.com/dmsmty/148_148_100/t010ec017a8cce0e42e.jpg)

![Alt text](https://p.ssl.qhimg.com/dmsmty/148_148_100/t010ec017a8cce0e42e.jpg "Optional title")

-----

### 参考式
```
![Alt text][id]
[id]: https://p.ssl.qhimg.com/dmsmty/148_148_100/t010ec017a8cce0e42e.jpg  "Optional title attribute"
```
![Alt text][id]
[id]: https://p.ssl.qhimg.com/dmsmty/148_148_100/t010ec017a8cce0e42e.jpg  "Optional title attribute"

-----
