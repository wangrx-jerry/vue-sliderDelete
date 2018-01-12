# 组件说明
## 这是一个基于vue2.x 移动端侧滑删除dmeo
>预览：

![image](/src/assets/Preview.png)
> 主要方法说明

### touch事件
- touchstart: 手指放到屏幕上时触发
- touchmove: 手指在屏幕上滑动式触发
- touchend:手指离开屏幕时触发
### 每个触摸事件被触发后，会生成一个event对象，event对象里额外包括以下三个触摸列表
- touches: 当前屏幕上所有手指的列表
- targetTouches: 当前dom元素上手指的列表，尽量使用这个代替touches
- changedTouches: 涉及当前事件的手指的列表，尽量使用这个代替touches
### 这些列表里的每次触摸由touch对象组成，touch对象里包含着触摸信息，主要属性如下：
- clientX / clientY: 触摸点相对浏览器窗口的位置
- pageX / pageY: 触摸点相对于页面的位置
- screenX  /  screenY: 触摸点相对于屏幕的位置
> 该组件用于移动端侧滑删除行数据
- 当滑块没有超过删除按钮的一半时自动回到起点位置
- 点击删除后删除行
- 利用vue slot（插槽），插入内容  

> 启动：

```
npm（cnpm）i
npm(cnpm) run dev
```

> 组件参数说明
- deleteLine:删除函数
- index:当前行的index
> 使用方法：
- 使用具名插槽和匿名插槽插入页面结构，有关插槽知识可参考：https://cn.vuejs.org/v2/api/#slot
> 最后，，，这是一个菜鸟(我)弄的，仅供参考～