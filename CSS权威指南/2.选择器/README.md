# 选择器

## 元素选择器

```css
html {
    color: black;
}
h1 {
    color: gray;
}
```

## 类选择器和ID选择器

### 类选择器

> 类选择器不许有class属性才能正常工作，css样式相同的属性，后面的样式会覆盖前面的样式, 和class的前后顺序没有影响

```css
.warning {
    font-weight: bold;
}
```

### ID选择器

```css
#first-para {
    font-weight: bold;
}
```

## 属性选择器

``` css
p[fontColor] {
    color: green;
}
```

## 部分属性选择器
| 类型 | 描述 |
| :- | :- |
| [foo~="bar"] | 选择 foo 属性值为一个空格分割的 bar 的所有元素 |
| [foo^="bar"] | 选择 foo 属性以 bar 开头的所有元素 |
| [foo$="bar"] | 选择 foo 属性以 bar 结尾的所有元素 |
| [foo*="bar"] | 选择 foo 属性值包含字串 bar 的所有元素 |
| [foo&#124;="bar"] | 选择 foo 属性值等于或者开头是 bar 的所有元素 |
