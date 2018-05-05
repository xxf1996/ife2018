# No.1 - 制作一个简单的菜单动画效果



## 任务目的

- 熟悉 CSS3 过渡子属性
- 通过 JavaScript 触发过渡效果
- 理解语义化，合理地使用 HTML 标签来构建页面

## 任务描述

- 通过 CSS transition 实现如下效果：
  [视频demo](https://eopa.bdstatic.com/ife%2F%E4%BB%BB%E5%8A%A1%E4%B8%80.mov)
- 每次点击【切换样式】按钮的时候，出现视频 demo 所示的动画效果。
- 学有余力的同学可以研究一下，如何通过修改贝塞尔曲线，让这个动效更贴近自然。     

## 任务注意事项

- CSS transition 的各项子属性（时间曲线）等详细值可以自由定义；
- 注意浏览器中的兼容性；
- HTML 及 CSS 代码结构清晰、规范；
- 代码中含有必要的注释；

## 在线学习参考资料

- [CSS3 新特性兼容方法总结](https://www.cnblogs.com/jesse131/p/5441199.html)
- [CSS3 过渡](http://www.w3school.com.cn/css3/css3_transition.asp)
- [Understanding CSS3 Transitions](http://alistapart.com/article/understanding-css3-transitions)
- [动效落地方法](https://zhuanlan.zhihu.com/uxelement)
- [优秀的 CSS 交互动效示例](https://lab.hakim.se/ladda/)





## 实践方案

- 使用`css3`的`transition`特性即可
- 实现效果：

![effect](p1.gif)

### note

- 直接用`border-bottom`使用渐变效果并非想象的效果，而是`border`的高度进行变化，而非宽度！
- 利用原生`js`实现类似于`jQuery`的`toggleClass()`方法，可以使用`DOMTokenList`接口的`toggle()`方法；如：

```js
line.classList.toggle('line-change'); // 切换样式
```

​	而`Element.classList`返回该元素的样式列表，可以直接使用上述方法；（尚不清楚该方法的兼容性）

- 如果使用样式（`class`）切换来实现这个效果，需要注意样式的优先级；如元素本身使用`id`样式，而切换一个`class`样式，同样的属性还是会以`id`样式优先的！所以还可以利用增删内联`inline`样式·（即`style`属性）来进行样式切换，内联样式的优先级高于`id`选择器；



### 参考文档

1. [DOMTokenList - Web API 接口 | MDN](https://developer.mozilla.org/zh-CN/docs/Web/API/DOMTokenList)