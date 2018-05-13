## No.6 - 利用 CSS animation 制作一个炫酷的 Slider



### 任务目的

- 学习 CSS animation keyframes
- 理解动画中 关键帧 的概念
- 掌握  CSS  transform 3D 变形

### 任务描述

- 观看视频中的效果 、通过纯CSS 实现一个立方体翻转的效果
    [视频demo](http://jadyoap.bj.bcebos.com/ife%2F%E4%BB%BB%E5%8A%A1%E4%BA%94.mov)
- 要求 hover 的时候， 立方体绕着「通过其中心的纵轴」旋转

### 任务注意事项

- 注意不同浏览器中的兼容性
- 请注意代码风格的整齐、优雅
- HTML 及 CSS 代码结构清晰、规范
- 代码中含有必要的注释       

### 在线学习参考资料

- [CSS3 新特性兼容方法总结](https://www.cnblogs.com/jesse131/p/5441199.html)
- [CodePen 立方体 demo ](https://codepen.io/jordizle/pen/haIdo)
- [CSS3 3D transform 详解](http://www.zhangxinxu.com/wordpress/2012/09/css3-3d-transform-perspective-animate-transition/)
- [CSS Transforms 3D ](http://www.w3school.com.cn/css3/css3_3dtransform.asp)
- [CSS3 @keyframes 规则](http://www.w3school.com.cn/cssref/pr_keyframes.asp)
- [CSS3 过渡](http://www.w3school.com.cn/css3/css3_transition.asp)
- [CSS3 变形](http://www.w3school.com.cn/cssref/pr_transform.asp)
- [CSS Transforms Module](https://www.w3.org/TR/css-transforms-1/)
- [CSS3中的变形 transform详解](https://www.cnblogs.com/afighter/p/5726888.html)



## 实现方案

- 该任务主要是实现一个图片切换的动画效果，使用`css3`新增的`@keyframes`与`animation`属性即可实现
- 用`@keyframes`声明动画的关键帧，然后在`animation`对相应动画进行使用，并设置动画播放时间和变化曲线，以达到还原设计的要求
- 需要注意到一个细节，即前一图片不会在新的图片被点击后就立马消失，而是以『被覆盖』的形式消失，所以不能直接采用使用一个图片切换`src`属性的模式，需要两幅图片轮流切换。