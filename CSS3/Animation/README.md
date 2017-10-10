# Animation 动画

> 关键帧(from)中出现的属性才会在动画中使用; 如果没有的话，这些属性将在整个动画中使用其初始定义的值.

> 只有同时在0% 和100% 关键帧中出现的属性才会在动画中使用; 如果没有的话，这些属性将在整个动画中使用其初始定义的值(第一个定义的帧).

> 关键帧中出现的 !important 关键词将会被忽略

- duration 动画整个过程持续多少秒
- timing-function 动画轨迹（贝塞尔曲线）
- delay 延迟多少秒开始播放动画
- iteration-count 动画播放次数，infinite无限次
- direction 动画方向，alternate偶数和奇数次方向不同（制作连贯动画）
- play-state 动画开始暂停，paused暂停

> 时间值第一个解析为duration持续时间，第二个解析为delay延时时间