## Spinbutton
Spinbutton组件是一个限制取值范围或者取值为一系列分离值的input输入框；一般Spinbutton组件由三部分组成，包括展示当前值的input框、增大和减少按钮用来调节当前值；
一般input框是组件内唯一可focus的元素，通过监听keydown事件判断快捷键来调节当前值的大小，且焦点始终在input框内；input框一般也允许用户直接输入和编辑当前值；如果Spinbutton的取值范围非常大，应当支持以大/小两种步长的方式来调节值，比如按下 Up/Down 键支持当前值以1的步长进行变化，按下 Page Up/Page Down 键支持当前值以10的步长进行变化；

### Keyboard Interaction

- Up Arrow: 增大当前值，一步长/次.
- Down Arrow: 减少当前值，一步长/次.
- Home: 把当前值设为最小值.
- End: 把当前值设为最大值.
- Page Up (可选): 增大当前值，较大步长/次.
- Page Down (可选): 减少当前值，较大步长/次.

### WAI-ARIA Roles, States, and Properties
- 获得焦点的input框赋值role="spinbutton"；
- input框设置[aria-valuenow](/aria?id=aria-valuenow-amp-aria-valuetext-property)属性值为当前spinbutton的值；
- 如果spinbutton有最小值，为input框设置[aria-valuemin](/aria?id=aria-valuemin-amp-aria-valuemax-property)属性；
- 如果spinbutton有最大值，为input框设置[aria-valuemax](/aria?id=aria-valuemin-amp-aria-valuemax-property)属性；
- 在[aria-valuenow](/aria?id=aria-valuenow-amp-aria-valuetext-property)的属性值不容易理解的情况下，如一周有七日，若用1-7数值用户会很难理解，使用[aria-valuetext](/aria?id=aria-valuenow-amp-aria-valuetext-property)="星期一"补充说明会使得当前值更易理解；
- 使用[aria-labelledby](/aria?id=aria-labelledby-property) 或者 [aria-label](/aria?id=aria-label-property)提供label;
注意：
### Example

- [Element](http://element.eleme.io/#/zh-CN/component/input-number)
- [Open Ajax](http://oaa-accessibility.org/example/33/)