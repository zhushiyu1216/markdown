# 文本格式
本节将介绍常见的文本格式，如粗体、斜体等，Markdown不建议对字体颜色和大小随意设置，这样不便于版本统一，所以markdown是不提供这些设置。不过Markdown兼容HTML，如果确实想这样做，你可能需要学习一下HTML了，这属于Markdown的高级用法了，后面的章节会介绍。

## 换行
Markdown的文本默认是连在一块儿的，我们平时的回车换行，Markdown是不会换行的。Markdown里实现换行有两种方法：

（1）行尾加两个及以上空格，再按回车； 如果需要再换一行，则重复以上操作；注意，最多只能换两行哦。
  
书写如下：  
![空格换行代码](images/text_line_code_whitespace.png)  

显示如下：  
![空格换行代码](images/text_line_graph_whitespace.png)  

（2）使用两个及以上“回车”换行。这个换行方式的行间距会明显高于使用双空格+回车，后面我们再解释原因；注意，这种换行方式，无论你打几个加车也只能换一行。

书写如下：  
![双回车换行](images/text_line_code_return.png)  

显示如下：  
![双回车换行](images/text_line_graph_return.png)  

我们再来说说这两个换行方式的区别，学过HTML的同学应该知道，在HTML中换行用`<br>`，如果要新起一个段落，可以使用`<p></p>`。上边这两种换行方式最终转化为HTML后，“双空格+回车”对应的就是`<br>`，“双回车”对应的就是`<p></p>`，这也为什么“双空格+回车”两个行是紧挨着，而“双回车”起到的是分段的作用，所以间隔会大一些。  
另外，Markdown为了排版效果，不允许我们有连续的换行或换段。

## 字体
Markdown仅支持和粗体和斜体两种字体样式，但两者还可以组合，开成粗斜体，我们分别来看看如何标记这几种字体。

（1）粗体，两边分别使用两个“\*”号夹起来  
书写：`**粗体**`  
显示：**粗体**

（2）斜体，两边分别使用一个“\*”号夹起来  
书写：`*斜体*`  
显示：*斜体*

（3）粗斜体，两边分别使用三个“\*”号夹起来  
书写：`***粗斜体***`  
显示：***粗斜体***

也有教程上说使用中横杠“-”也可以，但在MacDown亲测有一定的兼容性问题，容易显示错，而且在生成gitbook时是不生效的，所以建议还是使用“\*”号。

## 分割线
Markdown的分割线比较随意，只要一行内只有下横杠“\_”或“\*”，且不少于3个就可以表示一个分割线。为了显眼，我们一般会使用比3个多很多的“\_”或“\*”。注意，同一行内不能有其它字符。

写法如下：  

    ***  
    ************************************
    * * * * * * * * * * * * * * * * * *
    ** * * * * * *** * **** * **** ****************
    ___  
    ____________________________
    __ _ __   _ __ ____ ___________   _ _ _ ___

显示如下：  
***  
************************************
* * * * * * * * * * * * * * * * * *
** * * * * * *** * **** * **** ****************
___  
____________________________
__ _ __   _ __ ____ ___________   _ _ _ ___
我们还是建议使用下横杠来写分割线，因为星号已经在粗体中使用了，这里再用容易出现不兼容或者混淆，同时，下线线的确也更像分隔线一些。

## 删除线
删除线也是我们平时经常会遇到的文本格式，语法格式为在要删除的文本两边加上两个“~”波浪线即可。  
写法：`~~我是删除线格式~~`  
显示： ~~我是删除线格式~~

注意，Macdown软件是不支持删除线格式的，所以如果你使用的是Macdown，你是无法使用删除线的，导出的HTML或PDF也没有，但如果你只是用Macdown编辑，最终会上传到某些平台，那是没问题的，上传后会正确显示。

## 下划线
markdown默认语法不支持下划线，要实现下划线功能，需要用HTML。HTML的用法会在后面的章节中讲，不过下划线属于文本格式，且平时用到的比较多，我们在这里提前讲一下。  
HTML的写法要比mardown复杂很多，它同样需要在要设置格式的文本两边对应做一下修饰，不过它的前后两个标签是不一样的，前面用`<u>`，后面用`<u\>`，大小写都可以。  

写法：`<u>我是下划线<u/>`  
显示：<u>我是下划线<u/>

## 脚本注释
如果我们的文章内有很多引用，通常我们是要标明出处的，这时就可以使用脚本注释了，用户点击脚本注释就可以跳转到注释的说明处。一般脚本注释都是放在页底的。说的理直接一些，脚本注释实际上很类似于页内链接，即HTML中的锚点。

脚本注释第一步先定义注释内容，一般放在页底，书写方法为英文中括号，内加上箭头，后加英文冒号，如：  
`[^1]: 我是脚本注释的内容`  
这里的“1”是锚点地址，在脚注的地方要用到。  
使用脚注：  
`是这样创建脚本注释的[^1]`  
这里的“1”就是刚才定义的脚注锚点。  
显示如下：  
是这样创建脚本注释的[^1]

也可以在底部的脚本注释内使用链接，写法为：  
`[^2]: [我是带链接的脚注谙](http://markdown.codebook.cf)`  
使用方法与通常的脚本注释相同：  
`我是带链接的脚本注释[^2]`  
显示如下：  
我是带链接的脚本注释[^2]

## 字体颜色
Markdown不支持设置字体颜色，要想实现颜色设置，需要借助HTML字体语法的支持，HTML字体标签为`<font></font>`，要设置字体颜色，只用将文本放入两个font标签中间，同时设置font标签的color属性即可。

写法如下：  
`<font color="red">我是文本</font>`  
上边的这个实例是将“我是文本”显示为红色。

显示为：  
<font color="red">我是文本</font>

HTML支持16种颜色以英文单词表示，它们是：

+ aqua <font color="aqua">浅绿色</font>
+ red <font color="red">红色</font>
+ yellow <font color="yellow">黄色</font>
+ blue <font color="blue">蓝色</font>
+ green <font color="green">绿色</font>
+ purple <font color="purple">紫色</font>
+ black <font color="black">黑色</font>
+ fuchsia <font color="fuchsia">紫红色</font>
+ gray <font color="gray">灰色</font>
+ lime <font color="lime">绿黄色</font>
+ maroon <font color="maroon">褐红色</font>
+ navy <font color="navy">深蓝色</font>
+ olive <font color="olive">橄榄色</font>
+ silver <font color="silver">银色</font>
+ teal <font color="teal">蓝色色</font>
+ white 白色


______________________

[^1]: 我是脚本注释的内容
[^2]: [我是带链接的脚本注释](http://markdown.codebook.cf)
