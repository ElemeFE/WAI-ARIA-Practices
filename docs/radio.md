## Radio
Radio组是由一系列 checkable radio button组成, 且在一个组中只有一个 radio button是 checked 状态。

### Keyboard Interaction
- 当Radio组接收到focus时：
 - 如果组内有radio处于checked状态，则focus设置在该元素；
 - 如果组件内没有radio处于checked状态，则组内第一个radio获得focus；
 
- Space：切换radio的checked状态；
- Right/Down：将focus移到组内下一个radio元素，如果是最后一个radio，则focus移到组内第一个radio。然后选中新的radio元素；
- Left/Up：将focus移到组内上一个radio元素，如果是第一个radio，则focus移到组内最后一个radio。然后选中新的radio元素；

注意：
上面描述的初始焦点行为与某些浏览器为原生HTMLradio组提供的行为略有不同。在有些浏览器下面，如果组内无radio被选中，使用 Shift+Tab将焦点移到组内时，会把focus聚焦到组内最后一个元素而不是第一个元素；

### WAI-ARIA Roles, States, and Properties
- 包含radio button元素的container元素应设置role="radiogroup"；
- 每个radio button元素设置role="radio"；
- 每个radio button应设置[aria-checked](/aria?id=aria-checked-state)值为true/false；
- 每个radio button默认使用它的文本内容作为label，也可使用[aria-labelledby](/aria?id=aria-labelledby-property) 或者 [aria-label](/aria?id=aria-label-property)提供；
- 可使用[aria-labelledby](/aria?id=aria-labelledby-property) 或者 [aria-label](/aria?id=aria-label-property)为radio group提供label；
- 如果页面上其他元素内容为group或者单个radio button提供了额外的描述文字，可使用[aria-describedby](/aria?id=aria-describedby-property)关联到包含描述文字的元素；

### Example
- [wai-aria-practices](https://www.w3.org/TR/wai-aria-practices/examples/radio/radio-1/radio-1.html)
- [wai-aria-practices](https://www.w3.org/TR/wai-aria-practices/examples/radio/radio-2/radio-2.html)
- [Element](http://element.eleme.io/#/zh-CN/component/radio)
- [material2](https://material.angular.io/components/radio/overview)
- [angular](https://ng-bootstrap.github.io/#/components/buttons/examples)
- [open ajax](http://www.oaa-accessibility.org/examplep/radio1/)
- [open ajax](http://www.oaa-accessibility.org/examplep/radio2/)