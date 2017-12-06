## Button
Button组件允许用户触发一个事件或者行为，比如提交表单、打开弹窗、取消行为或者删除操作。   
除了传统的Button组件类型，WAI-ARIA 还支持另外两种类型的Button。   
- 切换按钮：状态切换按钮有两种状态，pressed or not pressed，为了告诉AT设备按钮是一个状态切换按钮，   
需声明aria-pressed属性，比如语音播放器上的一个静音功能切换按钮，当按钮按下时，aria-pressed=true   
表示静音状态；一般当按钮状态发生改变时，label文字是不变的，比如当按钮按下时，读屏软件会类似于说    
"静音按钮被按下"这类话，如果设计的是label文字从"静音"改为"非静音"这种模式， aria-pressed属性就不需要了；
   
- menu按钮：能够打开menu面板的按钮，需声明[aria-haspopup](/aria)为true，告知 AT 设备点击按钮会有menu弹出；

### Keyboard Interaction
当button获得焦点时：
- Space：激活按钮
- Enter：激活按钮
- 随着按钮被激活，focus焦点元素的设置依赖于按钮的类型：
  - 如果激活按钮会弹出Dialog，焦点会移动到Dialog内
  - 如果激活按钮会关闭Dialog，焦点一般会回到打开这个Dialog的按钮，当弹窗是一个确认对话框，用以删除该按钮所在的上下文，焦点需要移动到新的上下文；
  - 如果激活按钮没有使当前上下文退出，则焦点保留在该按钮上
  - 如果激活按钮引起上下文发生改变，比如移到程序的下一步或新增一个search,应该将focus移动到后续行为的起始点；
  - 如果一个按钮被通过快捷键激活，焦点始终保存在快捷键发生的上下文中，比如在一个list中通过 Alt + U 来 激活UP按钮的行为，焦点始终保存在list中；

### WAI-ARIA Roles, States, and Properties
- Button组件应该有 role='button'
- Button组件应该有一个可访问的语义化label，默认情况下由button元素内的文本元素计算生成，也可以通过[aria-labelledby](/aria) 或者 [aria-label](/aria)提供
- 如果Button的功能描述出现在页面上，也可以通过[aria-describedby](/aria)='id'关联到包含描述文字的元素
- 如果Button的行为当前不可用，设置[aria-disabeld](/aria)= true
- 如果Button是一个状态切换按钮，需设置[aria-pressed](/aria)属性


### Example
<iframe width="100%" height="300" src="//jsfiddle.net/maranran/7nc39epo/7/embedded/result,html,css/?bodyColor=fff"  allowfullscreen="allowfullscreen" frameborder="0"></iframe>

### other Examples
- [wai-aria-practices](https://www.w3.org/TR/wai-aria-practices/examples/button/button.html)
- [material2](https://material.angular.io/components/button/overview)
- [material2](https://material.angular.io/components/button-toggle/overview)
- [ng-bootstrap](https://ng-bootstrap.github.io/#/components/buttons/examples)
- [Element](http://element.eleme.io/#/zh-CN/component/button)
- [oaa-accessibility](http://oaa-accessibility.org/example/4/)
