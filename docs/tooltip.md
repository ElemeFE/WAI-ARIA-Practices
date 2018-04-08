## Tooltip
Tooltip 是用于展示元素A的描述信息的弹层，一般当元素A状态为 :hover 或者 :focus 时显示。
弹层显示时，焦点依然保留在触发弹层显示的元素A上。当焦点离开该元素A时，弹层隐藏

### Keyboard Interaction

| Key | Description |  
| ------| ------ |  
| Escape | 关闭弹层 |  

### WAI-ARIA Roles, States, and Properties

- 元素赋值role="tooltip" 
- 元素A的[aria-describedby](/aria?id=aria-describedby-property)的值指向 tooltip 元素

### Examples
- [Element](http://element.eleme.io/#/zh-CN/component/tooltip)
- [material](https://material.angular.io/components/tooltip/overview)