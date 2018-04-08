## Dialog
Dialog 一般是需要用户对展示信息进行输入操作或者反应的窗体，Dialog 的设计是打断当前页面的工作流的一个弹层。Dialog 的作者应当保证对话框里面至少有一个 focusable 的后代元素。
当对话框展示的时候，作者应当聚焦到其中一个后代元素，对框内元素进行焦点管理以保证焦点始终在框内。
当框关闭的时候，焦点元素回归页面上某个可聚焦元素,一般是打开框的元素

### Keyboard Interaction

| Key | Description |  
| ------| ------ |  
| Tab / Shift+Tab  | 用于框内焦点切换 |  
| Escape | 关闭弹窗 |  

### WAI-ARIA Roles, States, and Properties
- 元素赋值role="dialog" 或 role="alertdialog" 
- 元素设置属性[aria-modal](/aria?id=aria-modal-property) = true
- 为组件提供一个可访问的语义化label，可使用[aria-labelledby](/aria?id=aria-labelledby-property) 或者 [aria-label](/aria?id=aria-label-property)提供

### dialog vs alertdialog
alertdialog 是 dialog 的 特殊版，一般用来向用户传递一个 alert 信息

### Examples
- [wai-aria-practices](https://www.w3.org/TR/wai-aria-practices-1.1/#dialog_modal)
- [Element](http://element.eleme.io/#/zh-CN/component/dialog)
- [material](https://material.angular.io/components/dialog/overview)