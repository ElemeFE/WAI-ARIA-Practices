## Breadcrumb
Breadcrumb是由一系列链接组成的列表，链接包括当前页面和其父级页面按照等级排列；它可以帮助用户确定在website的位置，一般是水平排列在页面的主要内容区域上方；
### Keyboard Interaction
链接一般使用原生a标签实现，当不是a标签时，应当保证链接元素的focusable属性为true；

### WAI-ARIA Roles, States, and Properties
- Breadcrumb组件应该包含在 role='navigation'或者<nav> 的导航区块元素内；
- 区域元素通过[aria-labelledby](/aria?id=aria-labelledby-property) 或者 [aria-label](/aria?id=aria-label-property)提供label；
- 表示当前页面的链接元素可设置[aria-current](/aria?id=aria-current-state)="page". 如果表示当前页面的元素不是一个链接，aria-current是可选的.

### Example
<iframe width="100%" height="300" src="//jsfiddle.net/maranran/2d7hfdLv/7/embedded/result,html,css/?bodyColor=fff"  allowfullscreen="allowfullscreen" frameborder="0"></iframe>

### other Examples
- [wai-aria-practices](https://www.w3.org/TR/wai-aria-practices/examples/breadcrumb/index.html)
- [Element](http://element.eleme.io/#/zh-CN/component/breadcrumb)
- [WCAG20](https://www.w3.org/WAI/WCAG20/Techniques/working-examples/G65/ex3.html)
- [uvd](https://www.uvd.co.uk/blog/accessible-breadcrumbs-using-aria/)