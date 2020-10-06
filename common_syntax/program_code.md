# 代码块
如果你写的是编程相关的文章，那代码块的使用方法就是你必须要掌握的技能了，Markdown为支持不同的代码展示需求，也给出了多种使用代码块儿的方法。

## 普通代码块
如果你只是要展示一段代码，目的仅为了也突出显示它的代码格式而已，则可以使用普通代码块。这个教程中展示的Markdown代码使用的都是这种格式。普通代码块儿使用四个空格开头就可以了，注意，普通代码块儿的四个空格一定要在新起段落的开头。

如：

        document.ready(function () {
            alert('markdown');
        });
        
显示为：

    document.ready(function () {
        alert('markdown');
    });
    
## 内嵌代码段
有时候我们并不需要一大段的代码，而只是一个简单的代码语句，而且是嵌在其它正常文本中，则可以使用这种格式。内嵌代码段使用两个“\`”号包裹即可，注意，“\`”并不是中文的顿号，而是英文文的一个样子类似的符号，不过它的位置比较靠上。它在键盘上的位置在左上角，跟“\~”号在同一个键上，在英文输入法下点击它即可。

使用方法：

    我是一个内嵌的代码`println("out put message")`，代码不长。

显示为：  
我是一个内嵌的代码`println("out put message")`，代码不长。

## 指定具体语言的代码块
如果你的文章读者是程序员，那把你展示的代码根据对应语言的语法进行高亮显示，他们阅读起来时会更加友好。  
指定语言的代码块要求首尾两行使用三个“\`”包裹，在首行的三个“\`”后写上你的语言名称。注意，一是符号“\`”跟上边的内嵌代码段符号一样，不是中文顿号；二是首行的三个“\'”必须新起一段（两个回车）；三是首尾的三个“\`”必须顶头，且分别在独立行内。

写法如下：

    ``` javascript
    $(document).ready(function () {
        alert('markdown');
    });
    ```
显示如下：

``` javascript
$(document).ready(function () {
    alert('markdown');
});
```

遗憾的是macdown对语言的支持能力比较有限，需要把你的markdown文档传到一些平台后再看了。

Markdown支持哪些语言，以及这此语言的名就都应该怎么写呢？我们可以看下面的这个表格。

| 名称 | 关键字 | 说明 |
| --- | --- | --- |
| Java | java | |
| JavaScript | js或jscript或javascript |  |
| PHP | php | |
| C | cpp或c | |
| Python | py或python | |
| Objective C | objc或obj-c | |
| swift | swift | |
| C# | c#或c-sharp或csharp | |
| Perl | perl或pl或Perl | |
| Shell | bash或shell | |
| GO | go或golang | |
| SQL | sql | |
| CSS | css | |
| Delphi | delphi或pascal或pas | |
| Visual Basic | vb或vbnet | |
| Groovy | groovy | |
| JSON | json | |
| XML | xml或xhtml或xslt或html | |
| Scala | scala | |
| matlab | matlab | |
| AppleScript | applescript | |
| ActionScript 3.0 | actionscript3或as3 | |
| ColdFusion | coldfusion或cf | |
| Erlang | erl或erlang | |
| JavaFX | jfx或javafx | |
| text | text或plain | |
| Ruby | ruby或rails或ror或rb | |
| SASS&SCSS | sass或scss | |
| diff&patch | diff patch | 用代码版本库时,遇到代码冲突,其语法就是这个 |
| F# | f#或f-sharp或fsharp | |
| R | r或s或splus | &nbsp; |


### 视频教程
<iframe src="//player.bilibili.com/player.html?aid=499405385&bvid=BV1rK411N78Z&cid=231126240&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width="800" height="600"> </iframe>