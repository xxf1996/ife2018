### 任务目的

- 深度理解掌握 transition-timing-function 以及它的意义
- 学会配合使用 CSS transform 和CSS transition 制作流畅动画
- 使用 CSS 伪元素触发过渡效果
- 合理的使用 CSS 布局

### 任务描述

- 在我们提供给你的 HTML 文件基础上，适当的添加 CSS transition 和 CSS transform 属性 ，实现视频 demo 中的效果；
- 鼠标 hover 上去的时候，出现小猫笑起来的动画；
  [动画 demo](http://jadyoap.bj.bcebos.com/ife%2F%E4%BB%BB%E5%8A%A13.mov)
  [下载.html 文件](http://jadyoap.bj.bcebos.com/ife%2FcssCatAnimation.html)
- transition 和transform 各项子属性的值可以自定 ；
- 对 CSS 布局比较感兴趣的同学，在学有余力的情况下，可以尝试自己用 CSS 画出小猫。

### 任务注意事项

- 注意浏览器中的兼容性
- 请注意代码风格的整齐、优雅
- HTML 及 CSS 代码结构清晰、规范
- 代码中含有必要的注释       

### 在线学习参考资料

- [CSS3 新特性兼容方法总结](https://www.cnblogs.com/jesse131/p/5441199.html)
- [CSS3贝塞尔曲线工具](http://www.css3beziercurve.net/)
- [CSS3 过渡](http://www.w3school.com.cn/css3/css3_transition.asp)
- [CSS3 变形](http://www.w3school.com.cn/cssref/pr_transform.asp)
- [CSS Transforms Module](https://www.w3.org/TR/css-transforms-1/)
- [CSS3 中的变形 transform详解](https://www.cnblogs.com/afighter/p/5726888.html)
- [CodePen 优秀动画示例](https://codepen.io/Alireza29675/pen/KwgwMy)



## 实践方案

- 由于基本布局已经给好了，所以只需要对动画部分进行处理即可。
- 主要还是利用`transition`和`transform`
- 关键是怎么让总体进行变化，之前从没想过像`:hover`这样的伪类选择器后还可以接子选择器，所以可以利用父类元素的状态变化从而使其子元素相应的变化：

```css
            .face:hover .eye-core{
                transform: scaleX(0.8);
            }
            .face:hover .eye-bottom{
                transform: translateY(-15px);
            }
            .face:hover .face-red{
                opacity: 1;
            }
            .face:hover .mouth{
                border-radius: 0 40% 50% 50%;
            }
            .container:hover .ear:nth-of-type(1){
                transform: rotate(-30deg);
            }
            .container:hover .ear:nth-of-type(2){
                transform: rotate(30deg);
            }
```

- 需要注意的是，左右两个耳朵需要向不同的方向进行旋转

![效果](p1.gif)

