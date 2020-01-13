# CSS values and units

## 1. 数字，长度和百分比
数值数据的类型：
+ `<integer>` : 整数。
+ `<number>` : 小数——可能带有小数部分，也可能没有。
+ `<dimension>` : 包括 `<length>`, `<angle>`, `<time>`, `<resolution>`类型。它有一个附加的单位。
+ `<percentage>` : 相对于其他值的一部分。

### 1.1 `<length>`长度
CSS中有两种类型的长度：**相对长度** 和 **绝对长度**。重要的是要知道它们之间的区别，以便理解他们控制的元素将变得有多大。

+ 绝对长度单位  
绝对长度单位——它们与其他任何东西都没有关系，通常被认为总是相同的大小。
<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">单位</th>
   <th scope="col">名称</th>
   <th scope="col">等价换算</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>cm</code></td>
   <td>厘米</td>
   <td>1cm = 96px/2.54</td>
  </tr>
  <tr>
   <td><code>mm</code></td>
   <td>毫米</td>
   <td>1mm = 1/10th of 1cm</td>
  </tr>
  <tr>
   <td><code>Q</code></td>
   <td>四分之一毫米</td>
   <td>1Q = 1/40th of 1cm</td>
  </tr>
  <tr>
   <td><code>in</code></td>
   <td>英寸</td>
   <td>1in = 2.54cm = 96px</td>
  </tr>
  <tr>
   <td><code>pc</code></td>
   <td>十二点活字</td>
   <td>1pc = 1/16th of 1in</td>
  </tr>
  <tr>
   <td><code>pt</code></td>
   <td>点</td>
   <td>1pt = 1/72th of 1in</td>
  </tr>
  <tr>
   <td><code>px</code></td>
   <td>像素</td>
   <td>1px = 1/96th of 1in</td>
  </tr>
 </tbody>
</table>

+ 相对长度单位  
相对长度单位相对于其他一些东西，比如父元素的字体大小，或者视图端口的大小。使用相对单位的好处是，经过一些仔细的规划，您可以使文本或其他元素的大小与页面上的其他内容相对应。
  - `em` 是“相对于当前父元素的字体大小”。  
  - `rem` 是“相对于根元素的字体大小”，根元素即 `<html>`，如果未设置根元素的字体大小，则通常是浏览器默认的 `1em=16px` 。
<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">单位</th>
   <th scope="col">相对于</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td><code>em</code></td>
   <td>父元素的字体大小</td>
  </tr>
  <tr>
   <td><code>ex</code></td>
   <td>字符“x”的高度</td>
  </tr>
  <tr>
   <td><code>ch</code></td>
   <td>数字“0”的宽度</td>
  </tr>
  <tr>
   <td><code>rem</code></td>
   <td>根元素的字体大小</td>
  </tr>
  <tr>
   <td><code>lh</code></td>
   <td>元素的line-height</td>
  </tr>
  <tr>
   <td><code>vw</code></td>
   <td>视窗宽度的1%</td>
  </tr>
  <tr>
   <td><code>vh</code></td>
   <td>视窗高度的1%</td>
  </tr>
  <tr>
   <td><code>vmin</code></td>
   <td>视窗较小尺寸的1%</td>
  </tr>
  <tr>
   <td><code>vmax</code></td>
   <td>视图大尺寸的1%</td>
  </tr>
 </tbody>
</table>

### 1.2 百分比
在许多情况下，百分比与长度的处理方法是一样的。百分比总是相对于其他值设置的。注意，虽然许多值接受长度或百分比，但也有一些值只接受长度。您可以在MDN属性引用页面上看到它能接受哪些值。如果允许的值包括 `<length-percent>` ，则可以使用长度或百分比。如果允许的值只包含 `<length>` ，则不能使用百分比。

### 1.3 数字
有些值接受数字，不添加任何单位。接受无单位数字的属性的一个例子是不透明度属性（ `opacity` ），它控制元素的不透明度，接受0(完全透明)和1(完全不透明)之间的数字。

**注意：**`opacity` 与 `rgba()` 、 `hsla()` 中alpha通道有一个关键的区别，即 `opacity` 设置元素里所有的内容的透明度，而alpha通道仅设置了颜色的透明度。

## 2. 颜色
+ 颜色关键字
+ 十六进制RGB值
+ RGB和RGBA的值
+ HSL和HSLA的值

## 3. 图片
`<image>` 数据类型用于图像为有效值的任何地方。它可以是一个通过 `url()` 函数指向的实际图像文件，也可以是一个渐变。

## 4. 位置
`<position>` 数据类型表示一组2D坐标，用于定位一个元素，如背景图像(通过 `background-position`)。

## 5. 字符串和标识符
一些属性的值可以是关键字，这些关键字被称为为 **标识符** ，一个CSS可以理解的特殊值。还有一些值被用引号括起来，被称为 **字符串** 。

## 6. 函数
在编程中，函数是一段可重用的代码，可以多次运行，以完成重复的任务，对开发人员和计算机都是如此。函数通常与JavaScript、Python或C++等语言相关联，但它们也以属性值的形式存在于CSS中。我们已经在颜色部分看到了函数的作用—— `rgb()`、`hsl()` 等。用于从文件返回图像的值—— `url()` 也是一个函数。

行为更类似于传统编程语言的值是 `calc()` 函数。这个函数使您能够在CSS中进行简单的计算。如果您希望计算出在为项目编写CSS时无法定义的值，并且需要浏览器在运行时为您计算出这些值，那么它特别有用。
