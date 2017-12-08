## aria
###### aria-labelledby (property)   
标识一个元素内容是当前元素的label,aria-labelledby作用和aria-label是一样的，都是为object提供 accessible name，当页面上没有可视的label内容时，使用aria-label，当两个属性同时存在，在计算object的accessible name 的算法中，aria-labelledby 的优先级高于 aria-label；aria-labelledby 的值一般是页面上可视元素的ID，注意：label内容是比较简洁的；

###### aria-label (property)  
定义一串字符串作为当前元素的label,作用同aria-labelledby，当label text存在于当前页面上，应使用aria-labelledby。

###### aria-describedby (property)  
标识一个元素内容是当前元素的description,用法和aria-labelledby类似。

###### aria-pressed (state) 
标识一个toggle buttons的当前"pressed"的状态，按钮被激活时值为true，在此激活时值变为false；作用和 aria-checked类似，只不过  aria-checked用在checkbox上面，aria-pressed用在role="button"的元素上；     

| Value | Description |  
| ------| ------ |  
| false | 元素支持被pressed，但处于未被pressed状态 |  
| true | 元素支持被pressed，且被pressed状态 |  
| mixed | 元素所控制的多个item的pressed状态不同，混合状态 |  
| undefined（default） | 元素不支持 pressed，也就是说不是一个toggle button |  

###### aria-haspopup (property) 
指示交互式弹出元素的可用性和类型，比如menu、dialog可以被当前元素激活；一个弹出元素一般是出现在其他页面内容之上的内容块且元素的container的role一般是menu,listbox,tree,grid或dialog；
aria-haspopup的值一般也就是上面几种role值类型；
当一个弹出元素有键盘交互时，应当保证激活弹出元素的按钮元素focusable，当激活按钮，弹出元素展示在页面上时，需要注意焦点的转移处理以及弹出元素内焦点的管理；   
注意： tooltip不被认为是一个弹出元素；

| Value | Description |  
| ------| ------ |  
| false（default）  | 当前元素没有弹出元素 |  
| true | 弹出元素类型为menu,为了兼容1.0版本 |  
| menu | 弹出元素类型为menu |  
| listbox | 弹出元素类型为listbox |  
| tree | 弹出元素类型为tree |  
| grid | 弹出元素类型为grid |  
| dialog | 弹出元素类型为dialog  |  

###### aria-disabeld (state) 
表示一个元素是可视的但是不可操作和编辑。当一个元素的aria-disabeld值为true时，当前元素及其后代元素都应是disabled状态且值不可被用户改变；

###### aria-current (state)
表示当前元素是container中或者一系列相关元素列表中的current元素，aria-current属性值是枚举类型，任何不在枚举列表中的值都会被认为是true；

| Value | Description |  
| ------| ------ |  
| false（default）  | 该元素不是current元素 |  
| page | 元素是current page，用在一系列页面链接列表中 |  
| step | 元素是current step，用在一系列步骤列表中 |  
| location | 元素是current location，用在一系列环境或上下文列表中 |  
| date | 元素是current date，用在一系列日期列表中 |  
| time | 元素是current time，用在一系列时间列表中 |  
| true | 元素是current元素，用在一系列元素中  |  

###### aria-checked (state)
标识当前checkbox、radio、或其它组件的 checked 状态；用在role值为 checkbox,option、radio、switch、menuitemcheckbox、treeitem、menuitem中；

| Value | Description |  
| ------| ------ |  
| false  | 元素可被选中，目前处于未选中状态|  
| true |  元素处于被选中状态  |  
| mixed | 元素处于部分选中状态 |  
| undefined(default) | 元素不支持 选中 |  