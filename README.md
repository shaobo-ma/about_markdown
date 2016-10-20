# 关于gitlab_README.md添加页面锚点的问题

####TOP
######【TOP为下文的测试做准备】

### markdown添加页内锚点一般有两种方法

+ **1.html标签实现**
```
加入链接：<a href="jump">点击发生跳转</a>

定义一个锚（id）<span id="jump">要跳转的地方</span>
```

***

+ **2.markdown语法实现**

```
[name](#_)                    [跳转到项目1]（#1）    
                        >>>
<span id="">__</span>         <h2 id="1">项目1</h2>
```

 [跳转到项目1](#1)

* <h2 id="1">项目1</h2>

* 项目2

* 项目3

* 项目4

* 项目5

* 项目6

*** 

#### 上述两种方法在markdown编辑器中都可实现页面内部跳转，在gitlab中无法实现。最后发现gitlab无法识别中文+英文+数字的id，只要保证链的id是<p color=red>`纯中文或纯英文`</p>即可。

```
[name](#_)>>>[回到顶部](#TOP)
```

[回到顶部](#TOP)
