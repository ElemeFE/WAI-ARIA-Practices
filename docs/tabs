## Tabs
Tabs是由一系列层叠的内容区域被称为tab panels 组成的，同一时间只展示一块 tab panels。每个 tab panels 有一个关联的 tab 元素， 当 tab 被激活时，展示相关联的 tab panels
tab list 一般是沿着 tab panels 的某个边缘分布的，一般是在顶部

### Keyboard Interaction

Tab:
- 当焦点移进 tab list 中时，将焦点设置在当前激活的 tab 元素
- 当焦点在tab list 中时，将焦点移动到页面Tab序列中下一个焦点元素，一般是在 tab list 之外的元素

当焦点在水平方向的 tab list 中时：
- Left: 将焦点设置到 tab list 中前一个 tab 元素上，(可选)激活当前  focused tab
- Right: 将焦点设置到 tab list 中后一个 tab 元素上，(可选)激活当前  focused tab

当焦点在 tab list 中时：
- Space or Enter: 激活当前 tab，如果不是自动激活的话
- (可选) Home：将焦点移动至第一个 tab
- (可选) End：将焦点移动至最后一个 tab
- (可选) Delete：如果允许删除，则删除当前 tab 元素 以及 相关联的 tab panel. 如果存在其他 tab , 将焦点设置到临近的 tab 元素上，并激活当前元素
### WAI-ARIA Roles, States, and Properties

- 包含 tab list 的元素，赋值 role=tablist
- tab 元素赋值 role=tab,被包含在 role=tablist 的元素中
- tab 元素关联的tab panel 赋值 role=tabpanel
- 每个 tab 设置 [aria-controls](/aria?id=aria-controls-property) 指向关联的 tabpanel
- 当前 激活的 tab 元素 设置  aria-selected 为true， 其余 tab 元素设置为 false
- 每个 tabpanel 元素应该设置  aria-labelledby ，属性值指向关联的 tab 元素
- 如果一个 tab 元素 包含一个 弹出的菜单，应设置  aria-haspopup 值为 menu or true
- 如果 role=tablist 的元素是垂直的，则设置 aria-orientation 值为 vertical, 默认值为 horizontal

### Examples
- [Element](http://element-cn.eleme.io/#/zh-CN/component/tabs)
- [material](https://material.angular.io/components/tabs/overview)
- [open ajax](http://oaa-accessibility.org/example/34/)
- [wai-aria-practices](https://www.w3.org/TR/wai-aria-practices/examples/tabs/tabs-1/tabs.html)
- [wai-aria-practices](https://www.w3.org/TR/wai-aria-practices/examples/tabs/tabs-2/tabs.html)