### 任务目的

- 掌握  CSS  transform 3D 变形
- 使用 CSS 伪元素触发过渡效果
- 熟悉 CSS transform 各项子属性

### 任务描述

- 根据 动效 demo 中的效果 、通过 CSS 实现一个卡片翻转的效果。
- [动效 demo](http://jadyoap.bj.bcebos.com/ife%2F%E4%BB%BB%E5%8A%A1%E5%9B%9B.mov)
- [下载设计稿图片资源](http://jadyoap.bj.bcebos.com/ife%2F%E4%BB%BB%E5%8A%A1%E5%9B%9B%E8%AE%BE%E8%AE%A1%E7%A8%BF.zip)

### 任务注意事项

- 注意不同浏览器中的兼容性
- 请注意代码风格的整齐、优雅
- HTML 及 CSS 代码结构清晰、规范
- 代码中含有必要的注释       

### 在线学习参考资料

- [CSS3 新特性兼容方法总结](https://www.cnblogs.com/jesse131/p/5441199.html)
- [CSS3 3D transform 详解](http://www.zhangxinxu.com/wordpress/2012/09/css3-3d-transform-perspective-animate-transition/)
- [CSS Transforms 3D ](http://www.w3school.com.cn/css3/css3_3dtransform.asp)
- [CSS3 过渡](http://www.w3school.com.cn/css3/css3_transition.asp)
- [CSS3 变形](http://www.w3school.com.cn/cssref/pr_transform.asp)
- [CSS Transforms Module](https://www.w3.org/TR/css-transforms-1/)
- [CSS3中的变形 transform详解](https://www.cnblogs.com/afighter/p/5726888.html)
- [codepen 优秀动画示例](https://codepen.io/Alireza29675/pen/KwgwMy)



## 实现方案

- 这个主要是实现卡片正反两面的翻转效果，可以使用`backface-visibility`这个属性来实现；
- `backface-visibility`表示元素的背面旋转后是否可见，默认为`visible`（即可见），设置为`hidden`则不可见；
- 因此可以通过设置正面图片的`backface-visibility`为`hidden`，当旋转`90`度后正面图片的背面不可见，而背面图片则变为可见，达到正反两面切换的效果；
- 实现效果如下：

![效果图](p1.gif)

## 参考文档

1. [CSS3 backface-visibility 属性](http://www.w3school.com.cn/cssref/pr_backface-visibility.asp)