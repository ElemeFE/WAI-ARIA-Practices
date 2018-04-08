## aria
###### aria-labelledby (property)   
标识一个元素内容是当前元素的 label,aria-labelledby 作用和 aria-label 是一样的，都是为 object 提供 accessible name，当页面上没有可视的label内容时，使用aria-label，当两个属性同时存在，在计算object的accessible name 的算法中，aria-labelledby 的优先级高于 aria-label；aria-labelledby 的值一般是页面上可视元素的ID，注意：label内容是比较简洁的；

###### aria-label (property)  
定义一串字符串作为当前元素的 label,作用同 aria-labelledby，当 label text 存在于当前页面上，应使用 aria-labelledby。

###### aria-describedby (property)  
标识一个元素内容是当前元素的 description,用法和 aria-labelledby 类似。

###### aria-pressed (state) 
标识一个 toggle buttons 的当前 "pressed" 的状态，按钮被激活时值为 true，在此激活时值变为 false；作用和 aria-checked 类似，只不过  aria-checked用在checkbox上面，aria-pressed用在role="button"的元素上；     

| Value | Description |  
| ------| ------ |  
| false | 元素支持被 pressed，但处于未被 pressed 状态 |  
| true | 元素支持被 pressed，且被 pressed 状态 |  
| mixed | 元素所控制的多个 item 的 pressed 状态不同，混合状态 |  
| undefined（default） | 元素不支持 pressed，也就是说不是一个 toggle button |  

###### aria-haspopup (property) 
指示交互式弹出元素的可用性和类型，比如 menu、dialog 可以被当前元素激活；一个弹出元素一般是出现在其他页面内容之上的内容块且元素的 container 的 role 一般是 menu,listbox,tree,grid或dialog；
aria-haspopup的值一般也就是上面几种 role 值类型；
当一个弹出元素有键盘交互时，应当保证激活弹出元素的按钮元素 focusable，当激活按钮，弹出元素展示在页面上时，需要注意焦点的转移处理以及弹出元素内焦点的管理；   
注意： tooltip 不被认为是一个弹出元素；

| Value | Description |  
| ------| ------ |  
| false（default）  | 当前元素没有弹出元素 |  
| true | 弹出元素类型为 menu,为了兼容1.0版本 |  
| menu | 弹出元素类型为 menu |  
| listbox | 弹出元素类型为 listbox |  
| tree | 弹出元素类型为 tree |  
| grid | 弹出元素类型为 grid |  
| dialog | 弹出元素类型为 dialog  |  

###### aria-disabeld (state) 
表示一个元素是可视的但是不可操作和编辑。当一个元素的 aria-disabeld 值为 true 时，当前元素及其后代元素都应是 disabled 状态且值不可被用户改变；

###### aria-current (state)
表示当前元素是 container 中或者一系列相关元素列表中的 current元素，aria-current 属性值是枚举类型，任何不在枚举列表中的值都会被认为是 true；

| Value | Description |  
| ------| ------ |  
| false（default）  | 该元素不是 current 元素 |  
| page | 元素是 current page，用在一系列页面链接列表中 |  
| step | 元素是 current step，用在一系列步骤列表中 |  
| location | 元素是 current location，用在一系列环境或上下文列表中 |  
| date | 元素是 current date，用在一系列日期列表中 |  
| time | 元素是 current time，用在一系列时间列表中 |  
| true | 元素是 current 元素，用在一系列元素中  |  

###### aria-checked (state)
标识当前checkbox、radio、或其它组件的 checked 状态；用在role值为 checkbox,option、radio、switch、menuitemcheckbox、treeitem、menuitem中；

| Value | Description |  
| ------| ------ |  
| false  | 元素可被选中，目前处于未选中状态|  
| true |  元素处于被选中状态  |  
| mixed | 元素处于部分选中状态 |  
| undefined(default) | 元素不支持 选中 |  

###### aria-valuenow & aria-valuetext (property)
该属性使用在有取值范围的组件上如slider、progress等；如果组件当前值不知道时，可以不设置该属性值，当组件aria-valuenow取值范围有最大最小值时，需设置aria-valuemax and aria-valuemin属性；
aria-valuenow取值为数字，对于progressbar和scrollbar组件，AT设备会把 aria-valuenow 渲染为百分比取值，对于slider和spinbutton组件，AT设备会渲染其当前数值；
当组件的当前值使用数字不能准确传达语义时，可使用aria-valuetext为当前值提供友好的可替代文字.当 aria-valuetext 和 aria-valuenow 同时存在时, AT设备会读取 aria-valuetext 值来替代 aria-valuenow。


###### aria-valuemin & aria-valuemax (property)
为有取值范围的组件提供最大最小值，最小值aria-valuemin应当小于等于最大值aria-valuemax；

###### aria-orientation (property)
定义一个元素的方向是水平，垂直还是不确定的；属性默认值是undefined,但在某些role值上是有隐含值的，比如slider默认为horizontal，scrollbar默认为vertical;

| Value | Description |  
| ------| ------ |  
| horizontal  | 元素朝向是水平的|  
| vertical | 元素朝向是垂直的  |  
| undefined(default) | 元素朝向是未定义或不明确的 |

###### aria-modal (property)
用来标识一个元素是不是蒙层元素。当蒙层元素展示时，用户交互被限定在蒙层元素的后代元素中，直至蒙层元素被关闭。当蒙层元素展示时，AT设备应当导航到该元素，除非作者明确设置了焦点元素。

###### aria-busy (state)

标识一个元素的内容将会被更改，当一个元素的 aria-busy 为 true 时，AT会忽略该元素及其子元素的内容更新，直至 aria-busy = false时，才会一次性
把更新作为一个整体反馈给使用者。
