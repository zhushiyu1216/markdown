# 图片
图片是我们在编辑文章时最常用到的元素之一了。Markdown设计之初主要是供程序员来使用，同时，在Markdown推出的年代，网络上的文章也都是图文为主，所以Markdown的语法主要集中在图文的处理。不过音视频的使用在后边我们也会介绍。  

很多教程会先讲超链接的用法，再讲图片，因为图片跟链接很像。但我觉得图片相对简单一些，同时如果图片要增加超链接，仍然要先学会图片的使用方法，所以我把图片使用放在前面讲。

图片除了普通展示外，还有alt和title的等稍高级一些的用法，接下来会分别进行讲解。

## 添加图片
添加图片的语法稍复杂，不过后面我们介绍了各部分的作用后，理解起来就比较容易了。  
添加图片的语法为：感叹号 + 中括号 + 小括号，小括号内写上图片地址。注意：Markdown的标记符号都是英文。

书写方法：  
`![](https://markdown.codebook.cf/common_syntax/images/markdown.jpg)`

显示为：  
![](https://markdown.codebook.cf/common_syntax/images/markdown.jpg)

## 图片alt替换文本
学过HTML的同学应该都知道图片标签“img”有一个“alt”属性，来标记当指定的url图片不能正常显示时，显示这alt属性的值。alt实际上就是alternative（替换）这个英文单词的简写。  
Markdown图片语法的中间那个中括号就是为了设置alt属性的，我们来测试一下。

书写方法：  
`![图片不存在了](https://markdown.codebook.cf/common_syntax/images/markdown_no.jpg)`

显示为：  
![图片不存在了](https://markdown.codebook.cf/common_syntax/images/markdown_no.jpg)

alt的值显示的情境有以下四种：

+ 网速太慢  
+ src 属性中的错误  
+ 浏览器禁用图像  
+ 用户使用的是屏幕阅读器  

注意，Macdown不显示alt，不过强烈建议还要是把alt写上，这样在比较恶劣的环境下，用户依然可以看到你要表达的内容。

## 图片title
同样，学习过HTML的同学也应该知道，HTML的img标签中还有一个title属性，它的作用是当用户把鼠标放在图片上静止一会儿，图片上会浮出一个文本框显示title属性的内容。Markdown也可以实现这个能力，将title放在图片标记的小括号内，图片地址后，以空间分隔，以英文双引号引起来。

书写方法：  
`![Markdown](https://markdown.codebook.cf/common_syntax/images/markdown.jpg "I love markdown")`

显示为：  
![Markdown](https://markdown.codebook.cf/common_syntax/images/markdown.jpg "I love markdown")

## 关于图片标记前面的感叹号
下一节我们会学习文本超链接，你会发现超链接和图片的用法大体一样，为了区分，所以在图片的标记前加个感叹号。知道这个区别，可以方便大家记忆图片和超链接的使用方法。

## 图片宽高
Markdown不提供图片尺寸的设置，如果想设置图片尺寸，只能用HTML的img标签了。

img标签的用法为：  
`<img src="https://markdown.codebook.cf/common_syntax/images/markdown.jpg" alt="markdown" width="42" height="42">`

属性说明：  

| 属性 | 类型 | 是否必须 | 说明 |
| --- | --- | --- | --- |
| alt | 文本 | 否 | 规定图像的替代文本 |
| title | 文本 | 否 | 规定元素的工具提示文本（tooltip text）|
| width | 数字 | 否 | 图片宽度，单位为象素 |
| height | 数字 | 否 | 图片高度，单位为象素 |

HTML标签的各属性要用双引号引起来。

上边的代码显示为：  
<img src="https://markdown.codebook.cf/common_syntax/images/markdown.jpg" alt="markdown" width="42" height="42">

## 图片链接
下一节我们会讲链接的用法，图片链接放在超链接一节中讲。 点击查看[图片链接用法](link.md)。