## 前端三大拿：HTML、CSS、JS

- HTML是**内容**，CSS是**样式**，JavaScript是**行为**。
- HTML **内容**展示：请点击我...
- CSS **样式**展示：请点击我...
- JavaScript **行为**展示：请点击我...

```javascript
function sample1_func() {
    var text_area = document.getElementById("sample1_desc");
    var a, b;
    while (isNaN(a)) a = Number(prompt("请输入第一个数字"));
    while (isNaN(b)) b = Number(prompt("请输入第二个数字"));
    text_area.innerHTML += a + "+" + b + "=" + (a + b) + "<br>";
}
var obj = document.getElementById("sample1");
obj.onclick = sample1_func;
```

```html
<p>HTML <b>内容</b>展示：<span>请点击我...</span></p>
<p>CSS <b>样式</b>展示：<span class="sample1">请点击我...</span></p>
<p>JavaScript <b>行为</b>展示：<span class="sample1" id="sample1">请点击我...</span></p>
<p id="sample1_desc"></p>
```

```css
.sample1 {
    color: #339999;
    text-decoration: underline;
    cursor:pointer;
    border: 3px solid red;
}

#sample1_desc {
    width: 40%;
    height: 100px;
    border: 5px solid #000;
    border-radius: 20px;
    overflow: auto;
    text-indent: 0;
    padding-left: 2em;
}
```

## HTML 概念

- HTML 指的是超文本标记语言 (**H**yper **T**ext **M**arkup **L**anguage)
- HTML 不是一种编程语言，而是一种**标记语言** (markup language)
- 标记语言是一套**标记标签** (markup tag)
- HTML 使用**标记标签**来描述网页

```html
<h1>这是一级标题</h1>
<h2>这是二级标题</h2>
<p>这是段落，这个标签里面可以写很多话，你可以试试</p>
<a href="https://www.baidu.com/" target="_blank">这是链接，可以点击，点我打开百度</a>
||||||
<a href="https://www.taobao.com/" target="_blank">这是链接，可以点击，点我打开淘宝</a>
<br>
<img height="200px" src="http://47.93.11.51:88/img/2019-05-26/54E9C51263E1462585A8F6595841EEC0.jpg">
```

## CSS 概念

- CSS 指的是层叠样式表 (**C**ascading **S**tyle **S**heets)
- 用来表示 HTML 文档样式的计算机语言
- 由**选择器**和**属性列表**组成
- 控制元素**颜色**、**大小**、**位置**、**形状和动画**(CSS3新增)

```html
<h1>这是一级标题</h1>
<h2>这是二级标题</h2>
<p>这是段落，这个标签里面可以写很多话，你可以试试</p>
<a href="https://www.baidu.com/" target="_blank">这是链接，可以点击，点我打开百度</a>
||||||
<a href="https://www.taobao.com/" target="_blank">这是链接，可以点击，点我打开淘宝</a>
<br>
鼠标放到下面图片上，会有神奇效果。<br>
<img height="200px" src="http://47.93.11.51:88/img/2019-05-26/54E9C51263E1462585A8F6595841EEC0.jpg">
```

```css
h1 {
    color: gold;
    text-decoration: underline;
}

p {
    width: 100%;
    text-align-last: justify; 
}

a {
    color: yellowgreen;
    display: block;
    text-decoration: none;
}

img {
    height: 100px;
    width: 300px;
    border: 5px solid red;
}

img:hover {
    cursor: pointer;
    position: relative;
    left: 20px;
    top: 20px;
    transform: skewX(30deg);
}
```

## HTML & CSS 发展历史

| html | 2004-2014<br />HTML5定稿 | 2001(W3C)<br/>XHTML1.1 | 2000(W3C)<br/>XHTML1.0 | 1999(W3C)<br/>HTML4.0.1 | 1997(W3C)<br/>HTML4.0 | 1996(W3C)<br/>HTML3.2   | 1995(W3C)<br/>HTML2.0    | 1993(IETF)<br/>HTML1.0 |
| ---- | ------------------------ | ---------------------- | ---------------------- | ----------------------- | --------------------- | ----------------------- | ------------------------ | ---------------------- |
| css  | 周边工具<br/>PostCSS     | 周边工具<br/>SCSS      | 周边工具<br/>LESS CSS  | 2011(W3C)<br/>CSS3      | 1998(W3C)<br/>CSS2    | 1997(W3C)<br/>CSS工作组 | 1994(Argo)<br/>CSS被提出 |                        |

## HTML 基础语法

### 元 素

```html
<a href="http://haizeix.com" style="color:blue;">点击我<a/>
```

**元素**代表 HTML 上一个独立的组成部分。

可能是一个链接，可能是一个段落，也可能是布局的一块，也可能是一个图片。

### 标 签

```html
<a href="http://haizeix.com" style="color:blue;">点击我<a/>
```

**标签**大多数时候是一个元素的语义描述。

从功能实现角度来说的话，标签的这种语义描述完全没有意义。

从代码规范性角度来讲的话，这种语义，是很有必要的，尤其对于现代搜索引擎来说，意义重大。

例如：a 标签表示链接，img 标签表示图片，p 标签表示段落，ul 标签表示无序列表，nav 表示导航，这是 h5 新加入的标签。

### 属 性

```html
<a href="http://haizeix.com" style="color:blue;">点击我<a/>
```

**属性**是用来描述标签的某些性质的。

上述中 a 标签中的 href，用来指定跳转链接。style 用来设置标签的一些样式。

## HTML 基础结构

### HTML文档

**<html>**标签所包含的部分，内部主要包含**头部信息**和**内容主体**两部分。

### 头部信息

**<head>**标签所包含的部分，可以包含如下标签：

| 编 号 | 标 签                                                     | 说 明                                  |
| ----- | --------------------------------------------------------- | -------------------------------------- |
| 1     | [title](https://www.w3school.com.cn/tags/tag_title.asp)   | 网站标题                               |
| 2     | [style](https://www.w3school.com.cn/tags/tag_style.asp)   | 今后要学习的 **CSS** 写在这里面        |
| 3     | [script](https://www.w3school.com.cn/tags/tag_script.asp) | 今后要学习的 **JavaScript** 写在这里面 |
| 4     | [link](https://www.w3school.com.cn/tags/tag_link.asp)     | 引用外部样式、logo 等会使用这个        |
| 5     | [meta](https://www.w3school.com.cn/tags/tag_meta.asp)     | 作用很神奇，后续逐渐展开               |
| 6     | [base](https://www.w3school.com.cn/tags/tag_base.asp)     | 规定了浏览器中的默认地址和默认目标     |

### 内 容 主 体

**<body>**标签所包含的部分，网页中**最最最**重要的主体部分。所谓的编写 HTML 部分的内容，说的就是这部分。来认识几个基本标签：

| 编 号 | 标 签                                                        | 说 明                                                    |
| ----- | ------------------------------------------------------------ | -------------------------------------------------------- |
| 1     | [h[1-6\]](https://www.w3school.com.cn/tags/tag_hn.asp)       | 标题标签，大小不一样的标题                               |
| 2     | [hr](https://www.w3school.com.cn/tags/tag_hr.asp)            | 水平分割线                                               |
| 3     | [p](https://www.w3school.com.cn/tags/tag_p.asp)              | 段落标签，用来区分段落                                   |
| 4     | [pre](https://www.w3school.com.cn/tags/tag_pre.asp)          | 进阶的段落标签，保留内容中的换行和段落                   |
| 5     | [br](https://www.w3school.com.cn/tags/tag_br.asp)            | 换行标签，用于在文本中换行                               |
| 6     | [a](https://www.w3school.com.cn/tags/tag_a.asp)              | 超链接，通常实现点击链接，跳转到另外一个页面的效果       |
| 7     | [img](https://www.w3school.com.cn/tags/tag_img.asp)          | 图片标签，用来插入一张图片                               |
| 8     | [i](https://www.w3school.com.cn/tags/tag_i.asp)、[em](https://www.w3school.com.cn/tags/tag_em.asp) | 斜体                                                     |
| 9     | [b](https://www.w3school.com.cn/tags/tag_b.asp)、[strong](https://www.w3school.com.cn/tags/tag_strong.asp) | 加粗                                                     |
| 10    | [sub](https://www.w3school.com.cn/tags/tag_sub.asp)、[sup](https://www.w3school.com.cn/tags/tag_sup.asp) | 下标(Subscript)，上标(Superscript)                       |
| 11    | [div](https://www.w3school.com.cn/tags/tag_div.asp)          | 代表独立的一个区域，布局届的一哥，理论上可以变成任何元素 |

## CSS 基础结构

```css
<style>
body {
    background-color: #abcdef;
}
.red {
    color: red;
}
#head {
    border: 5px solid #336699;
}
</style>
```

### 选 择 器

顾名思义，**选择器**就是用来选择要修改样式的元素。选择器，有些时候，选择的是一个元素，有些时候选择的是一组元素。示例代码中的 body 属于**标签选择器**，.red 是**类选择器**，#head 是 **id 选择器**，这三者也是最常用的三种选择器。下表中，列出了 CSS 中的一些常用的基础选择器：

[W3School 参考链接](https://www.w3school.com.cn/cssref/css_selectors.ASP)

| 编 号 | 选 择 器                                                     | 例 子      | 说 明                                               |
| ----- | ------------------------------------------------------------ | ---------- | --------------------------------------------------- |
| 1     | [element](https://www.w3school.com.cn/cssref/selector_element.asp) | p,h1,div   | 元素选择器，直接写标签名                            |
| 2     | [.class](https://www.w3school.com.cn/cssref/selector_class.asp) | .red       | 类选择器，以点(.)作为开头                           |
| 3     | [#id](https://www.w3school.com.cn/cssref/selector_id.asp)    | #head      | id 选择器，以 # 作为开头                            |
| 4     | [:hover](https://www.w3school.com.cn/cssref/selector_hover.asp) | a:hover    | 伪类选择器，以 : 作为开头，鼠标悬浮的元素           |
| 5     | [:before](https://www.w3school.com.cn/cssref/selector_before.asp) | div:before | 伪元素选择器，以 : 作为开头，在元素内的最前插入元素 |
| 6     | [:after](https://www.w3school.com.cn/cssref/selector_after.asp) | div:after  | 伪元素选择器，以 : 作为开头，在元素内的最后插入元素 |

### 属 性 列 表

通过选择器，确定了一组元素以后，接下来，我们可以在大括号内，设置相关元素的样式属性，这些样式属性，可以控制元素的**颜色**、**大小**、**位置**、**形状和动画**（CSS3 新增）。先来看几个控制元素**颜色**和**大小**的属性方法：

| 编 号 | 属 性                                                        | 说 明                                           |
| ----- | ------------------------------------------------------------ | ----------------------------------------------- |
| 1     | [background](https://www.w3school.com.cn/cssref/pr_background.asp) | 设置元素的背景属性，最简单的是设置颜色          |
| 2     | [height](https://www.w3school.com.cn/cssref/pr_dim_height.asp) | 设置元素的高度                                  |
| 3     | [width](https://www.w3school.com.cn/cssref/pr_dim_width.asp) | 设置元素的宽度                                  |
| 4     | [padding](https://www.w3school.com.cn/cssref/pr_padding.asp) | 设置元素的内边距                                |
| 5     | [border](https://www.w3school.com.cn/cssref/pr_border.asp)   | 设置元素的边框                                  |
| 6     | [margin](https://www.w3school.com.cn/cssref/pr_margin.asp)   | 设置元素的外边距                                |
| 7     | [display](https://www.w3school.com.cn/css/pr_class_display.asp) | 设置元素的展示类型：block、inline、inline-block |

### 标准盒子模型

想要学习 CSS 属性设置，必须要理解的就是『**标准盒子模型**』，有标准就有非标准，非标准，也叫做『**IE 盒子模型**』，下图就是『**标准盒子模型**』:
