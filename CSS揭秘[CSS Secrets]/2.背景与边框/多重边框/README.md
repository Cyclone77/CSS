## 多重边框

### [box-shadow](https://developer.mozilla.org/zh-CN/docs/Web/CSS/box-shadow) 边框的投影

#### 取值

- none：无阴影
- length①：第1个长度值用来设置对象的阴影水平偏移值。可以为负值
- length②：第2个长度值用来设置对象的阴影垂直偏移值。可以为负值
- length③：如果提供了第3个长度值则用来设置对象的阴影模糊值。不允许负值
- length④：如果提供了第4个长度值则用来设置对象的阴影外延值。可以为负值
- color：设置对象的阴影的颜色。
- inset：设置对象的阴影类型为内阴影。该值为空时，则对象的阴影类型为外阴影

> 可以设定多组效果，每组参数值以逗号分隔。对应的脚本特性为box-shadow的特性。

> 投影的行为跟边框不完全一致， 因为它不会影响布局， 而且也不会受到 box-sizing 属性的影响。

> box-shadow 属性加上 inset 关键字， 来使投影绘制在元素的**内圈**。需要增加额外的内边距来腾出足够的空隙。
而不加inset关键字的称为**外圈**，它们并不会响应鼠标事件， 比如悬停或点击。 

[试一试](http://play.csssecrets.io/multiple-borders)

### [outline](https://developer.mozilla.org/zh-CN/docs/Web/CSS/outline) 轮廓

CSS的outline属性是用来设置一个或多个单独的轮廓属性的简写属性 ， 例如 outline-style, outline-width 和 outline-color。 多数情况下，简写属性更加可取和便捷。

轮廓与边框在以下几个方面存在不同：

- 轮廓不占据空间，它们被描绘于内容之上
- 轮廓可以是非矩形的。在Gecko/Firefox中，轮廓是矩形的，但是Opera则会围绕元素结构绘制非矩形的形状，如下图

#### 语法

/* 宽度 | 样式 | 颜色 */ 

outline: 1px solid white;

#### outline-offset

- outline-offset是以border边界作为参考点的，从0开始，正值从border边界往外延，负值从border边界往里缩；    
- outline的边框画在border的外面；
- outlines相关属性不占据布局空间，不会影响元素的尺寸；

> outline边框不会根据border-radius的圆角产生圆角。这被w3c工作组视为BUG后期可能会处理。