# 列表
列表是我们在写一些条理或条款时经常用到的形式，列表一般分为有序列表或无序列表两种形式；同时，列表还有二级、三级列表、多级列表等形式，我们分别来介绍一下。

## 无序列表
无序列表是在每一行开头处加一个小圆点，实现方式为在新一段的开头，用“\*”、“\+”或“\-”加空格来标记，注意，只是能新的一段开头，换行的开头是不行的。

写法如下：  

    * 我是第一条  
    + 我是第二条  
    - 我是第三条  

显示如下：

* 我是第一条  
+ 我是第二条  
- 我是第三条  

不过我们平时使用时，统一使用一种符号即可，如我们选择“\+”，星号建议在粗、斜体中使用，中划线在二级标题时使用。  
如：

    + 我是列表第一条
    + 我是列表第二条
    + 我是列表第三条
    
## 有序列表
有序列表可以是1、2、3这样开头，也可以是（1）（2）（3）这种，还可以是a、b、c这种，但Markdown只支持1.2.3这种，如果想用其它形式，需要自己实现。有序列表仍然要求在段落的开头使用“1.”加一个空格来标记，注意，空格也是必须的，可以有多个。

写法如下：

    1. 我是第一条
    2. 我是第二条
    3. 我是第三条
    4.       我是第四条

显示如下：

1. 我是第一条
2. 我是第二条
3. 我是第三条
4.         我是第四条

## 多级列表
列表有多个层级也是我们常常会遇到的情况，不过Markdown不建议列表有过多的层级，三级即可，再深的层级排版会比较难看，所以Markdown的多级列表中有三种表示方法：一级为实心圆或123，二级为空心圆，三级为实心方块。如果有四级、五级等更多层级，也使用实心方块来表示。

我们先来看多级无序列表的写法：

    + 我是一级列表
        + 我是二级列表
            + 我是三级列表
            + 我是并列三级列表
              + 我是四级列表
        
            
显示如下： 

+ 我是一级列表
    + 我是二级列表
        + 我是三级列表
        + 我是并列三级列表
            + 我是四级列表
            
我们再来看多级有序列表，Markdown中有序列表样式比较单一，所以各级列表序号没有区别：

    1. 我是一级有序列表1
    2. 我是一级有序列表2
        1. 我是二级有序列表
        2. 我是二级无序列表
            1. 我是三级列表
            2. 我是三级列表

显示如下：

1. 我是一级有序列表1
2. 我是一级有序列表2
    1. 我是二级有序列表
    2. 我是二级无序列表
        1. 我是三级列表
        2. 我是三级列表

有序列表和无序列表是可以混合使用的，不过对应层级上的序号样式不会变化，如下，二级列表使用无序，它仍然会显示为空心圆。

    1. 我是一级有序列表1
    2. 我是一级有序列表2
        + 我是二级无序列表
        + 我是二级无序列表
            + 我是三级无序列表
            
显示如下：

1. 我是一级有序列表1
2. 我是一级有序列表2
    + 我是二级无序列表
    + 我是二级无序列表
        + 我是三级无序列表


### 视频教程
<iframe src="//player.bilibili.com/player.html?aid=839434637&bvid=BV1W54y1279g&cid=229141124&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true" width="800" height="600"> </iframe>

[打赏](../include/donate.md ':include')