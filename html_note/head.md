# `<head>` 元素

## 1. 什么是HTML头部？
&emsp;&emsp;HTML 头部是包含在 `<head>` 元素里面的内容。不像 `<body>` 元素的内容会显示在浏览器中，head 里面的内容不会在浏览器中显示，它的作用是包含一些页面的元数据。

## 2. 增加一个标题
* 元素 `<title>` 是用来表示整个HTML文档标题的元数据。title 一般是浏览器中一个页面的名称。
* 元素 `<title>` 也被以其他的方式使用着，比如说，添加书签时 `<title>` 的内容被作为建议的书签名；元素 `<title>` 的内容也被用在搜索的结果中。

## 3. 元数据：`<meta>` 元素
元数据就是描述数据的数据，HTML使用 `<meta>`元素来为一个文档添加元数据。
### 指定文档中字符的编码
```html
<meta charset="utf-8">
```
这个元素简单的指定了文档的字符编码 —— 在这个文档中被允许使用的字符集。utf-8 是一个通用的字符集，它包含了任何人类语言中的大部分的字符。
### 添加作者和描述
许多 `<meta>` 元素包含了`name` 和 `content` 特性：
* `name` 指定了 meta 元素的类型； 说明该元素包含了什么类型的信息。
* `content` 指定了实际的元数据内容。
```html
<meta name="author" content="FS-Luo">
<meta name="description" content="This is my HTML learning notes">
```
&emsp;&emsp;指定作者在某些情况下是很有用的：如果你需要联系页面的作者，问一些关于页面内容的问题。 一些内容管理系统能够自动获取页面作者的信息，然后用于某些用途。
&emsp;&emsp;指定包含关于页面内容的关键字的页面内容的描述是很有用的，因为它可能或让你的页面在搜索引擎的相关的搜索出现得更多 （这些行为术语上被称为 Search Engine Optimization, or SEO.）

## 4. 增加网页图标
1. 将其保存在与网站的索引页面相同的目录中，以.ico格式保存（大多数浏览器将支持更通用的格式，如.gif或.png，但使用ICO格式将确保它能在如Internet Explorer 6一样久远的浏览器显示）
2. 将以下代码添加到HTML `<head>` 中以引用它：
```html
<link rel="shortcut icon" href="favicon.ico" type="image/x-icon">
```

## 5. 在HTML中应用CSS和JavaScript
* 添加 CSS 需要使用 `<link>` 元素
    + `<link>`元素经常位于文档的头部。link元素有2个属性，`rel="stylesheet"` 表明这是文档的样式表，而 `href` 包含了样式表文件的路径。
    ```html
    <link rel="stylesheet" href="my-css-file.css">
    ```
* 添加 JavaScript 需要使用 `<script>` 元素
    + `<script>` 部分没必要非要放在文档头部；实际上，把它放在文档的尾部（在 `</body>`标签之前）是一个更好的选择，这样可以确保在加载脚本之前浏览器已经解析了HTML内容（如果脚本加载某个不存在的元素，浏览器会报错）。
    ```html
    <script src="my-js-file.js"></script>
    ```
    + `<script>` 元素看起来像一个空元素，但它并不是，因此需要一个结束标记。您还可以选择将脚本放入 `<script>` 元素中，而不是指向外部脚本文件。

## 6. 为文档设定主语言
最后，值得一提的是你应该为站点设定语言，可以通过添加lang属性到HTML开始标签中来实现:
```html
<html lang="en-US">
```