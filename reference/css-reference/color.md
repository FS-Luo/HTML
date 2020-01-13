# `<color>`
CSS 数据类型 `<color>` 表示一种标准RGB色彩空间（sRGB color space）的颜色。一种颜色可以用以下任意的方式来描述：
- 使用一个关键字
- 使用RGB立体坐标（RGB cubic-coordinate）系统（以“#”加十六进制或者 rgb() 和 rgba() 函数表达式的形式）
- 使用HSL圆柱坐标（HSL cylindrical-coordinate）系统（以 hsl() 和 hsla() 函数表达式的形式）  

一个与 sRGB 空间中色彩相关联的 `<color>` 值也有一个阿尔法通道（alpha-channel）坐标，即 *透明度值*，来标明颜色如何与它的背景色混合（composite）。

## 1. 色彩关键字
在使用关键字时有几个需要留意的注意事项：
+ 除了通常的 16 个 HTML 基本颜色，其它的不能被用于 HTML 。HTML 将通过一个特定的计算程序转换这些未知的值，这将导致成为完全不同的颜色。这些关键字应只被用于 SVG 和 CSS 。
+ 未知的关键字会让 CSS 属性无效。无效的属性将被忽略，该颜色将没有作用。这是一个和 HTML 相比不同的行为。
+ 未使用关键字定义的颜色在 CSS 中有任意的透明度，它们是单实色。
+ 色彩关键字中所有的 `grey` 与 `gray` 可以相互替换。
+ 虽然关键字的名称取自常见的 X11 颜色名，然而由于生产商为具体的硬件所做的定制，颜色可能与 X11 系统上相应的颜色有所偏差。

<table id="colors_table">
 <thead>
  <tr>
   <th scope="col">规范</th>
   <th scope="col">颜色</th>
   <th scope="col">关键字</th>
   <th scope="col">RGB 十六进制数</th>
   <th scope="col">实样</th>
  </tr>
 </thead>
 <tbody>
  <tr style="position: relative;">
   <td rowspan="16"><a class="external" href="https://www.w3.org/TR/CSS1/" hreflang="en" lang="en" rel="noopener" title="CSS Level&nbsp;1">CSS Level&nbsp;1</a></td>
   <td style="background: #000;"></td>
   <td style="text-align: center;"><code>black</code>（黑）</td>
   <td><code>#000000</code></td>
   <td style="background: black;"></td>
  </tr>
  <tr>
   <td style="background: #C0C0C0;"></td>
   <td style="text-align: center;"><code>silver</code>（银）</td>
   <td><code>#c0c0c0</code></td>
   <td style="background: silver;"></td>
  </tr>
  <tr>
   <td style="background: #808080;"></td>
   <td style="text-align: center;"><code>gray</code><sup><a href="#1" title="color_value#1">[*]</a></sup>（灰）</td>
   <td><code>#808080</code></td>
   <td style="background: gray;"></td>
  </tr>
  <tr>
   <td style="background: #FFF;"></td>
   <td style="text-align: center;"><code>white</code>（白）</td>
   <td><code>#ffffff</code></td>
   <td style="background: white;"></td>
  </tr>
  <tr>
   <td style="background: #800000;"></td>
   <td style="text-align: center;"><code>maroon</code>（褐）</td>
   <td><code>#800000</code></td>
   <td style="background: maroon;"></td>
  </tr>
  <tr>
   <td style="background: #F00;"></td>
   <td style="text-align: center;"><code>red</code>（红）</td>
   <td><code>#ff0000</code></td>
   <td style="background: red;"></td>
  </tr>
  <tr>
   <td style="background: #800080;"></td>
   <td style="text-align: center;"><code>purple</code>（紫）</td>
   <td><code>#800080</code></td>
   <td style="background: purple;"></td>
  </tr>
  <tr>
   <td style="background: #F0F;"></td>
   <td style="text-align: center;"><code>fuchsia</code>（紫红）</td>
   <td><code>#ff00ff</code></td>
   <td style="background: fuchsia;"></td>
  </tr>
  <tr>
   <td style="background: #008000;"></td>
   <td style="text-align: center;"><code>green</code>（绿）</td>
   <td><code>#008000</code></td>
   <td style="background: green;"></td>
  </tr>
  <tr>
   <td style="background: #0F0;"></td>
   <td style="text-align: center;"><code>lime</code>（绿黄）</td>
   <td><code>#00ff00</code></td>
   <td style="background: lime;"></td>
  </tr>
  <tr>
   <td style="background: #808000;"></td>
   <td style="text-align: center;"><code>olive</code>（橄榄绿）</td>
   <td><code>#808000</code></td>
   <td style="background: olive;"></td>
  </tr>
  <tr>
   <td style="background: #FF0;"></td>
   <td style="text-align: center;"><code>yellow</code>（黄）</td>
   <td><code>#ffff00</code></td>
   <td style="background: yellow;"></td>
  </tr>
  <tr>
   <td style="background: #000080;"></td>
   <td style="text-align: center;"><code>navy</code>（藏青）</td>
   <td><code>#000080</code></td>
   <td style="background: navy;"></td>
  </tr>
  <tr>
   <td style="background: #00F;"></td>
   <td style="text-align: center;"><code>blue</code>（蓝）</td>
   <td><code>#0000ff</code></td>
   <td style="background: blue;"></td>
  </tr>
  <tr>
   <td style="background: #008080;"></td>
   <td style="text-align: center;"><code>teal</code>（青）</td>
   <td><code>#008080</code></td>
   <td style="background: teal;"></td>
  </tr>
  <tr>
   <td style="background: #0FF;"></td>
   <td style="text-align: center;"><code>aqua</code>（水绿）</td>
   <td><code>#00ffff</code></td>
   <td style="background: aqua;"></td>
  </tr>
  <tr>
   <td><a class="external" href="https://www.w3.org/TR/CSS2/" hreflang="en" lang="en" rel="noopener" title="CSS Level&nbsp;2 (Revision&nbsp;1)">CSS Level&nbsp;2 (Revision&nbsp;1)</a></td>
   <td style="background: #FFA500;"></td>
   <td style="text-align: center;"><code>orange</code>（橙）</td>
   <td><code>#ffa500</code></td>
   <td style="background: orange;"></td>
  </tr>
  <tr>
   <td rowspan="128"><a class="external" href="https://drafts.csswg.org/css-color-3/" hreflang="en" lang="en" rel="noopener" title="CSS Color Module Level&nbsp;3">CSS Color Module Level&nbsp;3</a></td>
   <td style="background: #f0f8ff;"></td>
   <td style="text-align: center;"><code>aliceblue</code>（浅灰蓝）</td>
   <td><code>#f0f8ff</code></td>
   <td style="background: aliceblue;"></td>
  </tr>
  <tr>
   <td style="background: #faebd7;"></td>
   <td style="text-align: center;"><code>antiquewhite</code>（古董白）</td>
   <td><code>#faebd7</code></td>
   <td style="background: antiquewhite;"></td>
  </tr>
  <tr>
   <td style="background: #7fffd4;"></td>
   <td style="text-align: center;"><code>aquamarine</code>（海蓝）</td>
   <td><code>#7fffd4</code></td>
   <td style="background: aquamarine;"></td>
  </tr>
  <tr>
   <td style="background: #f0ffff;"></td>
   <td style="text-align: center;"><code>azure</code>（蔚蓝）</td>
   <td><code>#f0ffff</code></td>
   <td style="background: azure;"></td>
  </tr>
  <tr>
   <td style="background: #f5f5dc;"></td>
   <td style="text-align: center;"><code>beige</code>（浅褐）</td>
   <td><code>#f5f5dc</code></td>
   <td style="background: beige;"></td>
  </tr>
  <tr>
   <td style="background: #ffe4c4;"></td>
   <td style="text-align: center;"><code>bisque</code>（橘黄）</td>
   <td><code>#ffe4c4</code></td>
   <td style="background: bisque;"></td>
  </tr>
  <tr>
   <td style="background: #ffebcd;"></td>
   <td style="text-align: center;"><code>blanchedalmond</code>（杏仁白）</td>
   <td><code>#ffebcd</code></td>
   <td style="background: blanchedalmond;"></td>
  </tr>
  <tr>
   <td style="background: #8a2be2;"></td>
   <td style="text-align: center;"><code>blueviolet</code>（蓝紫）</td>
   <td><code>#8a2be2</code></td>
   <td style="background: blueviolet;"></td>
  </tr>
  <tr>
   <td style="background: #a52a2a;"></td>
   <td style="text-align: center;"><code>brown</code>（褐）</td>
   <td><code>#a52a2a</code></td>
   <td style="background: brown;"></td>
  </tr>
  <tr>
   <td style="background: #deb887;"></td>
   <td style="text-align: center;"><code>burlywood</code>（原木色）</td>
   <td><code>#deb887</code></td>
   <td style="background: burlywood;"></td>
  </tr>
  <tr>
   <td style="background: #5f9ea0;"></td>
   <td style="text-align: center;"><code>cadetblue</code>（灰蓝）</td>
   <td><code>#5f9ea0</code></td>
   <td style="background: cadetblue;"></td>
  </tr>
  <tr>
   <td style="background: #7fff00;"></td>
   <td style="text-align: center;"><code>chartreuse</code>（黄绿）</td>
   <td><code>#7fff00</code></td>
   <td style="background: chartreuse;"></td>
  </tr>
  <tr>
   <td style="background: #d2691e;"></td>
   <td style="text-align: center;"><code>chocolate</code>（巧克力色）</td>
   <td><code>#d2691e</code></td>
   <td style="background: chocolate;"></td>
  </tr>
  <tr>
   <td style="background: #ff7f50;"></td>
   <td style="text-align: center;"><code>coral</code>（珊瑚红）</td>
   <td><code>#ff7f50</code></td>
   <td style="background: coral;"></td>
  </tr>
  <tr>
   <td style="background: #6495ed;"></td>
   <td style="text-align: center;"><code>cornflowerblue</code>（矢车菊蓝）</td>
   <td><code>#6495ed</code></td>
   <td style="background: cornflowerblue;"></td>
  </tr>
  <tr>
   <td style="background: #fff8dc;"></td>
   <td style="text-align: center;"><code>cornsilk</code>（玉米穗黄）</td>
   <td><code>#fff8dc</code></td>
   <td style="background: cornsilk;"></td>
  </tr>
  <tr>
   <td style="background: #dc143c;"></td>
   <td style="text-align: center;"><code>crimson</code>（深红）</td>
   <td><code>#dc143c</code></td>
   <td style="background: crimson;"></td>
  </tr>
  <tr>
   <td style="background: #00008b;"></td>
   <td style="text-align: center;"><code>darkblue</code>（深蓝）</td>
   <td><code>#00008b</code></td>
   <td style="background: darkblue;"></td>
  </tr>
  <tr>
   <td style="background: #008b8b;"></td>
   <td style="text-align: center;"><code>darkcyan</code>（深青）</td>
   <td><code>#008b8b</code></td>
   <td style="background: darkcyan;"></td>
  </tr>
  <tr>
   <td style="background: #b8860b;"></td>
   <td style="text-align: center;"><code>darkgoldenrod</code>（暗金）</td>
   <td><code>#b8860b</code></td>
   <td style="background: darkgoldenrod;"></td>
  </tr>
  <tr>
   <td style="background: #a9a9a9;"></td>
   <td style="text-align: center;"><code>darkgray</code><sup><a href="#1" title="color_value#1">[*]</a></sup>（深灰）</td>
   <td><code>#a9a9a9</code></td>
   <td style="background: darkgray;"></td>
  </tr>
  <tr>
   <td style="background: #006400;"></td>
   <td style="text-align: center;"><code>darkgreen</code>（深绿）</td>
   <td><code>#006400</code></td>
   <td style="background: darkgreen;"></td>
  </tr>
  <tr>
   <td style="background: #a9a9a9;"></td>
   <td style="text-align: center;"><code>darkgrey</code><sup><a href="#1" title="color_value#1">[*]</a></sup>（深灰）</td>
   <td><code>#a9a9a9</code></td>
   <td style="background: darkgrey;"></td>
  </tr>
  <tr>
   <td style="background: #bdb76b;"></td>
   <td style="text-align: center;"><code>darkkhaki</code>（暗黄褐）</td>
   <td><code>#bdb76b</code></td>
   <td style="background: darkkhaki;"></td>
  </tr>
  <tr>
   <td style="background: #8b008b;"></td>
   <td style="text-align: center;"><code>darkmagenta</code>（深紫）</td>
   <td><code>#8b008b</code></td>
   <td style="background: darkmagenta;"></td>
  </tr>
  <tr>
   <td style="background: #556b2f;"></td>
   <td style="text-align: center;"><code>darkolivegreen</code>（深橄榄绿）</td>
   <td><code>#556b2f</code></td>
   <td style="background: darkolivegreen;"></td>
  </tr>
  <tr>
   <td style="background: #ff8c00;"></td>
   <td style="text-align: center;"><code>darkorange</code>（深橙）</td>
   <td><code>#ff8c00</code></td>
   <td style="background: darkorange;"></td>
  </tr>
  <tr>
   <td style="background: #9932cc;"></td>
   <td style="text-align: center;"><code>darkorchid</code>（深兰花紫）</td>
   <td><code>#9932cc</code></td>
   <td style="background: darkorchid;"></td>
  </tr>
  <tr>
   <td style="background: #8b0000;"></td>
   <td style="text-align: center;"><code>darkred</code>（深红）</td>
   <td><code>#8b0000</code></td>
   <td style="background: darkred;"></td>
  </tr>
  <tr>
   <td style="background: #e9967a;"></td>
   <td style="text-align: center;"><code>darksalmon</code>（深橙红）</td>
   <td><code>#e9967a</code></td>
   <td style="background: darksalmon;"></td>
  </tr>
  <tr>
   <td style="background: #8fbc8f;"></td>
   <td style="text-align: center;"><code>darkseagreen</code>（深海绿）</td>
   <td><code>#8fbc8f</code></td>
   <td style="background: darkseagreen;"></td>
  </tr>
  <tr>
   <td style="background: #483d8b;"></td>
   <td style="text-align: center;"><code>darkslateblue</code>（暗灰蓝）</td>
   <td><code>#483d8b</code></td>
   <td style="background: darkslateblue;"></td>
  </tr>
  <tr>
   <td style="background: #2f4f4f;"></td>
   <td style="text-align: center;"><code>darkslategray</code><sup><a href="#1" title="color_value#1">[*]</a></sup>（墨绿）</td>
   <td><code>#2f4f4f</code></td>
   <td style="background: darkslategray;"></td>
  </tr>
  <tr>
   <td style="background: #2f4f4f;"></td>
   <td style="text-align: center;"><code>darkslategrey</code><sup><a href="#1" title="color_value#1">[*]</a></sup>（墨绿）</td>
   <td><code>#2f4f4f</code></td>
   <td style="background: darkslategrey;"></td>
  </tr>
  <tr>
   <td style="background: #00ced1;"></td>
   <td style="text-align: center;"><code>darkturquoise</code>（暗宝石绿）</td>
   <td><code>#00ced1</code></td>
   <td style="background: darkturquoise;"></td>
  </tr>
  <tr>
   <td style="background: #9400d3;"></td>
   <td style="text-align: center;"><code>darkviolet</code>（深紫罗兰）</td>
   <td><code>#9400d3</code></td>
   <td style="background: darkviolet;"></td>
  </tr>
  <tr>
   <td style="background: #ff1493;"></td>
   <td style="text-align: center;"><code>deeppink</code>（深粉红）</td>
   <td><code>#ff1493</code></td>
   <td style="background: deeppink;"></td>
  </tr>
  <tr>
   <td style="background: #00bfff;"></td>
   <td style="text-align: center;"><code>deepskyblue</code>（深天蓝）</td>
   <td><code>#00bfff</code></td>
   <td style="background: deepskyblue;"></td>
  </tr>
  <tr>
   <td style="background: #696969;"></td>
   <td style="text-align: center;"><code>dimgray</code><sup><a href="#1" title="color_value#1">[*]</a>（暗灰）</sup></td>
   <td><code>#696969</code></td>
   <td style="background: dimgray;"></td>
  </tr>
  <tr>
   <td style="background: #696969;"></td>
   <td style="text-align: center;"><code>dimgrey</code><sup><a href="#1" title="color_value#1">[*]</a>（暗灰）</sup></td>
   <td><code>#696969</code></td>
   <td style="background: dimgrey;"></td>
  </tr>
  <tr>
   <td style="background: #1e90ff;"></td>
   <td style="text-align: center;"><code>dodgerblue</code>（遮板蓝）</td>
   <td><code>#1e90ff</code></td>
   <td style="background: dodgerblue;"></td>
  </tr>
  <tr>
   <td style="background: #b22222;"></td>
   <td style="text-align: center;"><code>firebrick</code>（砖红）</td>
   <td><code>#b22222</code></td>
   <td style="background: firebrick;"></td>
  </tr>
  <tr>
   <td style="background: #fffaf0;"></td>
   <td style="text-align: center;"><code>floralwhite</code>（花白）</td>
   <td><code>#fffaf0</code></td>
   <td style="background: floralwhite;"></td>
  </tr>
  <tr>
   <td style="background: #228b22;"></td>
   <td style="text-align: center;"><code>forestgreen</code>（丛林绿）</td>
   <td><code>#228b22</code></td>
   <td style="background: forestgreen;"></td>
  </tr>
  <tr>
   <td style="background: #dcdcdc;"></td>
   <td style="text-align: center;"><code>gainsboro</code>（浅灰）</td>
   <td><code>#dcdcdc</code></td>
   <td style="background: gainsboro;"></td>
  </tr>
  <tr>
   <td style="background: #f8f8ff;"></td>
   <td style="text-align: center;"><code>ghostwhite</code>（幽灵白）</td>
   <td><code>#f8f8ff</code></td>
   <td style="background: ghostwhite;"></td>
  </tr>
  <tr>
   <td style="background: #ffd700;"></td>
   <td style="text-align: center;"><code>gold</code>（金）</td>
   <td><code>#ffd700</code></td>
   <td style="background: gold;"></td>
  </tr>
  <tr>
   <td style="background: #daa520;"></td>
   <td style="text-align: center;"><code>goldenrod</code>（橘黄）</td>
   <td><code>#daa520</code></td>
   <td style="background: goldenrod;"></td>
  </tr>
  <tr>
   <td style="background: #adff2f;"></td>
   <td style="text-align: center;"><code>greenyellow</code>（黄绿）</td>
   <td><code>#adff2f</code></td>
   <td style="background: greenyellow ;"></td>
  </tr>
  <tr>
   <td style="background: #808080;"></td>
   <td style="text-align: center;"><code>grey</code>（灰）</td>
   <td><code>#808080</code></td>
   <td style="background: grey;"></td>
  </tr>
  <tr>
   <td style="background: #f0fff0;"></td>
   <td style="text-align: center;"><code>honeydew</code>（蜜瓜色）</td>
   <td><code>#f0fff0</code></td>
   <td style="background: honeydew;"></td>
  </tr>
  <tr>
   <td style="background: #ff69b4;"></td>
   <td style="text-align: center;"><code>hotpink</code>（亮粉）</td>
   <td><code>#ff69b4</code></td>
   <td style="background: hotpink;"></td>
  </tr>
  <tr>
   <td style="background: #cd5c5c;"></td>
   <td style="text-align: center;"><code>indianred</code>（印第安红）</td>
   <td><code>#cd5c5c</code></td>
   <td style="background: indianred;"></td>
  </tr>
  <tr>
   <td style="background: #4b0082;"></td>
   <td style="text-align: center;"><code>indigo</code>（靛蓝）</td>
   <td><code>#4b0082</code></td>
   <td style="background: indigo;"></td>
  </tr>
  <tr>
   <td style="background: #fffff0;"></td>
   <td style="text-align: center;"><code>ivory</code>（象牙白）</td>
   <td><code>#fffff0</code></td>
   <td style="background: ivory;"></td>
  </tr>
  <tr>
   <td style="background: #f0e68c;"></td>
   <td style="text-align: center;"><code>khaki</code>（卡其色）</td>
   <td><code>#f0e68c</code></td>
   <td style="background: khaki;"></td>
  </tr>
  <tr>
   <td style="background: #e6e6fa;"></td>
   <td style="text-align: center;"><code>lavender</code>（淡紫）</td>
   <td><code>#e6e6fa</code></td>
   <td style="background: lavender;"></td>
  </tr>
  <tr>
   <td style="background: #fff0f5;"></td>
   <td style="text-align: center;"><code>lavenderblush</code>（淡紫红）</td>
   <td><code>#fff0f5</code></td>
   <td style="background: lavenderblush ;"></td>
  </tr>
  <tr>
   <td style="background: #7cfc00;"></td>
   <td style="text-align: center;"><code>lawngreen</code>（草绿）</td>
   <td><code>#7cfc00</code></td>
   <td style="background: lawngreen;"></td>
  </tr>
  <tr>
   <td style="background: #fffacd;"></td>
   <td style="text-align: center;"><code>lemonchiffon</code>（粉黄）</td>
   <td><code>#fffacd</code></td>
   <td style="background: lemonchiffon;"></td>
  </tr>
  <tr>
   <td style="background: #add8e6;"></td>
   <td style="text-align: center;"><code>lightblue</code>（淡蓝）</td>
   <td><code>#add8e6</code></td>
   <td style="background: lightblue;"></td>
  </tr>
  <tr>
   <td style="background: #f08080;"></td>
   <td style="text-align: center;"><code>lightcoral</code>（浅珊瑚色）</td>
   <td><code>#f08080</code></td>
   <td style="background: lightcoral;"></td>
  </tr>
  <tr>
   <td style="background: #e0ffff;"></td>
   <td style="text-align: center;"><code>lightcyan</code>（淡青）</td>
   <td><code>#e0ffff</code></td>
   <td style="background: lightcyan;"></td>
  </tr>
  <tr>
   <td style="background: #fafad2;"></td>
   <td style="text-align: center;"><code>lightgoldenrodyellow</code>（浅金黄）</td>
   <td><code>#fafad2</code></td>
   <td style="background: lightgoldenrodyellow ;"></td>
  </tr>
  <tr>
   <td style="background: #d3d3d3;"></td>
   <td style="text-align: center;"><code>lightgray</code><sup><a href="#1" title="color_value#1">[*]</a></sup>（浅灰）</td>
   <td><code>#d3d3d3</code></td>
   <td style="background: lightgray;"></td>
  </tr>
  <tr>
   <td style="background: #90ee90;"></td>
   <td style="text-align: center;"><code>lightgreen</code>（浅绿）</td>
   <td><code>#90ee90</code></td>
   <td style="background: lightgreen;"></td>
  </tr>
  <tr>
   <td style="background: #d3d3d3;"></td>
   <td style="text-align: center;"><code>lightgrey</code><sup><a href="#1" title="color_value#1">[*]</a></sup>（浅灰）</td>
   <td><code>#d3d3d3</code></td>
   <td style="background: lightgrey;"></td>
  </tr>
  <tr>
   <td style="background: #ffb6c1;"></td>
   <td style="text-align: center;"><code>lightpink</code>（淡粉）</td>
   <td><code>#ffb6c1</code></td>
   <td style="background: lightpink;"></td>
  </tr>
  <tr>
   <td style="background: #ffa07a;"></td>
   <td style="text-align: center;"><code>lightsalmon</code>（浅肉色）</td>
   <td><code>#ffa07a</code></td>
   <td style="background: lightsalmon;"></td>
  </tr>
  <tr>
   <td style="background: #20b2aa;"></td>
   <td style="text-align: center;"><code>lightseagreen</code>（浅海绿）</td>
   <td><code>#20b2aa</code></td>
   <td style="background: lightseagreen;"></td>
  </tr>
  <tr>
   <td style="background: #87cefa;"></td>
   <td style="text-align: center;"><code>lightskyblue</code>（浅天蓝）</td>
   <td><code>#87cefa</code></td>
   <td style="background: lightskyblue;"></td>
  </tr>
  <tr>
   <td style="background: #778899;"></td>
   <td style="text-align: center;"><code>lightslategray</code><sup><a href="#1" title="color_value#1">[*]</a></sup>（浅青灰）</td>
   <td><code>#778899</code></td>
   <td style="background: lightslategray;"></td>
  </tr>
  <tr>
   <td style="background: #778899;"></td>
   <td style="text-align: center;"><code>lightslategrey</code><sup><a href="#1" title="color_value#1">[*]</a></sup>（浅青灰）</td>
   <td><code>#778899</code></td>
   <td style="background: lightslategrey;"></td>
  </tr>
  <tr>
   <td style="background: #b0c4de;"></td>
   <td style="text-align: center;"><code>lightsteelblue</code>（浅钢蓝）</td>
   <td><code>#b0c4de</code></td>
   <td style="background: lightsteelblue;"></td>
  </tr>
  <tr>
   <td style="background: #ffffe0;"></td>
   <td style="text-align: center;"><code>lightyellow</code>（浅黄）</td>
   <td><code>#ffffe0</code></td>
   <td style="background: lightyellow;"></td>
  </tr>
  <tr>
   <td style="background: #32cd32;"></td>
   <td style="text-align: center;"><code>limegreen</code>（酸橙绿）</td>
   <td><code>#32cd32</code></td>
   <td style="background: limegreen;"></td>
  </tr>
  <tr>
   <td style="background: #faf0e6;"></td>
   <td style="text-align: center;"><code>linen</code>（亚麻色）</td>
   <td><code>#faf0e6</code></td>
   <td style="background: linen;"></td>
  </tr>
  <tr>
   <td style="background: #66cdaa;"></td>
   <td style="text-align: center;"><code>mediumaquamarine</code>（中绿）</td>
   <td><code>#66cdaa</code></td>
   <td style="background: mediumaquamarine;"></td>
  </tr>
  <tr>
   <td style="background: #0000cd;"></td>
   <td style="text-align: center;"><code>mediumblue</code>（中蓝）</td>
   <td><code>#0000cd</code></td>
   <td style="background: mediumblue;"></td>
  </tr>
  <tr>
   <td style="background: #ba55d3;"></td>
   <td style="text-align: center;"><code>mediumorchid</code>（间兰花紫）</td>
   <td><code>#ba55d3</code></td>
   <td style="background: mediumorchid;"></td>
  </tr>
  <tr>
   <td style="background: #9370db;"></td>
   <td style="text-align: center;"><code>mediumpurple</code>（中紫）</td>
   <td><code>#9370db</code></td>
   <td style="background: mediumpurple;"></td>
  </tr>
  <tr>
   <td style="background: #3cb371;"></td>
   <td style="text-align: center;"><code>mediumseagreen</code>（间海绿）</td>
   <td><code>#3cb371</code></td>
   <td style="background: mediumseagreen;"></td>
  </tr>
  <tr>
   <td style="background: #7b68ee;"></td>
   <td style="text-align: center;"><code>mediumslateblue</code>（中暗蓝）</td>
   <td><code>#7b68ee</code></td>
   <td style="background: mediumslateblue;"></td>
  </tr>
  <tr>
   <td style="background: #00fa9a;"></td>
   <td style="text-align: center;"><code>mediumspringgreen</code>（中春绿）</td>
   <td><code>#00fa9a</code></td>
   <td style="background: mediumspringgreen;"></td>
  </tr>
  <tr>
   <td style="background: #48d1cc;"></td>
   <td style="text-align: center;"><code>mediumturquoise</code>（中海湖蓝）</td>
   <td><code>#48d1cc</code></td>
   <td style="background: mediumturquoise;"></td>
  </tr>
  <tr>
   <td style="background: #c71585;"></td>
   <td style="text-align: center;"><code>mediumvioletred</code>（中紫罗兰）</td>
   <td><code>#c71585</code></td>
   <td style="background: mediumvioletred;"></td>
  </tr>
  <tr>
   <td style="background: #191970;"></td>
   <td style="text-align: center;"><code>midnightblue</code>（午夜蓝）</td>
   <td><code>#191970</code></td>
   <td style="background: midnightblue;"></td>
  </tr>
  <tr>
   <td style="background: #f5fffa;"></td>
   <td style="text-align: center;"><code>mintcream</code>（薄荷乳白）</td>
   <td><code>#f5fffa</code></td>
   <td style="background: mintcream;"></td>
  </tr>
  <tr>
   <td style="background: #ffe4e1;"></td>
   <td style="text-align: center;"><code>mistyrose</code>（粉玫瑰红）</td>
   <td><code>#ffe4e1</code></td>
   <td style="background: mistyrose;"></td>
  </tr>
  <tr>
   <td style="background: #ffe4b5;"></td>
   <td style="text-align: center;"><code>moccasin</code>（鹿皮色）</td>
   <td><code>#ffe4b5</code></td>
   <td style="background: moccasin;"></td>
  </tr>
  <tr>
   <td style="background: #ffdead;"></td>
   <td style="text-align: center;"><code>navajowhite</code>（纳瓦白）</td>
   <td><code>#ffdead</code></td>
   <td style="background: navajowhite;"></td>
  </tr>
  <tr>
   <td style="background: #fdf5e6;"></td>
   <td style="text-align: center;"><code>oldlace</code>（浅米色）</td>
   <td><code>#fdf5e6</code></td>
   <td style="background: oldlace;"></td>
  </tr>
  <tr>
   <td style="background: #6b8e23;"></td>
   <td style="text-align: center;"><code>olivedrab</code>（橄榄褐）</td>
   <td><code>#6b8e23</code></td>
   <td style="background: olivedrab;"></td>
  </tr>
  <tr>
   <td style="background: #ff4500;"></td>
   <td style="text-align: center;"><code>orangered</code>（橙红）</td>
   <td><code>#ff4500</code></td>
   <td style="background: orangered;"></td>
  </tr>
  <tr>
   <td style="background: #da70d6;"></td>
   <td style="text-align: center;"><code>orchid</code>（兰花紫）</td>
   <td><code>#da70d6</code></td>
   <td style="background: orchid;"></td>
  </tr>
  <tr>
   <td style="background: #eee8aa;"></td>
   <td style="text-align: center;"><code>palegoldenrod</code>（灰菊黄）</td>
   <td><code>#eee8aa</code></td>
   <td style="background: palegoldenrod;"></td>
  </tr>
  <tr>
   <td style="background: #98fb98;"></td>
   <td style="text-align: center;"><code>palegreen</code>（苍绿）</td>
   <td><code>#98fb98</code></td>
   <td style="background: palegreen;"></td>
  </tr>
  <tr>
   <td style="background: #afeeee;"></td>
   <td style="text-align: center;"><code>paleturquoise</code>（苍宝石绿）</td>
   <td><code>#afeeee</code></td>
   <td style="background: paleturquoise;"></td>
  </tr>
  <tr>
   <td style="background: #db7093;"></td>
   <td style="text-align: center;"><code>palevioletred</code>（苍紫罗兰）</td>
   <td><code>#db7093</code></td>
   <td style="background: palevioletred;"></td>
  </tr>
  <tr>
   <td style="background: #ffefd5;"></td>
   <td style="text-align: center;"><code>papayawhip</code>（木瓜色）</td>
   <td><code>#ffefd5</code></td>
   <td style="background: papayawhip;"></td>
  </tr>
  <tr>
   <td style="background: #ffdab9;"></td>
   <td style="text-align: center;"><code>peachpuff</code>（桃色）</td>
   <td><code>#ffdab9</code></td>
   <td style="background: peachpuff;"></td>
  </tr>
  <tr>
   <td style="background: #cd853f;"></td>
   <td style="text-align: center;"><code>peru</code>（秘鲁色）</td>
   <td><code>#cd853f</code></td>
   <td style="background: peru;"></td>
  </tr>
  <tr>
   <td style="background: #ffc0cb;"></td>
   <td style="text-align: center;"><code>pink</code>（粉）</td>
   <td><code>#ffc0cb</code></td>
   <td style="background: pink;"></td>
  </tr>
  <tr>
   <td style="background: #dda0dd;"></td>
   <td style="text-align: center;"><code>plum</code>（李子色）</td>
   <td><code>#dda0dd</code></td>
   <td style="background: plum;"></td>
  </tr>
  <tr>
   <td style="background: #b0e0e6;"></td>
   <td style="text-align: center;"><code>powderblue</code>（粉蓝）</td>
   <td><code>#b0e0e6</code></td>
   <td style="background: powderblue;"></td>
  </tr>
  <tr>
   <td style="background: #bc8f8f;"></td>
   <td style="text-align: center;"><code>rosybrown</code>（玫瑰粽）</td>
   <td><code>#bc8f8f</code></td>
   <td style="background: rosybrown;"></td>
  </tr>
  <tr>
   <td style="background: #4169e1;"></td>
   <td style="text-align: center;"><code>royalblue</code>（宝蓝）</td>
   <td><code>#4169e1</code></td>
   <td style="background: royalblue;"></td>
  </tr>
  <tr>
   <td style="background: #8b4513;"></td>
   <td style="text-align: center;"><code>saddlebrown</code>（马鞍棕）</td>
   <td><code>#8b4513</code></td>
   <td style="background: saddlebrown;"></td>
  </tr>
  <tr>
   <td style="background: #fa8072;"></td>
   <td style="text-align: center;"><code>salmon</code>（鲑肉色）</td>
   <td><code>#fa8072</code></td>
   <td style="background: salmon;"></td>
  </tr>
  <tr>
   <td style="background: #f4a460;"></td>
   <td style="text-align: center;"><code>sandybrown</code>（沙褐色）</td>
   <td><code>#f4a460</code></td>
   <td style="background: sandybrown;"></td>
  </tr>
  <tr>
   <td style="background: #2e8b57;"></td>
   <td style="text-align: center;"><code>seagreen</code>（海绿）</td>
   <td><code>#2e8b57</code></td>
   <td style="background: seagreen;"></td>
  </tr>
  <tr>
   <td style="background: #fff5ee;"></td>
   <td style="text-align: center;"><code>seashell</code>（贝壳白）</td>
   <td><code>#fff5ee</code></td>
   <td style="background: seashell;"></td>
  </tr>
  <tr>
   <td style="background: #a0522d;"></td>
   <td style="text-align: center;"><code>sienna</code>（赭）</td>
   <td><code>#a0522d</code></td>
   <td style="background: sienna;"></td>
  </tr>
  <tr>
   <td style="background: #87ceeb;"></td>
   <td style="text-align: center;"><code>skyblue</code>（天蓝）</td>
   <td><code>#87ceeb</code></td>
   <td style="background: skyblue;"></td>
  </tr>
  <tr>
   <td style="background: #6a5acd;"></td>
   <td style="text-align: center;"><code>slateblue</code>（青蓝）</td>
   <td><code>#6a5acd</code></td>
   <td style="background: slateblue;"></td>
  </tr>
  <tr>
   <td style="background: #708090;"></td>
   <td style="text-align: center;"><code>slategray</code><sup><a href="#1" title="color_value#1">[*]</a></sup>（青灰）</td>
   <td><code>#708090</code></td>
   <td style="background: slategray;"></td>
  </tr>
  <tr>
   <td style="background: #708090;"></td>
   <td style="text-align: center;"><code>slategrey</code><sup><a href="#1" title="color_value#1">[*]</a></sup>（青灰）</td>
   <td><code>#708090</code></td>
   <td style="background: slategrey;"></td>
  </tr>
  <tr>
   <td style="background: #fffafa;"></td>
   <td style="text-align: center;"><code>snow</code>（雪白）</td>
   <td><code>#fffafa</code></td>
   <td style="background: snow;"></td>
  </tr>
  <tr>
   <td style="background: #00ff7f;"></td>
   <td style="text-align: center;"><code>springgreen</code>（春绿）</td>
   <td><code>#00ff7f</code></td>
   <td style="background: springgreen;"></td>
  </tr>
  <tr>
   <td style="background: #4682b4;"></td>
   <td style="text-align: center;"><code>steelblue</code>（铁青）</td>
   <td><code>#4682b4</code></td>
   <td style="background: steelblue;"></td>
  </tr>
  <tr>
   <td style="background: #d2b48c;"></td>
   <td style="text-align: center;"><code>tan</code>（棕褐）</td>
   <td><code>#d2b48c</code></td>
   <td style="background: tan;"></td>
  </tr>
  <tr>
   <td style="background: #d8bfd8;"></td>
   <td style="text-align: center;"><code>thistle</code>（苍紫）</td>
   <td><code>#d8bfd8</code></td>
   <td style="background: thistle;"></td>
  </tr>
  <tr>
   <td style="background: #ff6347;"></td>
   <td style="text-align: center;"><code>tomato</code>（番茄红）</td>
   <td><code>#ff6347</code></td>
   <td style="background: tomato;"></td>
  </tr>
  <tr>
   <td style="background: #40e0d0;"></td>
   <td style="text-align: center;"><code>turquoise</code>（蓝绿）</td>
   <td><code>#40e0d0</code></td>
   <td style="background: turquoise;"></td>
  </tr>
  <tr>
   <td style="background: #ee82ee;"></td>
   <td style="text-align: center;"><code>violet</code>（紫罗兰色）</td>
   <td><code>#ee82ee</code></td>
   <td style="background: violet;"></td>
  </tr>
  <tr>
   <td style="background: #f5deb3;"></td>
   <td style="text-align: center;"><code>wheat</code>（麦色）</td>
   <td><code>#f5deb3</code></td>
   <td style="background: wheat;"></td>
  </tr>
  <tr>
   <td style="background: #f5f5f5;"></td>
   <td style="text-align: center;"><code>whitesmoke</code>（烟白）</td>
   <td><code>#f5f5f5</code></td>
   <td style="background: whitesmoke;"></td>
  </tr>
  <tr>
   <td style="background: #9acd32;"></td>
   <td style="text-align: center;"><code>yellowgreen</code>（黄绿）</td>
   <td><code>#9acd32</code></td>
   <td style="background: yellowgreen;"></td>
  </tr>
  <tr>
   <td><a class="external" href="https://drafts.csswg.org/css-color/" hreflang="en" lang="en" rel="noopener" title="CSS Color Module Level&nbsp;4">CSS Color Module Level&nbsp;4</a></td>
   <td style="background: #639;"></td>
   <td style="text-align: center;"><code>rebeccapurple</code>（利百加紫）</td>
   <td><code>#663399</code></td>
   <td style="background: rebeccapurple;"></td>
  </tr>
 </tbody>
</table>


## 2. `transparent` 关键字
`transparent` 关键字表示一个完全透明的颜色，即该颜色看上去将是背景色。从技术上说，它是带有阿尔法通道为最小值的黑色，是 `rgba(0,0,0,0)` 的简写。

## 3. `currentColor` 关键字
`currentColor` 关键字代表原始的 `color` 属性的计算值。它允许让继承自属性或子元素的属性颜色属性以默认值不再继承。

它也能用于那些继承了元素的 `color` 属性计算值的属性，相当于在这些元素上使用 `inherit` 关键字，如果这些元素有该关键字的话。

## 4. `rgb()`
颜色可以使用红-绿-蓝（red-green-blue (RGB)）模式的两种方式被定义：
+ **十六进制符号 `#RRGGBB` 和 `#RGB`**
    - "#" 后跟6位十六进制字符（0-9, A-F）。
    - "#" 后跟3位十六进制字符（0-9, A-F）。

三位数的 RGB 符号（`#RGB`）和六位数的形式（`#RRGGBB`）是相等的。
例如， `#f03` 和 `#ff0033` 代表同样的颜色。

+ **函数符 `rgb(R,G,B)`**  
"rgb" 后跟3个 `<integer>` 或3个 `<percentage>` 值。  
例如 `100%` 相当于 整数 `255`，也相当于十六进制符号里的 `F` 或 `FF` 。

<pre style="background-color: lightgrey; color: black; font-weight: bold;">
/* These examples all specify the same RGB color: */

 #f03
 #F03
 #ff0033
 #FF0033
 rgb(255,0,51)
 rgb(255, 0, 51)
 <s>rgb(255, 0, 51.2)</s> /* ERROR! Don't use fractions, use integers */ 
 rgb(100%,0%,20%)
 rgb(100%, 0%, 20%)
 <s>rgb(100%, 0, 20%)</s> /* ERROR! Don't mix up integer and percentage notation */
</pre>

## 5. `hsl()`
颜色也可以使用 `hsl()` 函数符被定义为 **色相-饱和度-明度**（Hue-saturation-lightness）模式。HSL 相比 RGB 的优点是更加直观：你可以估算你想要的颜色，然后微调。它也更易于创建相称的颜色集合。（通过保持相同的色相并改变明度/暗度和饱和度）。

**色相(Hue)** 表示色环（即代表彩虹的一个圆环）的一个角度。这个角度作为一个无单位的 `<number>` 被给出。定义 `red=0=360`，其它颜色分散于圆环，所以 `green=120`， `blue=240`，以此类推。作为一个角度，它隐含像 `-120=240` 和 `480=120` 这样的回环。

**饱和度** 和 **明度** 由百分数来表示。  
`100%` 是满饱和度，`0%` 是一种灰度。  
`100%` 明度是白色，`0%` 明度是黑色，而 `50%` 明度是“一般的”。

<pre style="background-color: lightgrey; color: black; font-weight: bold;">
hsl(0,  100%,50%)   <span style="background-color: hsl(0,100%,50%);"> /* red */   </span>
hsl(30, 100%,50%)   <span style="background: hsl(30,100%,50%);">&nbsp;            </span> 
hsl(60, 100%,50%)   <span style="background: hsl(60,100%,50%);">&nbsp;            </span>
hsl(90, 100%,50%)   <span style="background: hsl(90,100%,50%);">&nbsp;            </span>
hsl(120,100%,50%)   <span style="background: hsl(120,100%,50%);"> /* green */ </span>
hsl(150,100%,50%)   <span style="background: hsl(150,100%,50%);">&nbsp;            </span>
hsl(180,100%,50%)   <span style="background: hsl(180,100%,50%);">&nbsp;            </span>
hsl(210,100%,50%)   <span style="background: hsl(210,100%,50%);">&nbsp;            </span>
hsl(240,100%,50%)   <span style="background: hsl(240,100%,50%);"> /* blue */  </span>
hsl(270,100%,50%)   <span style="background: hsl(270,100%,50%);">&nbsp;            </span>
hsl(300,100%,50%)   <span style="background: hsl(300,100%,50%);">&nbsp;            </span>
hsl(330,100%,50%)   <span style="background: hsl(330,100%,50%);">&nbsp;            </span>
hsl(360,100%,50%)   <span style="background: hsl(360,100%,50%);"> /* red */   </span>

hsl(120,100%,25%)   <span style="background: hsl(120,100%,25%);"> /* dark green */  </span>
hsl(120,100%,50%)   <span style="background: hsl(120,100%,50%);"> /* green */       </span>
hsl(120,100%,75%)   <span style="background: hsl(120,100%,75%);"> /* light green */ </span>

hsl(120,100%,50%)   <span style="background: hsl(120,100%,50%);"> /* green */  </span>
hsl(120, 67%,50%)   <span style="background: hsl(120,67%,50%);">&nbsp;             </span>
hsl(120, 33%,50%)   <span style="background: hsl(120,33%,50%);">&nbsp;             </span>
hsl(120,  0%,50%)   <span style="background: hsl(120,0%,50%);">&nbsp;             </span>

hsl(120, 60%,70%)   <span style="background: hsl(120,60%,70%);"> /* pastel green */ </span>
</pre>

## 6. `rgba()`
颜色可以使用 `rgba()` 函数符在红-绿-蓝-阿尔法（RGBa）模式下被定义。RGBa 扩展了 RGB 颜色模式，它包含了阿尔法通道，允许设定一个颜色的透明度。  
**a** 表示透明度：0=透明；1=不透明；

<pre style="background-color: lightgrey; color: black; font-weight: bold;">
rgba(255,0,0,0.1)   <span style="background: rgba(255,0,0,0.1);"> /* 10% opaque red */  </span>
rgba(255,0,0,0.4)   <span style="background: rgba(255,0,0,0.4);"> /* 40% opaque red */  </span>
rgba(255,0,0,0.7)   <span style="background: rgba(255,0,0,0.7);"> /* 70% opaque red */  </span>
rgba(255,0,0,  1)   <span style="background: rgba(255,0,0,1);"> /* full opaque red */ </span>
</pre>

## 7. `hsla()`
颜色可以使用 `hsla()` 函数符在色相-饱和度-明度-阿尔法（HSLa）模式下被定义。HSLa 扩展自 HSL 颜色模式，包含了阿尔法通道，可以规定一个颜色的透明度。  
**a** 表示透明度：0=透明；1=不透明；

<pre style="background-color: lightgrey; color: black; font-weight: bold;">
hsla(240,100%,50%,0.05)  <span style="background: hsla(240,100%,50%,0.05);"> /* 5% opaque blue */   </span>
hsla(240,100%,50%, 0.4)  <span style="background: hsla(240,100%,50%,0.4);"> /* 40% opaque blue */  </span>
hsla(240,100%,50%, 0.7)  <span style="background: hsla(240,100%,50%,0.7);"> /* 70% opaque blue */  </span>
hsla(240,100%,50%,   1)  <span style="background: hsla(240,100%,50%,1);"> /* full opaque blue */ </span>
</pre>


