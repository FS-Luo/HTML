# CSS Reference from MDN

# <font style="color: red">border</font>

## <font style="color: hotpink">1. border-bottom</font>
`border-bottom` 简写属性把 **下边框** 的所有属性： `border-bottom-color`，`border-bottom-style` 与 `border-bottom-width` 设置到了一个声明中，描述了元素的下边框样式。三个简写属性可以任意顺序排列, 并且任意一个都可以被省略，所有未被显式定义的参数都将设置为默认值:
- `border-bottom-width`: `medium`
- `border-bottom-style`: `none`
- `border-bottom-color`: `currentcolor`
### <font style="color: violet">1.1 border-bottom-color</font>

### <font style="color: violet">1.2 border-bottom-style</font>
```css
/* Keyword values */
border-bottom-style: none;
border-bottom-style: hidden;
border-bottom-style: dotted;
border-bottom-style: dashed;
border-bottom-style: solid;
border-bottom-style: double;
border-bottom-style: groove;
border-bottom-style: ridge;
border-bottom-style: inset;
border-bottom-style: outset;

/* Global values */
border-bottom-style: inherit;
border-bottom-style: initial;
border-bottom-style: unset;
```

<span style="border-bottom-style: none">none</span>
<span style="border-bottom-style: hidden">hidden</span>
<span style="border-bottom-style: dotted">dotted</span>
<span style="border-bottom-style: dashed">dashed</span>
<span style="border-bottom-style: solid">solid</span>  
<span style="border-bottom-style: double">double</span>
<span style="border-bottom-style: groove">groove</span>
<span style="border-bottom-style: ridge">ridge</span>
<span style="border-bottom-style: inset">inset</span>
<span style="border-bottom-style: outset">outset</span>

### <font style="color: violet">1.3 border-bottom-width</font>
```css
/* Keyword values */
border-bottom-width: thin;
border-bottom-width: medium;
border-bottom-width: thick;

/* <length> values */
border-bottom-width: 10em;
border-bottom-width: 3vmax;
border-bottom-width: 6px;

/* Global keywords */
border-bottom-width: inherit;
border-bottom-width: initial;
border-bottom-width: unset;
```

<span style="width: 4em; border-bottom-style: solid; border-bottom-width: thin; ">thin</span>
<span style="width: 4em; border-bottom-style: solid; border-bottom-width: medium;">medium</span>
<span style="width: 4em; border-bottom-style: solid; border-bottom-width: thick;">thick</span>
