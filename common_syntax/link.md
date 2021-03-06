# 超链接
在网上写文章，是离不开超链接的，超链接不仅仅是简单的点击后跳转，它还有不少小技巧在里面的，比如链接title、锚点、链接复用等。

## 普通文本超链接
Markdown添加普通超链比较简单，将要设置超链接的部分用英文中括号括起来，紧接着使用英文小括号将链接地址括起来就可以了。

写法如下：

    我是超链接，[点击我](http://markdown.codebook.cf)
    
显示为：

我是超链接，[点击我](http://markdown.codebook.cf)

细心的人或者前端程序员都知道，很多链接文字，当鼠标放上去静止一会儿（约2秒），会在鼠标旁边显示更长的一段说明文字，鼠标移开后就消失了。这个文字叫做链接title。Markdown的链接标题只用在链接地址后加一个空格，然后用英文双引号将提示文字引起来就可以。

写法如下：

     我是超链接，[点击我](http://markdown.codebook.cf "Markdown专业教程")
     
显示如下：

我是超链接，[点击我](http://markdown.codebook.cf "Markdown专业教程")

## 图片超链接
写图片超链接前，你要先知道如何添加图片，不会的同学可以[点击我](image.md)去学习。  
图片超链接其实很简单，只用将普通文本超链接的文本改成图片的写如即可，写法如下：

    [![Markdown](images/markdown.jpg)](http://markdown.codebook.cf)
    
显示如下：

[![Markdown](images/markdown.jpg)](http://markdown.codebook.cf)  

## 自动链接
当我们在文章内显示一个网址时，希望这个网址可以加上链接，让用户点击后直接跳转。可以使用上面的普通文本超链接的形式，但网址需要写两次，难免有点复杂。Markdown提供了自动链接的方法，只要把你希望跳转的网址使用尖括号括起来，它自动会变成链接地址。

写法如下：  
`<http://markdown.codebook.cf>`

显示如下：  
<http://markdown.codebook.cf>

注意，由于自动链接语法相对简单，所以不能为链接添加title。


### 视频教程
<iframe src="//player.bilibili.com/player.html?aid=287067101&bvid=BV19f4y1S7qh&cid=235816428&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width="800" height="600"> </iframe>

## 锚点
写过HTML网页的人对锚点这个概念都不会陌生，锚点就是在网页内跳转，比如，当一个页面内容很多时，用户看一部分内容，其它内容已经无法在同一屏幕内展示了，这时，如果你想链接到文章别的部分，就可以使用锚点，用户点击后屏幕直接滑动到你设置锚点的位置。

Markdown只支持在标题上设置锚点，你标题名称就是锚点名，设置跳转链接时只用在标题内容前加上#号即可，如：  
`[跳转](#anchor)`

有很多Markdown编辑器都不支持锚点，如Macdown就不行，但不用担心，当发布成笔记或博文后，一般平台都是支持的。

本节的内容就比较多，我们在“普通文本超链接”标题上加个锚点：  
`跳转到[普通文本超链接](#普通文本超链接)`

效果如下：  
跳转到[普通文本超链接](#普通文本超链接)

## 链接复用
链接复用在我们平时编辑过程中用到的比较少，不过当你的文档中有大量重复的链接时，使用它会让你的修改变的非常方便。你可以把要在多处使用的链接统一定义在页面底部，并给各个链接起一个名字，使用链接的地方直接使用这个名字来代替链接地址。这样当需要修改链接时，只修改定义的地方即可。

定义方法也比较简单，将链接名称用英文中括号括起来，后面跟上一个冒号和一个空格，再后面跟上要定义链接地址即可。  
定义方法如下：    
`[markdown]: http://markdown.codebook.cf`

使用链接的地方，小括号及其内部的链接地址换成中括号和链接名称，写法如下：  
`点击[打开教程][markdown]`

显示如下：  
点击[打开教程][markdown]

## 在新窗口打开链接
很多时候，我们设置了链接，但不希望用户直接在本窗口打开链接，这样会把我们当前文档覆盖掉，而是希望用户在一个新窗口内查看。Markdown本身的语法并没有对此做很好的支持，我们需要找其它方法实现。有两种方法可以实现。

一、通过HTML代码来实现  
HTML的链接支持比Markdown丰富，但书写起来会稍繁琐一些，大家先看一下怎么写：  
`<a href="http://markdown.codebook.cf" target="_blank">Markdown教程</a>`

HTML使用a标签来定义链接，标签的href属性定义链接地址，两个a标签内的部分为链接文本。a的另一个属性target可以定义打开的窗口，设置为“_blank”时，可以使用新窗口打开。

上面的代码效果如下：  
<a href="http://markdown.codebook.cf" target="_blank">Markdown教程</a>

二、另一个方法是仍然通过Markdown语法来实现，在已有链接格式后面增加target属性，写法如下：  
`[Markdown教程](http://markdown.codebook.cf){:target="_blank"}`  
通过一对大括号，内以冒号开头，后面加上target属性，属性值仍然是"_blank"。

效果如下：  
[Markdown教程](http://markdown.codebook.cf){target="_blank"}  

注意，这个实现方法很多Markdown编辑器是不支持的，如Macdown就不支持，我们可以在博客等平台上发布后看效果是否正确，笔者使用的docsify就不支持此方法。


[markdown]: http://markdown.codebook.cf


### 视频教程
<iframe src="//player.bilibili.com/player.html?aid=287067101&bvid=BV19f4y1S7qh&cid=235816428&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width="800" height="600"> </iframe>

[打赏](../include/donate.md ':include')