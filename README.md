# bootstrap-learning-note
# **bootstrap全局样式篇**<small>(学习一下类名样式规则)</small>

bootstrap 作为一款在github上有118k   star的响应式项目是很值得我们学习的，
其中的**栅格系统**的思想对于响应式布局是很好的思想，bootstrap分为几大块，今天学习总结的是样式篇，对于这一章，我更多的是认为就是一个记忆的过程，因为这些全局样式
如果你对css和html比较精通手写也是可以的，但是bootstrap所提供的less预编译，他的样式写法和类名写法还是很有参考意义的；在学习bootstrap之前建议去 学习一下grunt和 less 那样会更有助于学习理解和记忆；为了更好的记忆和学习我写了下面的文章，列出了一些我认为比较重要的地方跟大家分享学习。
好了下面大家一起记单词吧！


## 标题 

    h1-h6   small 副标题
    提供.h1 到.h6 和 .small 的类名
为了便于记忆初始大小是36px  然后依次按 6 6 4 4 2  的大小递减
    
    

标题 |字体大小
---|---
h1 | 36px
h2 | 30px
h3 | 24px
h4 | 18px
h5|  14px
h6|  12px

    
    
Bootstrap 将全局 font-size 设置为 14px，line-height 设置为 1.428。这些属性直接赋予 <body> 元素和所有段落元素。另外，<p> （段落）元素还被设置了等于 1/2 行高（即 10px）的底部外边距（margin）。
    
### **记住一些标签**
标签名 | 作用
---|---  
.lead |类可以让段落突出显示。
u | 下划线
strong | 强调
em |斜体
ins del | 被删除的和无用文本 
.text-left text-方向|文本对齐类 
.text-justify |
.text-nowrap |不换行
address  |地址
ul.list-unstyled |无样式列表
ul.list-inline   |内联列表
.text-overflow |自动截断
    dl.dl-horizontal| 横着的描述
    
    
    <dl>
      <dt>...</dt>
      <dd>...</dd>
    </dl>  
带有描述的短语列表。
    

    
横着的
##     表格
    <table class="table">
  ...
</table>

类名 | 作用
---|---
.table-striped  |条纹状表格
.table-bordered |带边框的表格
.table-hover   |鼠标悬停

状态类  |作用 (就是颜色不一样)
---|---
.active	|鼠标悬停在行或单元格上时所设置的颜色
.success|	标识成功或积极的动作
.info	|标识普通的提示信息或动作
.warning	|标识警告或需要用户注意
.danger	|标识危险或潜在的带来负面影响的动作
.table-responsive | 响应式表格<br/>



<p style='color:red;'>
注意响应式表格这个不是在table上面加是在  table外面的div加类名（其会在小屏幕设备上（小于768px）水平滚动。当屏幕大于 768px 宽度时，水平滚动条消失。）<p/>



## 表单 （在全局样式中这部分算是比较多的内容了）

类名 | 作用
---|---
.form-control |宽度属性为 width: 100%
 .form-group| label 等元素包在 .form-group 中可以获得最好的排列
 label.sr-only |将其隐藏
 .checkbox-inline|inline的checkbox
 .radio-inline |inline的radio
 .form-control-static|静态控件（及纯文本）
#####  水平排列的表单
 ++通过为表单添加 .form-horizontal 类，并联合使用 Bootstrap 预置的栅格类，可以将 label 标签和控件组水平并排布局++

  
将 label 元素和前面提到的控件包裹在 .form-group 中可以获得最好的排列
内联表单

## 按钮



<p style='color:red;'>tip:a  role="button"  作为不是点击的功能</p>

##### 尺寸
.btn-lg、.btn-sm 或 .btn-xs


```
激活状态  .active  
btn禁用状态  disabled="disabled"

链接（<a>）元素 .disabled 类
```

类名| 颜色
---|---
btn-default | 背景灰色黑字
btn-primary | 深蓝
btn-success| 浅绿
 btn-info| 浅蓝
btn-warning|浅黄色
btn-danger|浅红
btn-link| 字是蓝色链接



## 图片 
<span style='color:red;'>.img-responsive</span> 实际上是 max-width: 100%;、 height: auto; 和 display: block   的样式<br/>
图片水平居中.**center-block**

##### 图片形状

类名 | 作用
---|---
img-rounded | 圆角图片
img-circle | 圆形图片
img-thumbnail| 带有内边距padding的方形图片



## 辅助类

#### 情境文本颜色  文字颜色 

类名  | 作用（颜色）
---|---
text-muted | 缓和的，温和的
text-primary |  深蓝
text-success|浅绿
text-info|浅蓝
text-warning|浅黄色
text-danger|浅红




#### 情境背景色
**于此类似情景背景色为bg开头**
```
<p class="bg-primary">...</p>
<p class="bg-success">...</p>
<p class="bg-info">...</p>
<p class="bg-warning">...</p>
<p class="bg-danger">...</p>
```
关闭按钮

```
<button type="button" class="close" aria-label="Close"><span aria-hidden="true">&times;</span></button>
```
三角符号

```
<span class="caret"></span>
```

类名 | 作用
---|---
.close | 关闭按钮
.caret|三角符号
pull-left|快速浮动
pull-right|快速浮动
center-block|让内容块居中（已知宽度水平居中）
.show 和 .hidden |显示或隐藏内容
invisible |可见性
|
|


.pull-left() less 编译pull-left  可以作为 mixin使用

### 响应式工具

类名 |不同尺寸的可见和隐藏
---|---
.visible-xs-*|  小于768可见
.visible-sm-*|大于768可见
.visible-md-*|	大于992可见
.visible-lg-*|		大于1200可见
.hidden-xs|	
.hidden-sm|	
.hidden-md|	
.hidden-lg|	

#### 打印类  不常用不记了


**总结**：bootstrap 的全局样式定义了一些常用的类名，甚至可以帮助你在不写css的情况下构建看起来不错的响应式页面，对于不懂样式的开发人员无疑是福音，对于懂的则可以根据bootstrap的构建和less 中mixin的写法去写出更漂亮的页面；<br/>
**重点**:<br/>
        <span style='color:red;'>1.栅格系统</span>   <br/>
        <span style='color:red;'>2.类名的记忆和less中的mixin</span>