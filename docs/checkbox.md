## Checkbox
ARIA支持两种类型的checkbox组件:
- 双状态：常见的类型，允许用户在checked and not checked两种状态之前选择；
- 混合状态：这类组件支持第三种状态—部分选中，它的状态由一个group中的双状态组件的checked状态决定；
  - 当group中所有checkbox状态为checked时，该组件为checked状态；
  - 当group中所有checkbox状态为not checked时，该组件是not checked状态；
  - 当group中部分checkbox状态为checked时，该组件是部分选中状态； 
  
用户可以通过与混合状态checkbox组件交互来改变其所控制的group中的双状态checkbox组件的状态；
  - 选中组件，group中所有checkbox为选中状态；
  - 取消选中组件，group中所有checkbox为未选中状态；
  
### Keyboard Interaction
checkbox的focusable属性为true，且当checkbox :focus时，按下Space键可以改变组件的checked状态；

### WAI-ARIA Roles, States, and Properties
- 为组件设置role="checkbox"
- 为组件提供一个可访问的语义化label，可使用[aria-labelledby](/aria?id=aria-labelledby-property) 或者 [aria-label](/aria?id=aria-label-property)提供
- 当组件被选中时, 设置[aria-checked](/aria?id=aria-checked-state)为true.
- 当组件取消选中时, 设置[aria-checked](/aria?id=aria-checked-state)为false.
- 如果组件为部分选中状态，设置[aria-checked](/aria?id=aria-checked-state)为mixed.
- 如果一组checkbox作为一个逻辑组存在，这些checkbox应该包含在一个role="group"元素中且应为该元素提供一个label;
- 如果页面上有可视化的文字和checkbo相关，可通过[aria-describedby](/aria?id=aria-describedby-property)='id'关联到包含描述文字的元素;

### Example
- [双状态](https://www.w3.org/TR/wai-aria-practices/examples/checkbox/checkbox-1/checkbox-1.html)
- [混合状态](https://www.w3.org/TR/wai-aria-practices/examples/checkbox/checkbox-2/checkbox-2.html)
- [material2](https://material.angular.io/components/checkbox/overview)
- [Element](http://element.eleme.io/#/zh-CN/component/checkbox)