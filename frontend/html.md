# HTML 知识点
[查看思维导图](./../minds/html.svg)
<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [HTML 知识点](#html-知识点)
  - [学习HTML，究竟在学什么](#学习html究竟在学什么)
  - [基本语法](#基本语法)
    - [定义基本元素](#定义基本元素)
    - [HTML文档](#html文档)
    - [HTML元素构成](#html元素构成)
      - [HTML 提示：使用小写标签](#html-提示使用小写标签)
    - [HTML属性](#html属性)
    - [注释](#注释)
  - [网页结构](#网页结构)
    - [基本架子](#基本架子)
      - [标准代码结构](#标准代码结构)
      - [!DOCTYPE](#doctype)
        - [常见声明：](#常见声明)
          - [HTML5](#html5)
          - [HTML4](#html4)
          - [XHTML1.0](#xhtml10)
      - [HTML <meta> charset 属性](#html-meta-charset-属性)
      - [favicon-网页标签的小图标](#favicon-网页标签的小图标)
  - [HTML的应用](#html的应用)
    - [HTML手册使用](#html手册使用)
    - [通用属性和通用事件](#通用属性和通用事件)
    - [常见场景](#常见场景)
      - [导航](#导航)
      - [文字](#文字)
      - [图片](#图片)
      - [表单](#表单)
      - [节点、样式](#节点样式)
      - [多媒体](#多媒体)
  - [HTML的结构最佳实践](#html的结构最佳实践)
    - [书写规范](#书写规范)
    - [嵌套规范](#嵌套规范)
    - [语义化](#语义化)
    - [SEO的HTML要点](#seo的html要点)

<!-- /code_chunk_output -->


## 学习HTML，究竟在学什么

HTML(Hyper Text Markdown Language)是用来描述网页结构的语言，通过英文全称直接翻译就是超文本标记语言．

所以重点在
1. **标记语言**
2. **网页结构**


用来标记的是主体应当是标签，那么我们学习HTML目标应当是２个：
1. 学习HTML标签的用法．
2. 使用HTML标签组织网页结构．

并且在此上述两个的基础上，我们要追求什么样的网页结构是合理的

## 基本语法
### 定义基本元素
- HTML 标签是由尖括号包围的关键词，比如 `<html>`
- HTML 标签通常是成对出现的，比如 `<b> 和 </b>`
- 标签对中的第一个标签是开始标签，第二个标签是结束标签
- 开始和结束标签也被称为开放标签和闭合标签

### HTML文档
- HTML 文档描述网页
- HTML 文档包含 HTML 标签和纯文本
- HTML 文档也被称为网页
- Web 浏览器的作用是读取 HTML 文档，并以网页的形式显示出它们。浏览器不会显示 HTML 标签，而是使用标签来解释页面的内容。
### HTML元素构成
- HTML 元素以开始标签起始
- HTML 元素以结束标签终止
- 元素的内容是开始标签与结束标签之间的内容
- 某些 HTML 元素具有空内容（empty content）
- 空元素在开始标签中进行关闭（以开始标签的结束而结束）
- 大多数 HTML 元素可拥有属性

#### HTML 提示：使用小写标签
HTML 标签对大小写不敏感：  `<P> 等同于 <p>`。许多网站都使用大写的 HTML 标签。

W3School 使用的是小写标签，因为万维网联盟（W3C）在 HTML 4 中推荐使用小写，而在未来 (X)HTML 版本中强制使用小写。

### HTML属性
- HTML 标签可以拥有属性。属性提供了有关 HTML 元素的更多的信息。
- 属性总是以名称/值对的形式出现，比如：name="value"。
- 属性总是在 HTML 元素的开始标签中规定。
- HTML 提示：使用小写属性
- 始终为属性值加引号
- [HTML 属性参考手册](https://www.w3school.com.cn/tags/html_ref_standardattributes.asp)

### 注释
注释标签   `<!-- 与 -->` 用于在 HTML 插入注释。

例子：
    
     <!-- 在此处写注释 -->

## 网页结构
### 基本架子
#### 标准代码结构
一般来说，大多数代码编辑器都会自动生成：

```<!DOCTYPE html>
<html>
<head>
<title>这是一个网页的标题</title>
<meta charset="UTF-8">
</head>
<body>
网页内容
</body>
</html>
```
这个结构几乎是一个主流的标准了，下面讲解这个结构的内容
#### !DOCTYPE
Web 世界中存在许多不同的文档。只有了解文档的类型，浏览器才能正确地显示文档。
HTML 也有多个不同的版本，只有完全明白页面中使用的确切 HTML 版本，浏览器才能完全正确地显示出 HTML 页面。这就是 <!DOCTYPE> 的用处。
<!DOCTYPE> 不是 HTML 标签。它为浏览器提供一项信息（声明），即 HTML 是用什么版本编写的。
##### 常见声明：
###### HTML5
```
<!DOCTYPE html>
```
###### HTML4
```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN"
"http://www.w3.org/TR/html4/loose.dtd">
```
###### XHTML1.0
```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
```

#### HTML <meta> charset 属性
- charset 属性规定 HTML 文档的字符编码。提示：charset 属性可以通过任意元素上的 lang 属性来重写。
- charset 属性是 HTML5 中的新属性，且替换了：`<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">`。仍然允许使用 http-equiv 属性来规定字符集，但是使用新方法可以减少代码量。
- 常用的值：UTF-8 - Unicode 字符编码
ISO-8859-1 - 拉丁字母表的字符编码
在理论上，可以使用任何字符编码，但并不是所有浏览器都能够理解它们。某种字符编码使用的范围越广，浏览器就越有可能理解它。如需查看所有可用的字符编码，请访问 [IANA](http://www.iana.org/assignments/character-sets/character-sets.xhtml) 字符集。

#### favicon-网页标签的小图标
在head标签中，我们可以编写一段html的语言来显示favicon，即显示网页标签上的小图标。这种做法已经是网页主流结构常见的一部分了。

## HTML的应用
### HTML手册使用
### 通用属性和通用事件
### 常见场景
#### 导航
#### 文字
#### 图片
#### 表单
#### 节点、样式
#### 多媒体
## HTML的结构最佳实践
### 书写规范
### 嵌套规范
### 语义化
### SEO的HTML要点

