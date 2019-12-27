# HTML Text fundamentals
## 1. 基础: 标题和段落
大部分的文本结构由标题和段落组成。
* 标题(Heading)  
`<h1>` `<h2>` `<h3>` `<h4>` `<h5>` `<h6>`。  
每个元素代表文档中不同级别的内容; `<h1>` 表示主标题（the main heading），`<h2>` 表示二级子标题（subheadings），`<h3>` 表示三级子标题（sub-subheadings）等等。
* 段落(Paragraph)  
每个段落是通过 `<p>` 元素标签进行定义的。
```html
<h1>我是主标题</h1>
<h2>我是二级子标题</h2>
<p>我是段落</p>
```
### 1. 编辑结构层次
* 您应该最好只对每个页面使用一次`<h1>` — 这是顶级标题，所有其他标题位于层次结构中的下方。
* 请确保在层次结构中以正确的顺序使用标题。不要使用 `<h3>` 来表示副标题，后面跟 `<h2>` 来表示副副标题 - 这是没有意义的，会导致奇怪的结果。
* 在可用的六个标题级别中，您应该旨在每页使用不超过三个，除非您认为有必要使用更多。具有许多级别的文档（即，较深的标题层次结构）变得难以操作并且难以导航。在这种情况下，如果可能，建议将内容分散在多个页面上。
### 2. 为什么我们需要结构化?
- 用户在阅读网页时，往往会快速浏览以查找相关内容，经常只是阅读开头的标题。
- 对您的网页建立索引的搜索引擎将标题的内容视为影响网页搜索排名的重要关键字。没有标题，您的网页在SEO（搜索引擎优化）方面效果不佳。
- 严重视力障碍者通常不会阅读网页，他们用听力来代替。完成这项工作的软件叫做屏幕阅读器（screen reader）。该软件提供了快速访问给定文本内容的方法。在使用的各种技术中，它们通过朗读标题来提供文档的概述，让用户能快速找到他们需要的信息。如果标题不可用，用户将被迫听到整个文档的大声朗读。
- 使用CSS样式化内容，或者使用JavaScript做一些有趣的事情，你需要包含相关内容的元素，所以CSS / JavaScript可以有效地定位它。  
### 3. 为什么我们需要语义？
* 我们需要确保使用了正确的元素来给予内容正确的意思、作用以及外形。
* 例如，`<h1>` 元素也是一个语义元素，它给出了页面上用来表示顶级标题的角色（或意义）的文本。一般来说，浏览器会给它一个更大的字形来让它看上去像个标题。更重要的是，**它的语义值将以多种方式被使用**，比如通过搜索引擎和屏幕阅读器。

## 2. 列表
### 1. 无序列表(Unordered list)
无序的列表被用来标记每个项目，项目的顺序并不重要 。
```html
<ul>
    <li>item_1</li>
    <li>item_2</li>
    <li>item_3</li>
    <li>...</li>
</ul>
```

### 2. 有序列表(Ordered list)
有序的列表是根据项目的顺序列出来的。
```html
<ol>
    <li>item_1</li>
    <li>item_2</li>
    <li>item_3</li>
    <li>...</li>
</ol>
```

### 3. 嵌套列表(Nesting lists)
将一个列表嵌入到另一个列表是完全可以的。

## 3. 重点强调
### 1. 强调
使用 `<em></em>` (emphasis)元素将文字写成 *斜体* 来强调文本。
### 2. 非常重要
使用 `<strong></strong>` (strong importance)元素将文字写成 **粗体** 来强调重要的文本。
### 3. 斜体字、粗体字、下划线...
* `<i>` : 斜体文字  
* `<b>` : 粗体文字  
* `<u>` : 下划线  
仅仅影响表象而没有语义，被称为表象元素(presentational elements)。  

**关于下划线的警告**：人们很容易把下划线和超链接联系起来。因此，在Web上，最好只在链接上使用下划线。当语义适合时使用`<u>`元素，但是有时候在Web上用CSS改变下划线默认的的样式更加合适。



# Advanced text formatting
## 1. 描述列表
**描述列表** (description list): 用于标记一组项目及其相关描述，例如一组术语和定义，或者是一组问题和答案等。  
+ 描述列表：`<dl></dl>`
+ 列表中的每一项： `<dt></dt>` (description term)
+ 每个描述： `<dd></dd>` (description description)  
一个列表项 `<dt></dt>` 可以同时拥有多个描述 `<dd></dd>`。  
浏览器的默认样式会在描述列表的描述部分和描述术语之间产生缩进。

## 2. 引用
### 1. 块引用
&emsp;&emsp;如果一个块级内容（一个段落、多个段落、一个列表等）从其他地方被引用，你应该把它用 `<blockquote>` 元素包裹起来表示，并且在 `cite` 属性里用URL来指向引用的资源。浏览器在渲染块引用时默认会增加缩进，作为引用的一个指示符。
例如：
```html
<blockquote cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote"><p>The <strong>HTML <code>&lt;blockquote&gt;</code> Element</strong>(or <em>HTML Block Quotation Element</em>) indicates that the enclosed text is an extended quotation.</p></blockquote>
```
<blockquote cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote"><p>The <strong>HTML <code>&lt;blockquote&gt;</code> Element</strong>(or <em>HTML Block Quotation Element</em>) indicates that the enclosed text is an extended quotation.</p></blockquote>

### 2. 行内引用
行内元素用同样的方式工作，除了使用<q>元素。浏览器默认将其作为普通文本放入引号内表示引用。
例如：
```html
<p>The quote element--<code>&lt;q&gt;</code>--is <q cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q">intended for short quotations that don't require paragraph breaks.</q></p>
```
<p>The quote element--<code>&lt;q&gt;</code>--is <q cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q">intended for short quotations that don't require paragraph breaks.</q></p>

### 3. 引文
&emsp;&emsp;`cite` 属性内容不会被浏览器显示、屏幕阅读器阅读，需使用 JavaScript 或 CSS，浏览器才会显示 `cite`的内容。如果你想要确保引用的来源在页面上是可显示的，更好的方法使用 `<cite></cite>`元素。引文默认的字体样式为斜体。

```html
<p>According to the <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote"><cite>MDN blockquote page</cite></a>:</p>

<blockquote cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote"><p>The <strong>HTML <code>&lt;blockquote&gt;</code> Element</strong>(or <em>HTML Block Quotation Element</em>) indicates that the enclosed text is an extended quotation.</p></blockquote>
```
<p>According to the <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote"><cite>MDN blockquote page</cite></a>:</p>

<blockquote cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/blockquote"><p>The <strong>HTML <code>&lt;blockquote&gt;</code> Element</strong>(or <em>HTML Block Quotation Element</em>) indicates that the enclosed text is an extended quotation.</p></blockquote>

```html
<p>The quote element--<code>&lt;q&gt;</code>--is <q cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q">intended for short quotations that don't require paragraph breaks.</q> -- <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q"><cite>MDN q page</cite></a></p>
```
<p>The quote element--<code>&lt;q&gt;</code>--is <q cite="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q">intended for short quotations that don't require paragraph breaks.</q> -- <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/q"><cite>MDN q page</cite></a></p>

## 3. 缩略语
&emsp;&emsp;在web上看到的相当常见的元素是 `<abbr></abbr>` ——它常被用来包裹一个缩略语或缩写，并在 `title` 属性中提供缩写的解释，当光标移动到项目上时会出现提示。
```html
<p>我们使用 <abbr title="超文本标记语言(Hypertext Markup Language)">HTML</abbr> 来组织网页文档。</p>
```
<p>我们使用 <abbr title="超文本标记语言(Hypertext Markup Language)">HTML</abbr> 来组织网页文档。</p>

## 4. 标记联系方式
&emsp;&emsp;HTML有个用于标记联系方式的元素——`<address></address>`，它仅仅包含你的联系方式。但要记住的一点是，`<address>`元素是为了标记编写HTML文档的人的联系方式，而不是任何其他的内容。

## 5. 上标和下标
&emsp;&emsp;当你使用日期、化学方程式、和数学方程式时会偶尔使用上标和下标。 `<sup></sup>` 和 `<sub></sub>`元素可以解决这样的问题。
例如：
```html
<p>咖啡因的化学式是C<sub>8</sub>H<sub>10</sub>N<sub>4</sub>O<sub>2</sub></p>
```
<p>咖啡因的化学式是C<sub>8</sub>H<sub>10</sub>N<sub>4</sub>O<sub>2</sub></p>

## 6. 展示计算机代码
有大量的HTML元素可以来标记计算机代码：
* `<code></code>` : 用于标记计算机通用代码。
* `<pre></pre>` : 用于保留空白字符(通常用于代码块)，空白将会以与文本编辑器中相同的格式渲染出来。
* `<var></var>` : 用于标记具体变量名。
* `<kbd></kbd>` : 用于标记输入电脑的键盘（或其他类型）输入。
* `<samp></samp>` : 用于标记计算机程序的输出。

```html
<pre><code>const para = document.querySelector('p');

para.onclick = function(){
    alert('噢，噢，噢，别点我了。');
}</code></pre>

<p>请不要使用 <code>&lt;font&gt;</code> 、 <code>&lt;center&gt;</code> 等表象元素。</p>

<p>在上述的 JavaScript 示例中，<var>para</var> 表示一个段落元素。</p>


<p>按 <kbd>Ctrl</kbd>/<kbd>Cmd</kbd> + <kbd>A</kbd> 选择全部内容。</p>

<pre>$ <kbd>ping mozilla.org</kbd>
<samp>PING mozilla.org (63.245.215.20): 56 data bytes
64 bytes from 63.245.215.20: icmp_seq=0 ttl=40 time=158.233 ms</samp></pre>
```
<pre><code>const para = document.querySelector('p');

para.onclick = function(){
    alert('噢，噢，噢，别点我了。');
}</code></pre>

<p>请不要使用 <code>&lt;font&gt;</code> 、 <code>&lt;center&gt;</code> 等表象元素。</p>

<p>在上述的 JavaScript 示例中，<var>para</var> 表示一个段落元素。</p>


<p>按 <kbd>Ctrl</kbd>/<kbd>Cmd</kbd> + <kbd>A</kbd> 选择全部内容。</p>

<pre>$ <kbd>ping mozilla.org</kbd>
<samp>PING mozilla.org (63.245.215.20): 56 data bytes
64 bytes from 63.245.215.20: icmp_seq=0 ttl=40 time=158.233 ms</samp></pre>

## 7. 标记时间和日期
&emsp;&emsp;HTML 还支持将时间和日期标记为可供机器识别的格式的 `<time></time>` 元素。为什么需要这样做？因为世界上有许多种书写日期的格式，但是这些不同的格式不容易被电脑识别 — 假如你想自动抓取页面上所有事件的日期并将它们插入到日历中，`<time>` 元素允许你附上清晰的、可被机器识别的时间/日期来实现这种需求。

```html
<!-- 标准简单日期 -->
<time datetime="2016-01-20">20 January 2016</time>
<!-- 只包含年份和月份-->
<time datetime="2016-01">January 2016</time>
<!-- 只包含月份和日期 -->
<time datetime="01-20">20 January</time>
<!-- 只包含时间，小时和分钟数 -->
<time datetime="19:30">19:30</time>
<!-- 还可包含秒和毫秒 -->
<time datetime="19:30:01.856">19:30:01.856</time>
<!-- 日期和时间 -->
<time datetime="2016-01-20T19:30">7.30pm, 20 January 2016</time>
<!-- 含有时区偏移值的日期时间 -->
<time datetime="2016-01-20T19:30+01:00">7.30pm, 20 January 2016 is 8.30pm in France</time>
<!-- 调用特定的周 -->
<time datetime="2016-W04">The fourth week of 2016</time>
```