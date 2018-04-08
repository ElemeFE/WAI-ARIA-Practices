## Progress
Progress 用来展示某个任务进度当前状态

### WAI-ARIA Roles, States, and Properties
- role = progressbar
- 当一个进度条是用来表示用户的请求被接受且应用在朝着完成请求的方向进展。此时应该提供[aria-valuenow](http://localhost:3000/#/aria?id=aria-valuenow-amp-aria-valuetext-property), [aria-valuemin & aria-valuemax](http://localhost:3000/#/aria?id=aria-valuemin-amp-aria-valuemax-property),当进度值无法确定时，可以省略 aria-valuenow 值，AT设备会把 aria-valuenow 值渲染为百分数
- 当一个进度表是用来描述页面某个局域的 loading 进度，此时应使用[aria-describedby](http://localhost:3000/#/aria?id=aria-describedby-property) 来指向状态元素，且设置[aria-busy](/aria?id=aria-busy-state) = true 直至页面区域加载完毕
- 为组件提供一个可访问的语义化label，可使用[aria-labelledby](/aria?id=aria-labelledby-property) 或者 [aria-label](/aria?id=aria-label-property)提供
### other Examples
- [Element](http://element.eleme.io/#/zh-CN/component/progress)
- [material](https://material.angular.io/components/progress-bar/overview)