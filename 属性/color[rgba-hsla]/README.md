## color [rgba / hsla]

[MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/color_value)

### currentColor 关键字

> 承了当前元素的 color 属性。如果当前元素没有 color 属性，则寻找父元素的 color 属性, 以此类推；找不到则默认为黑色。

### rgb()

颜色可以使用红-绿-蓝（red-green-blue (RGB)）模式

### hsl()

色相-饱和度-明度（Hue-saturation-lightness）模式

- 色相（Hue）表示色环（即代表彩虹的一个圆环）的一个角度

- 饱和度和明度由百分数来表示。100% 是满饱和度，而 0% 是一种灰度。

- 100% 明度是白色， 0% 明度是黑色，而 50% 明度是“一般的”。

### rgba()

颜色可以使用 rgba() 函数符在红-绿-蓝-阿尔法（RGBa）模式下被定义。RGBa 扩展了 RGB 颜色模式，它包含了阿尔法通道，允许设定一个颜色的透明度。
> a 表示透明度：0=透明；1=不透明；

### hsla()

颜色可以使用 hsla() 函数符在色相-饱和度-明度-阿尔法（HSLa）模式下被定义。HSLa 扩展自 HSL 颜色模式，包含了阿尔法通道，可以规定一个颜色的透明度。
> a 表示透明度：0=透明；1=不透明；

### 流浪器支持

> rgb()支持IE4.0以上， 其他IE9以上才支持