### @规则

> @规则以一个@关键字开头，'@'字符后面紧跟着一个标识符（例如，'@import'，'@page'）
一个@规则包含直到下一个分号(;)前包括分号在内，或者下一个块的所有内容，无论哪个先出现
CSS 2.1用户代理必须忽略所有出现在块内部，或者跟在除@charset和@import规则外的任何无法忽略的语句后面的'@import'规则

例如，假设一个CSS 2.1解析器遇到了这样一个样式表:
``` CSS
@import "subs.css";
h1 { color: blue }
@import "list.css";
```
根据CSS 2.1，第二个'@import'是非法的，CSS 2.1解析器会忽略整条@规则，实际上把样式表变成了：
``` css
@import "subs.css";
h1 { color: blue }
```
下例中，第二个'@import'规则是非法的，因为它出现在一个'@media'块的内部
``` css
@import "subs.css";
@media print {
  @import "print-main.css";
  body { font-size: 10pt }
}
h1 {color: blue }
```
相反的，为了提高效率，只在媒体类型为'print'时引入样式表，可以使用带媒体类型的@import规则语法，例如：
``` css
@import "subs.css";
@import "print-main.css" print;
@media print {
  body { font-size: 10pt }
}
h1 {color: blue }
```
