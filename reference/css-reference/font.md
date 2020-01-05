# CSS Reference from MDN

# <font style="color: red">font</font>

## <font style="color: hotpink">1. font-family</font>
CSS 属性 `font-family` 允许您通过给定一个有先后顺序的，由字体名或者字体族名组成的列表来为选定的元素设置字体。  
`font-family` 属性指定的是一个优先级从高到低的可选字体列表。对字体的选择是**逐字**进行的，也就是说 **即使某个字符的周围字符都在某个字体中可以显示，但该字符在当前的字体文件中没有适合的图形，那么会继续尝试列表中靠后的字体**。因此应当至少在 `font-family` 列表中添加一个通用的字体族名，保证浏览器可以在无法得到最佳字体的情况下使用一个相对接近的备选字体。

### <font style="color: violet">1.1 语法</font>
```css
/* 一个字体族名和一个通用字体族名 */
font-family: "Gill Sans Extrabold", sans-serif;
font-family: "Goudy Bookletter 1911", sans-serif;

/* 仅有一个通用字体族名 */
font-family: serif;
font-family: sans-serif;
font-family: monospace;
font-family: cursive;
font-family: fantasy;
font-family: system-ui;
font-family: emoji;
font-family: math;
font-family: fangsong;

/* 全局值 */
font-family: inherit;
font-family: initial;
font-family: unset;
```

### <font style="color: violet">1.2 取值</font>
+ `<family-name>`  
一个字体族的名字。例如 "Times" 和 "Helvetica" 都是字体族名。字体族名可以包含空格，但**包含空格时应该加引号**。  
+ `<generic-name>`  
通用字体族名是一种备选机制，用于在指定的字体不可用时给出较为接近的字体。通用字体族名都是关键字，**所以不可以加引号**。 在列表的末尾应该至少有一个通用字体族名。 以下是该属性可能的取值以及他们的定义。
    - `serif`  
    带衬线字体，笔画结尾有特殊的装饰线或衬线。  
    例如： Lucida Bright, Lucida Fax, Palatino, Palatino Linotype, Palladio, URW Palladio, serif.
    - `sans-serif`  
    无衬线字体，即笔画结尾是平滑的字体。  
    例如， Open Sans, Fira Sans, Lucida Sans, Lucida Sans Unicode, Trebuchet MS, Liberation Sans, Nimbus Sans L, sans-serif.
    - `monospace`  
    等宽字体，即字体中每个字宽度相同。  
    例如， Fira Mono, DejaVu Sans Mono, Menlo, Consolas, Liberation Mono, Monaco, Lucida Console, monospace.
    - `cursive`  
    草书字体。这种字体有的有连笔，有的还有特殊的斜体效果。因为一般这种字体都有一点连笔效果，所以会给人一种手写的感觉。  
    例如，Brush Script MT, Brush Script Std, Lucida Calligraphy, Lucida Handwriting, Apple Chancery, cursive.
    - `fantasy`   
    Fantasy 字体主要是那些具有特殊艺术效果的字体。  
    例如，Papyrus, Herculanum, Party LET, Curlz MT, Harrington, fantasy.
    - `system-ui`  
    从浏览器所处平台处获取的默认用户界面字体。
    - `math`  
    针对显示数学相关字符的特殊样式问题而设计的字体：支持上标和下标、跨行括号、嵌套表达式和具有不同含义的 double struck glyph。
    - `emoji`  
    专门用于呈现 Emoji 表情符号的字体。
    - `fangsong`  
    一种汉字字体，介于宋体和楷体之间。这种字体常用于某些政府文件。


## <font style="color: hotpink">2. font-size</font>
font-size CSS 属性指定字体的大小。因为该属性的值会被用于计算em和ex长度单位，定义该值可能改变其他元素的大小。

```css
/* <absolute-size>，绝对大小值 */
font-size: xx-small;
font-size: x-small;
font-size: small;
font-size: medium;
font-size: large;
font-size: x-large;
font-size: xx-large;

/* <relative-size>，相对大小值 */
font-size: larger;
font-size: smaller;

/* <length>，长度值 */
font-size: 12px;
font-size: 0.8em;

/* <percentage>，百分比值 */
font-size: 80%;

font-size: inherit;
```

## <font style="color: hotpink">3. font-style</font>


## <font style="color: hotpink">4. font-weight</font>