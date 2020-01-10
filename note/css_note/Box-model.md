# The box model
## 1. 块级盒子（Block box）和内联盒子（Inline box）
**块级盒子** 的行为如下:
- 盒子会在内联的方向上扩展并占据父容器在该方向上的所有可用空间，在绝大数情况下意味着盒子会和父容器一样宽。
- 每个盒子都会换行。
- `width` 和 `height` 属性可以发挥作用
- 内边距（`padding`）, 外边距（`margin`） 和 边框（`border`） 会将其他元素从当前盒子周围“推开”。

**内联盒子** 的行为如下:
- 盒子不会产生换行。
- `width` 和 `height` 属性将不起作用。
- 内边距、外边距以及边框会被应用但是不会把其他处于 inline 状态的盒子推开。

除非特殊指定，默认情况下
+ 标题(`<h1>`等)和段落(`<p>`)等属于块级盒子。
+ 用做链接的 `<a>` 元素、`<span>`、 `<em>` 以及 `<strong>` 属于内联盒子。

## 2. CSS 盒模型
### 2.1 盒模型的组成部分
CSS中组成一个块级盒子需要:
- **Content box**: 这个区域是用来显示内容，大小可以通过设置 `width` 和 `height`。
- **Padding box**: 包围在内容区域外部的空白区域； 大小通过 `padding` 相关属性设置。
- **Border box**: 边框盒包裹内容和内边距。大小通过 `border` 相关属性设置。
- **Margin box**: 这是最外面的区域，是盒子和其他元素之间的空白区域。大小通过 `margin` 相关属性设置。  

如下图：
<img alt="" title="box model" src="images/box-model.png">

### 2.2 盒模型的种类
* 标准盒模型  
`width` 和 `height`实际设置的是 *content box*。而整个盒子的大小还需要加上 `padding` 和 `border`。  
    - 公式：  
    盒子宽度 = `width` + `padding` * 2 + `border` * 2  
    盒子高度 = `height` + `padding` * 2 + `border` * 2

* 替代（IE）盒模型  
`width` 和 `height`实际设置的就是整个盒子的宽度和高度。而 *content box* 的大小需要扣除 `padding` 和 `border`。

* **注意**: `margin` 不计入实际大小 —— 当然，它会影响盒子在页面所占空间，但是影响的是盒子外部空间。盒子的范围到边框为止，不会延伸到margin。

例如：  
```css
.box {
    width: 350px;
    height: 150px;
    margin: 25px;
    padding: 25px;
    border: 5px solid black;
}
```
标准盒模型：
- 盒子宽度 = `width` + `padding` * 2 + `border` * 2 = 410px
- 盒子高度 = `height` + `padding` * 2 + `border` * 2 = 210px
- 内容盒子宽度 = `width` = 350px
- 内容盒子高度 = `height` = 150px
<img alt="" title="standard box model" src="images/standard-box-model.png">

替代盒模型：
- 盒子宽度 = `width` = 350px
- 盒子高度 = `height` = 150px
- 内容盒子宽度 = `width` - `padding` * 2 - `border` * 2 = 290px
- 内容盒子高度 = `height` - `padding` * 2 - `border` * 2 = 90px
<img alt="" title="alternate box model" src="images/alternate-box-model.png">

默认浏览器会使用标准模型。如果需要使用替代模型，您可以通过为其设置 `box-sizing: border-box `来实现。 

如果你希望所有元素都使用替代模式，而且确实很常用，设置 `box-sizing` 在 `<html>` 元素上，然后设置所有元素继承该属性，正如下面的例子。
```css
html {
  box-sizing: border-box;
}
*, *::before, *::after {
  box-sizing: inherit;
}
```

## 3. 外边距，内边距，边框
### 3.1 外边距 `margin`
外边距是盒子周围一圈看不到的空间。它会把其他元素从盒子旁边推开。 外边距属性值可以为正也可以为负。设置负值会导致和其他内容重叠。无论使用标准模型还是替代模型，外边距总是在计算可见部分后额外添加。

我们可以使用 `margin` 属性一次控制一个元素的所有边距，或者每边单独使用等价的普通属性控制：
- `margin-top`
- `margin-right`
- `margin-bottom`
- `margin-left`

**常规语法**
```css
/*单值语法  所有边缘 */
margin: 1em; 
/*二值语法  纵向 横向 */
margin: 5% auto; 
/*三值语法 上 横向 下*/
margin: 1em auto 2em; 
/*四值语法 上 右 下 左*/
margin: 2px 1em 0 auto;
```
**外边距折叠**  
理解外边距的一个关键是外边距折叠的概念。如果你有两个外边距相接的元素，这些外边距将合并为一个外边距，即最大的单个外边距的大小。  
有许多规则规定了什么时候外边距会折叠，什么时候不会折叠。现在首先要记住的事情是，外边距会折叠这个事情。如果你用外边距创建空间而没有得到你想要的效果，那这可能就是这个原因。

### 3.2 边框 `border`
边框是在边距和填充框之间绘制的。如果您正在使用标准的盒模型，边框的大小将添加到框的宽度和高度。如果您使用的是替代盒模型，那么边框的大小会使内容框更小，因为它会占用一些可用的宽度和高度。

为边框设置样式：
+ 使用 `border` 属性一次设置所有四个边框的颜色、样式、宽度。
+ 分别设置每边的颜色、样式、宽度，可以使用：
  - `border-top`
  - `border-right`
  - `border-bottom`
  - `border-left`
+ 分别设置所有边的颜色、样式、宽度，可以使用：
  - `border-color`
  - `border-style`
  - `border-width`
+ 设置单边的颜色、样式、宽度，可以使用最细粒度的普通属性之一：
  - `border-top-width`
  - `border-top-style`
  - `border-top-color`
  - `border-right-width`
  - `border-right-style`
  - `border-right-color`
  - `border-bottom-width`
  - `border-bottom-style`
  - `border-bottom-color`
  - `border-left-width`
  - `border-left-style`
  - `border-left-color`

### 3.3 内边距 `padding`
内边距位于边框和内容区域之间。与外边距不同，没有负数的内边距，所以值必须是0或正值。应用于元素的任何背景都将显示在内边距后面，内边距通常用于将内容推离边框。  
我们可以使用 `padding` 简写属性控制元素所有边，或者每边单独使用等价的普通属性：
- `padding-top`
- `padding-right`
- `padding-bottom`
- `padding-left`

## 4. 内联盒子
以上所有的方法都完全适用于**块级盒子**。部分属性也可以应用于**内联盒子**。 

例如由 `<span>` 元素创建的内联盒子：宽度和高度被忽略了，外边距、内边距和边框是生效的，但它们不会改变其他内容与内联盒子的关系，因此内边距和边框会与段落中的其他单词重叠。

**`display: inline-block`**  
它在内联和块之间提供了一个中间状态。这对于以下情况非常有用：您不希望一个项切换到新行，但希望它可以设定宽度和高度，并避免上面看到的重叠。 
既可以实现块级盒子的部分效果：
- 设置 `width` 和 `height` 属性会生效。
- `padding`, `margin`, 以及 `border` 会推开其他元素。

也保留了内联盒子的部分效果：
- 不会跳转到新行。

应用实例：  
当您想要通过添加内边距使链接具有更大的命中区域时，这是很有用的。`<a>` 是像 `<span>` 一样的内联元素，你可以使用 `display: inline-block` 来设置内边距，让用户更容易点击链接。