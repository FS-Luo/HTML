# HTML Form

## 1. Web表单是什么？
**Web表单** 是用户与网站或应用程序之间交互的主要方式之一。表单允许用户输入数据，该数据通常发送到Web服务器进行处理和存储，或在客户端使用它以某种方式立即更新界面。

Web表单的HTML由一个或多个表单控件（也称为部件）以及一些有助于构建整体表单的其他元素组成-它们通常称为HTML表单。控件可以是单行或多行文本字段，下拉框，按钮，复选框或单选按钮，并且大多使用 `<input>` 元素创建，尽管也有一些其他元素需要学习。还可以对表单控件进行编程，以强制输入特定格式或值（表单验证），并与文本标签配对，以便于向正常用户或有视力缺陷的用户描述。

## 2. HTML表单元素
### 2.1 `<form>` 元素
所有表单都以一个 `<form>` 元素开始，这个元素正式定义了一个表单。就像 `<div>` 元素或 `<p>` 元素，它是一个容器元素，但也支持一些特定的属性来配置表单的行为方式。它的所有属性都是可选的，但实践中最好至少要设置 `action` 属性和 `method` 属性。
- `action` 属性定义了在提交表单时，应该把所收集的数据发送给谁(/那个模块)(URL)去处理。
- `method` 属性定义了发送数据的HTTP方法(可以是“get”或“post”)。

**注意:** 严格禁止在一个表单内嵌套另一个表单。嵌套会使表单的行为不可预知，而这取决于正在使用的浏览器。

### 2.2 `<label>` 元素
`<label>` 元素表示用户界面中某个元素的说明。

将一个 `<label>` 和一个 `<input>` 元素放在一起会有以下几点好处：
- 标签文本不仅与其相应的文本输入框在视觉上相关联; 也以编程方式与它相关联。 这意味着，当用户点击到表单输入时，屏幕阅读器可以读出标签，使用辅助技术的用户更容易理解应输入哪些数据.
- 单击 **input框本身** 或者 **关联的标签** 都能激活/聚焦 input框。这能增加input框的命中区域，为激活input框提供了方便，包括那些使用触摸屏设备的。

`<label>` 与 `<input>` 的匹配方式：
- 显示匹配：`<label>`元素的 **`for`** 属性和 `<input>` 元素的 **`id`** 属性的值保持一致。
- 隐式匹配：直接将 `<input>` 元素放入 `<label>` 元素内，无需使用 `for` 和 `id` 属性。

**注意：**  
+ 当点击或者触碰（tap）一个与表单控件相关联的 `<label>` 时，关联的控件的 `click` 事件也会触发。
+ 不要在 `<label>` 元素内放置 `<a>`, `<button>` 等元素！因为这会干扰用户激活与 `<label>` 相关联的 `<input>` 元素。
+ 也不要在 `<label>` 元素内放置标题元素（`<h1>`等），这会干扰许多辅助技术。如需类似的视觉效果，应该用CSS伪类更改样式并应用到 `<label>` 元素。
+ 如果一个表单的一部分需要一个标题，此时应该使用 `<legend>` 元素做标题，并将它放在 `<fieldset>` 元素中。
+ 如果 `<input>` 元素含有属性 `type="button"` 以及有效的 `value` 属性，那么就不需要添加 `<label>`元素，否则会干扰辅助技术解析。同理 `<button>` 元素也不需要 label。

### 2.3 `<input>` 元素
`<input>` 元素用于为Web表单创建交互式控件，以便接受来自用户的数据。根据设备和用户代理的不同，可以使用多种类型的输入数据和控件。由于输入类型和属性的组合数量之多，`<input>`元素是所有HTML中最强大，最复杂的元素之一。

`<input>` 的工作方式根据 `type` 属性的值的不同而有很大不同。 如果未指定此属性，则采用的默认类型为 `text`。

**`type` 属性**
type|description|basic examples
:-:|:-:|:-
`button`|默认显示为空的按钮。|<input type="button">
`checkbox`|复选框，允许 选择 / 取消选择。|<input type="checkbox">
`color`|用于指定颜色的控件；激活时会打开颜色选择器。|<input type="color">
`date`|用于输入日期（年-月-日）的控件；既可以输入，也可以选择。|<input type="date">
`datetime-local`|用于输入日期和时间（无时区）的控件。|<input type="datetime-local">
`email`|用于编辑电子邮件地址的字段。看起来像普通文本输入，但在支持的浏览器和带有动态键盘的设备中具有验证参数和相关的键盘。|<input type="email">
`file`|允许用户选择文件的控件。使用 `accept `属性定义控件可以选择的文件类型。|<input type="file">
`hidden`|不显示其外观的控件，但其值已提交给服务器。|<input type="hidden">
`image`|图形提交按钮，显示 `src` 属性定义的图像。如果 `src` 属性无效，则显示 `alt` 属性的值。|<input type="image">
`month`|用于输入年、月的控件。|<input type="month">
`number`|输入数字的控件；在设备支持时会显示微调器，并且具备默认验证。在带有动态键盘的某些设备中显示数字键盘。|<input type="number">
`password`|值会被遮盖的单行文本字段。如果网站不安全，将会警告用户。|<input type="password">
`radio`|单选按钮，允许从具有相同 `name` 属性的多个选项中选择一个值。|<input type="radio">
`range`|用于输入精确值不重要的数字的控件；默认显示为范围的中间值。结合 `min` 和 `max` 属性定义可接受值的范围。|<input type="range">
`reset`|将表单内容重置为默认值的按钮。不建议轻易使用。|<input type="reset">
`search`|用于输入搜索字符串的单行文本字段。换行符会自动从输入值中删除。在支持的浏览器中会包含一个删除图标，可用于清除该字段。 在带有动态键盘的设备上，会显示'Search'图标而不是'Enter'键。|<input type="search">
`submit`|提交表单的按钮。|<input type="submit">
`tel`|输入电话号码的控件。在带有动态键盘的设备中显示电话键盘。|<input type="tel">
`text`|默认值，单行文本字段。换行符会自动从输入值中删除。|<input type="text">
`time`|用于输入时间（无时区）的控件。|<input type="time">
`url`|输入URL的字段。看起来像文本输入，但在支持的浏览器和带有动态键盘的设备中具有验证参数和相关的键盘。|<input type="url">
`week`|用于输入年-周号（无时区）的控件。|<input type="week">


### 2.4 `<textarea>`元素
`<textarea>` 元素表示多行纯文本编辑控件，在您希望允许用户输入大量自由格式文本（例如，评论或反馈）时很有用。

+ `id` 属性：允许 `<textarea>` 与 `<label>` 元素关联。
+ `name` 属性：当提交表单时，`name` 属性的值会设置提交给服务器的数据点的名称。
+ `cols` 和 `rows` 属性：用于指定 `<textarea>` 的确切大小。设置这些值是保持一致性的一个好主意，因为浏览器的默认设置可能有所不同。
  - `cols` 属性：文本控件的可见宽度，以平均字符宽度为单位。 如果指定，则必须为正整数。如果未指定，则默认值为20。
  - `rows` 属性：文本控件的可见行数。
+ `maxlength` 和 `minlength`：`maxlength` 指定`<textarea>` 允许包含的最大字符数。还可以使用 `minlength` 设置被视为有效的最小长度，提交时浏览器会验证，如果小于该长度会提示无效。
+ `required` 属性：使用 `required` 属性指定 `<textarea>` 如果为空将不会被提交。这为 `<textarea>` 提供了简单的验证。
+ `<textarea>`开始标签和结束标签之间的内容是 `<textarea>`的默认内容。`<textarea>` 不支持 `value` 属性。而 `<input>` 的默认内容只能使用 `value` 属性设置。

### 2.5 `<button>` 元素
`<button>` 元素表示表单中可点击的按钮，也可以在需要简单、标准按钮功能的文档中的任何位置使用。 默认情况下，HTML按钮通常以基于运行平台（Win7, Win10, Mac OSX等）的样式来显示，但可以使用CSS更改按钮的外观。

+ `type` 属性：
  - `submit` ：此按钮将表单数据提交给服务器。如果未指定属性，或者属性动态更改为空值或无效值，则此值为默认值。
  - `reset` ：此按钮重置所有组件为初始值。
  - `button` ：此按钮没有默认行为。它可以有与元素事件相关的客户端脚本，当事件出现时可触发。
  - `menu` ：此按钮打开一个由指定 `<menu>` 元素进行定义的弹出菜单。

### 2.6 `<fieldset>` 和 `<legend>` 元素
`<fieldset>` 元素是一种方便的用于创建一组具有相同目的的小部件的方式，出于样式和语义的目的。 在 `<fieldset>` 元素中加上 `<legend>` 元素，相当于给这组小部件设置标题。`<legend>` 的文本内容正式地描述了 `<fieldset>` 里所含有部件的用途。

+ `<fieldset>` 元素：  
用于对Web表单内的多个控件以及标签（`<label>`）进行分组。
+ `<legend>` 元素：
用于设置其父元素 `<fieldset>` 的内容的标题。

## 3. 用于表单的通用HTML结构
除了用于HTML表单的特定结构之外，还可以使用其他的HTML通用结构来构造一个HTML表单。

+ 用 `<div>` 元素包装标签和它的小部件是很常见的做法。`<p>` 元素也经常被使用，HTML列表也是如此（列表在构造多个复选框或单选按钮时最为常见）。
+ 除了 `<fieldset>` 元素之外，使用HTML标题（例如 `<h1>`、`<h2>`）和分段（如 `<section>` ）来构造一个复杂的表单也是一种常见的做法。

通常可以从功能上划分开并分别包含在 `<section>` 元素中，以及用 `<fieldset>` 来包含单选按钮。