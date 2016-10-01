## 罗列Bootstrap的使用

viewport
=============
>width=device-width sets the width of the page to follow the screen-width of the device (which will vary depending on the device).
The initial-scale=1 part sets the initial zoom level when the page is first loaded by the browser.

起步
==============================
#####.container  .container-fluid
container :固定宽度
container-fluid: 100%宽度
container不能嵌套

网格布局
=================================
xs(phone) sm(table) md(desktop) lg(larger desktop)


默认设置
==================================
字体默认为14px,行高为1.428(20px),段落默认有行高的一半(10px)

```css
p {
  margin: 0 0 (@line-height-computed / 2);
}
```

```
  <small>创建小文本 font-size:65%</small>
  <mark> 添加背景色 padding:0.2em background-color:#fcf8e3;</mark>
  <abbr title="..."> 下面添加点画线，abbr[title]{cursor: help;border-bottom: 1px dotted #777;}</abbr>
  <blockquote> 引用模块，左侧竖线。.blockquote-reverse 右侧对齐，右侧竖线</blockquote>
  <code> 添加浅色背景 </code>
  <kbd> 键盘输入显示,黑底白字</kbd>
  <pre>代码块显示</pre>
```

表现状态字体颜色，背景颜色：
```
.text-muted, .text-primary, .text-success, .text-info, .text-warning, and .text-danger
.bg-primary, .bg-success, bg-info, bg-warning, and .bg-danger
```
```
.lead 突出显示一个段落
.small  85%字体大小
.text-left      文本向左对齐 text-align: left;
.text-center  文本居中对齐
.text-right     文本向右对齐
.text-justify 
.text-nowrap   文本不换行 white-space: nowrap;
.text-lowercase  小写转换 text-transform:lowercase
.text-uppercase  大写转化
.text-capitalize 首大写
.initialism 
.list-unstyled  移除list-style和左内补
.list-inline  行内list
.dl-horizontal  
.pre-scrollable 可滚动代码块
```


表格
=================================
* .table 默认样式
* .table-striped 交替颜色表格
```css
.table-striped {
  > tbody > tr:nth-of-type(odd) {
    background-color: @table-bg-accent;
  }
}
```
* .table-bordered 添加边框
* .table-hover 悬停背景高亮
* .table-condensed 紧凑型，减小内补
```css
.table-hover {
  > tbody > tr:hover {
    background-color: @table-bg-hover;
  }
}
```

 可以作用在tr td上的contextual classes
* .active
* .success
* .info
* .warning
* .danger

图片
=================================================
* .img-rounded     圆角6px
* .img-circle      圆形
* .img-thumbnail   inline-block 内补，添加倒角边框
* .img-responsive  响应式图片, 跟随父元素大小变化 display:block; max-width:100%,height:auto

jumbotron
==================================================
* div + .jumbotron 大幕显示，内补+大字体
* .page_header 大标题，下划线，边距内补


well
==================================================
    .well 边框+背景色+内补
    .well-sm
    .well-lg

Alert
===============================================
    .alert 警告信息
    .alert-success
    .alert-info
    .alert-warning
    .alert-danger
    .close 关闭消息 data-dismiss="alert"
    .fade .in 渐进式变化opacity

Button
================================================
.btn 默认按钮样式 可施加在button a input元素 

    .btn-default
    .btn-primary
    .btn-success
    .btn-info
    .btn-warning
    .btn-danger
    .btn-link
    
不同大小btn

    .btn-lg
    .btn-md
    .btn-sm
    .btn-xs

.btn-block 块级button width:100%

ButtonGroup
====================================================
div

* .btn-group            创建按钮组
* .btn-group-vertical   垂直按钮组
* .btn-group-justified  铺满整个宽度按钮组
* .btn.dropdown-toggle data-toggle="dropdown" 下拉按钮

```css
.btn-group, .btn-group-vertical {
    position: relative;
    display: inline-block;
    vertical-align: middle;
}
.btn-group-justified {
    display: table;
    width: 100%;
    table-layout: fixed;
    border-collapse: separate;
}
.btn-group-justified > .btn, .btn-group-justified > .btn-group {
    display: table-cell;
    float: none;
    width: 1%;
}
```

Glyphicons
=====================================================
符号字体
```
<span class="glyphicon glyphicon-name"></span>
```

Badge_Label
=====================================================
* span.badge  徽章  inline-block
* span.label  标签 label-success,label-default

Pagination
=====================================================
* ul.pagination 分页
* li.active     对应页面被选中
* li.disabled   对应页面被禁用
* .pagination-sm,.pagination-lg 大小分页
* ul.breadcrumb 面包屑分页

Pager
======================================================
* ul.pager 分页
* li.previous  li.next 排布按钮到两侧


ListGroup
=======================================================
    ul.list-group li.list-group-item  创建列表
    li span.badge 列表项中添加徽章
    
    div.list-group a.list-group-item 创建链接列表项
    .list-group-item.active     选中项
    .list-group-item.disable    禁用该项
    .list-group-item.list-group-item-success 
    .list-group-item.list-group-item-info
    
    list-group-item内可任意自定义元素
    .list-group-item-heading  上边距为0
    .list-group-item-text     下边距为0

Panel
==========================================================
    div.panel.panel-default      面板，边框+内补
    .panel .panel-body           面板内容
    .panel .panel-heading        面板标题
    
    .panel-group  多个panel组成panel-group
    
    .panel-default, .panel-primary, .panel-success, .panel-info

DropDown
===========================================================
    div.dropdown 下拉菜单position:relative; 内部菜单项绝对定位。
    触动按钮或链接上添加 .dropdown-toggle 和 data-toggle="dropdown"
    菜单项上添加         .dropdown-menu
    
    .dropdown-menu .divider          菜单项内部添加分隔线
    .dropdown-menu .dropdown-header  菜单项内部添加抬头
    .dropdown-menu .disabled         菜单项内禁用项    
    
    .dropdown-menu.dropdown-menu-right 右对齐菜单项

    <div class="dropdown">
      <button class="btn btn-primary dropdown-toggle" type="button" data-toggle="dropdown">Dropdown Example
      <span class="caret"></span></button>
      <ul class="dropdown-menu">
        <li><a href="#">HTML</a></li>
        <li><a href="#">CSS</a></li>
        <li><a href="#">JavaScript</a></li>
      </ul>
    </div>

Collapsible
=========================================================
显隐大量内容

* 在按钮上定义  data-toggle="collapse" data-target="#demo"
    在内容上定义  id="demo" class="collapse"


* 在a上定义   data-toggle="collapse" href="#demo"
    在内容上定义  id="demo" class="collapse"

```code
<button data-toggle="collapse" data-target="#demo">Collapsible</button>
<div id="demo" class="collapse">
Lorem ipsum dolor text....
</div>
```

可显隐的panel
```
<div class="panel-group">
  <div class="panel panel-default">
    <div class="panel-heading">
      <h4 class="panel-title">
        <a data-toggle="collapse" href="#collapse1">Collapsible panel</a>
      </h4>
    </div>
    <div id="collapse1" class="panel-collapse collapse">
      <div class="panel-body">Panel Body</div>
      <div class="panel-footer">Panel Footer</div>
    </div>
  </div>
</div>
```

可显隐的list-group
```
<div class="panel-group">
  <div class="panel panel-default">
    <div class="panel-heading">
      <h4 class="panel-title">
        <a data-toggle="collapse" href="#collapse1">Collapsible list group</a>
      </h4>
    </div>
    <div id="collapse1" class="panel-collapse collapse">
      <ul class="list-group">
        <li class="list-group-item">One</li>
        <li class="list-group-item">Two</li>
        <li class="list-group-item">Three</li>
      </ul>
      <div class="panel-footer">Footer</div>
    </div>
  </div>
</div>
```

Tabs/Pills
==================================================
* ul.list-inline   水平菜单
* ul.nav.nav-tabs  tab标签
* ul.nav.nav-justified  标签平铺
* ul.nav.nav-pills      pill标签
* ul.nav.nav-pills.nav-stacked  水平排布

tab动态显隐效果

* 在链接上添加 data-toggle="tab" href="#xx"
对应id的div 添加.tab-pane 包裹在 .tab-content

pill动态显隐效果

* 在链接上添加 data-toggle="pill" href="#xx"
对应id的div 添加.tab-pane 包裹在 .tab-content


Navigation_Bar
=====================================================

```code
<nav class="navbar navbar-inverse">
  <div class="container-fluid">
    <div class="navbar-header">
      <button type="button" class="navbar-toggle" data-toggle="collapse" data-target="#myNavbar">
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span> 
      </button>
      <a class="navbar-brand" href="#">WebSiteName</a>
    </div>
    <div class="collapse navbar-collapse" id="myNavbar">
      <ul class="nav navbar-nav">
        <li class="active"><a href="#">Home</a></li>
        <li><a href="#">Page 1</a></li>
        <li><a href="#">Page 2</a></li> 
        <li><a href="#">Page 3</a></li> 
      </ul>
      <ul class="nav navbar-nav navbar-right">
        <li><a href="#"><span class="glyphicon glyphicon-user"></span> Sign Up</a></li>
        <li><a href="#"><span class="glyphicon glyphicon-log-in"></span> Login</a></li>
      </ul>
    </div>
  </div>
</nav>
```

Form
=====================================
.form-control  默认设置，input textarea select默认100%宽度

三种类型的布局方式：
* 默认垂直布局
* 水平表单
* 内联表单

步骤:

    * 将label与控件元素包含在form-group之中
    * 将.form-control 添加在 input  textarea等元素中


    添加.form-inline在form,       内联表单
    添加.form-horizontal在form, 添加control-label在label,   水平表单


Form input
=======================================
Form 元素
    div.checkbox         复选框
    div.checkbox-inline  行内复选框
    
    div.radio            单选框
    div.radio-inline     行内单选框
    
    .has-success.form-control  高亮显示input元素
    
    .input-lg .input-sm 设置input元素的大小
    .span.help-block    添加help信息到input之后

Media
=======================================

    父元素:div.media
    字元素:div.media-left,div.media-body

Carousel
======================================
轮播插件

    最外层div   
    #myCarousel           指定id为myCarousel
    .carousel             添加轮播样式
    .slide                切换时滑动
    data-ride="carousel"  页面加载完即触发轮播

指示器list

    ul.carousel-indicators
    li指定data-target="#myCarousel",data-slide-to="0" 指定显示id为myCarousel的第一张轮播

轮播slide

    div.carousel-inner 指定轮播slide
    每个slide指定.item
    .item内部指定.carousel-caption设定标题

control
    a.carousel-control 指定控制链接，data-slide="next" 指定向后slide


Modal
=========================================
模态对话框

    触发button，定义data-toggle="modal" data-target="#myModal" 打开id为myModal的模态对话框
    
    内容：.modal.modal-dialog
    标题：.modal-header
    内容: .modal-body
    页脚：.modal-footer


ToolTip
=============================================
提示信息

    触发元素上添加： data-toggle="tooltip"，title属性指定显示文本，data-placement指定提示文本显示位置


Popover
=============================================
提示信息，与ToolTip类似，但单击后可以显示更多内容

    触发元素上添加：data-toggle="popover",title属性指定头部文字，data-content属性指定body文字
    data-placement指定提示位置
    
    data-trigger="focus" 外部点击时消失
    data-trigger="hover" 悬停时显示