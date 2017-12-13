## Slider
Slider组件允许用户从指定范围内选择值，典型的Slider是通过滑柄在轨迹上滑动来改变值；
### Keyboard Interaction
- Right/Up: 增大组件的值，一步长/次.
- Left/Down: 减少组件的值，一步长/次.
- Home: 滑尺值设为范围内最小值.
- End: 滑尺值设为范围内最大值.
- Page Up (可选): 增大当前值，较大步长/次.
- Page Down (可选): 减少当前值，较大步长/次.
注意： 焦点始终保持在滑柄(用户可用过鼠标拖动的可视化手柄)上。在有些情况下，上面指定键的值变化方向会反转；
### WAI-ARIA Roles, States, and Properties
- 为可聚焦的滑柄设置role="slider";
- 设置当前滑尺的值[aria-valuenow](/aria?id=aria-valuenow-amp-aria-valuetext-property)；
- 设置滑尺的取值范围 [aria-valuemin](/aria?id=aria-valuemin-amp-aria-valuemax-property) and [aria-valuemax](/aria?id=aria-valuemin-amp-aria-valuemax-property)；
- 在[aria-valuenow](/aria?id=aria-valuenow-amp-aria-valuetext-property)的属性值不容易理解的情况下，如一周有七日，若用1-7数值用户会很难理解，使用[aria-valuetext](/aria?id=aria-valuenow-amp-aria-valuetext-property)="星期一"补充说明会使得当前值更易理解；
- 使用[aria-labelledby](/aria?id=aria-labelledby-property) 或者 [aria-label](/aria?id=aria-label-property)提供label;
- 设置滑尺的滑动方向[aria-orientation](/aria?id=aria-orientation-property),默认值为horizontal，水平方向滑动；

## Slider(Multi-Thumb)
多滑柄Slider是指具有两个或多个滑柄，每个滑柄可以设置一个值从而形成一组相关值的组件；常见的是两个滑柄，设置一个最大值和最小值，形成一个取值区间；单个滑柄不允许越过另一个，也就是说一个滑柄的取值范围需在前一个滑柄的最大值，后一个滑柄的最小值之间；然而在某些多滑柄滑块中，每个滑柄的值的设置不依赖其他滑柄的取值；
### Keyboard Interaction
- 每个滑柄在页面上的tab list中的顺序应和视觉顺序保持一致
- 每个滑柄的tab顺序保持不变，不管它的值和视觉位置如何变化，主要是指一个滑柄的位置随着值的改变，越过其他滑柄的情况；
### WAI-ARIA Roles, States, and Properties
和单滑柄滑块保持一致；
### Example
- [wai-aria-practices](https://www.w3.org/TR/wai-aria-practices/examples/slider/slider-1.html)
- [wai-aria-practices](https://www.w3.org/TR/wai-aria-practices/examples/slider/slider-2.html)
- [oaa-accessibility](http://oaa-accessibility.org/example/32/)
- [Material2](https://material.angular.io/components/slider/overview)
- [Element](http://element.eleme.io/#/zh-CN/component/slider)