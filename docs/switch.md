## Switch
Switch 是一种拥有开/关两种状态的 checkbox，分别代表着 checked/unchecked 两种状态
### Keyboard Interaction
应当保证元素的 focusable 属性为true

### WAI-ARIA Roles, States, and Properties
- role = switch
-  [aria-checked](/aria?id=aria-checked-state) 属性值暗示着当前状态是开(true)还是关(false)，值 mixed 此时是无效的，等同于 false
-  为组件提供一个可访问的语义化label，可使用[aria-labelledby](/aria?id=aria-labelledby-property) 或者 [aria-label](/aria?id=aria-label-property)提供
### other Examples
- [Element](http://element.eleme.io/#/zh-CN/component/switch)
- [material](https://material.angular.io/components/slide-toggle/overview)