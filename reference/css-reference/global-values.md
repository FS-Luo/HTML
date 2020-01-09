# CSS Reference from MDN

# <font style="color: red">global values</font>

## <font style="color: hotpink">1. inherit</font>
* `inherit` 关键字使得元素获取其父元素的计算值。它可以应用于任何CSS属性，包括CSS简写属性 `all`。  
* 对于继承属性，`inherit` 关键字只是增强了属性的默认行为，仅在覆盖其它规则的时候被使用。对于非继承属性，`inherit` 指定的行为通常没有多大意义，一般使用 `initial` 或 `unset` 作为替代。  
* 继承始终来自文档树中的父元素，即使父元素不是包含块。

## <font style="color: hotpink">2. initial</font>
* `initial` 关键字将属性的初始（或默认）值应用于元素，该初始值由浏览器设置。它可以应用于任何CSS属性，包括CSS简写属性 `all`。可使用`all: initial`来将所有CSS属性还原到其初始状态。

## <font style="color: hotpink">3. unset</font>
CSS关键字 `unset` 根据属性是否能继承而有不同的表现形式：
- 如果是**继承属性**，那么 `unset` 的行为类似于 `inherit` 
- 如果是**非继承属性**，则类似于 `initial`。  

它可以应用于任何CSS属性，包括CSS简写属性 `all` 。