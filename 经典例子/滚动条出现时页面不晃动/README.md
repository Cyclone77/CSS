## 页面出现滚动条页面不晃动

当设置任何元素的属性(无滚动条时)为：overflow:auto或者(有滚动条时)设置为：overflow:hidden时，当前元素的内容会出现晃动（收缩）。
作为一个强迫症患者，怎么处理呢？

[MDN](https://developer.mozilla.org/zh-CN/docs/Web/CSS/length)这里有介绍。

这里引入vm这个单位。
> 代表视窗(Viewport)的宽度为1%，并没有实际的宽度，100wm就是100%的视口宽度。

就拿body来说：
``` css
body {
    width: 100vm;
    overflow-x: hidden;
}
```
以上代码就可以使得body出现滚动条或者隐藏滚动条的时候，页面不会出现晃动。
这里说下为什么要设置：overflow-x: hidden; 呢，因为你的视口宽度是页面的实际宽度+滚动条的宽度，已经超过了100%了，所以会出现横向的滚动条。

当然可以这样设置：
``` CSS
body {
    padding-left: calc(100vw - 100%);
}
```
视口的宽度-页面的实际宽度就是滚动条的宽度
