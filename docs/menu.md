## Menu
Menu组件为用户提供了一系列选择，比如一组操作或者功能。一般菜单通过一个按钮打开或者显示，点击其中一个菜单选项可以打开子菜单，通常当用户选择一个菜单项时菜单会关闭，除非是打开了一个子菜单；
我们一般常见的菜单是菜单栏，菜单栏通常是水平的且放在应用中窗口的顶端，为用户提供一系列快捷命令。

### Keyboard Interaction
- 当 menu 打开或 menubar 获得焦点时，键盘焦点应当放置在第一个 item 上， 所有的 menuitem 都都应当是 focusable 的
- Enter，当 focus 聚焦在 menuitem上时
    - 如果它有子菜单，则打开子菜单，并把焦点移到子菜单的第一个元素上
    - 否则 激活当前 item, 关闭 menu
- Space
    -（可选）当焦点在 menuitemcheckbox 时，改变 checked 状态，不关闭当前menu
    -（可选）当焦点在 menuitemradio 且 为 unchecked状态时， 改变 checked 状态，同时 unchecks 同组中其他 menuitemradio的状态，不关闭当前menu
    -（可选）当焦点在 一个包含子菜单的 menuitem 上时, 打开子菜单，并把焦点移到子菜单的第一个元素上
    -（可选）当焦点在 一个不包含子菜单的 menuitem 上时, 激活当前 menuitem, 关闭 menu
- Down
    - 当焦点在 menubar 中的一个 menuitem 上时， 打开子菜单，并把焦点移到子菜单的第一个元素上
    - 当焦点在 menu 中时，将焦点移动到下一个同级别的 menuitem 上
- Up
    -（可选）当焦点在 menubar 中的一个 menuitem 上时， 打开子菜单，并把焦点移到子菜单的最后一个元素上
    - 当焦点在 menu 中时，将焦点移动到上一个同级别的 menuitem 上
- Right
    - 当焦点在 menubar 中的 menuitem 上时， 将焦点移动到下一个 item上
    - 当焦点在 menu 中的包含子菜单的 menuitem 上时，打开子菜单，并把焦点移到子菜单的第一个元素上
    - 当焦点在 menu 中的不包含子菜单的 menuitem 上时，执行以下三种行为：
        - 关闭子菜单以及所有父menus
        - 将焦点移动到 menubar 中下一个 menuitem 上
        -（推荐）打开上一步中的 menuitem的子菜单但不移动焦点，或者 打开子菜单，并把焦点移到子菜单的第一个元素上
- Left
    - 当焦点在 menubar 中的 menuitem 上时， 将焦点移动到前一个 item上
    - 当焦点在 子菜单中的 menuitem 上时，关闭子菜单，并把焦点移回该子菜单的父 menuitem 上
    - 当焦点在 menubar 中某个 menuitem 的子菜单中时，执行以下三种行为：
        - 关闭子菜单
        - 将焦点移动到 menubar 中上一个 menuitem 上
        -（推荐）打开上一步中的 menuitem的子菜单但不移动焦点，或者 打开子菜单，并把焦点移到子菜单的第一个元素上

Escape: 关闭包含焦点的菜单，并把焦点移动到打开当前菜单的 元素上。比如 menu button 或者 父 menuitem
Tab: 将焦点移动到 tab 队列中的下一个元素上，如果当前 focus的元素不在 menubar 中，关闭 menubar 中 所有打开的 menu
Shift + Tab： 将焦点移动到 tab 队列中的上一个元素上，如果当前 focus 的元素不在 menubar 中，关闭 menubar 中 所有打开的 menu

### WAI-ARIA Roles, States, and Properties

- 包含所有菜单项的父元素 role 值为 menu 或 menubar.
- 单个菜单项 role 值为 menuitem、menuitemcheckbox 或 menuitemradio
- 如果点击一个菜单项会打开子菜单，则该菜单项被认为是一个父菜单项，子菜单 role=menu 的元素应该在 Dom 结构上包含或者逻辑上 owned by ([aria-owns](/aria?id=aria-owns-property))这个父菜单项
- 父菜单项设置属性[aria-haspopup](/aria?id=aria-haspopup-property) 值为 menu 或 true
- 父菜单项设置属性[aria-expanded](/aria?id=aria-expanded-state),当子菜单打开或可视时，设置为true, 关闭时设置为false
- 当 menuitemcheckbox or menuitemradio 状态为 checked 时, [aria-checked](/aria?id=aria-checked-state) 设置为 true.
- 当子菜单项状态为 disabled, [aria-disabled](/aria?id=aria-disabeld-state) 设置为 true.
- 若 一个menu被分成多个组，应当使用 role=separator 的元素来分割组，比如 包含一系列的 menuitemradio 的 menu，且 separators 的[aria-orientation](/aria?id=aria-orientation-property) 属性值应当与方向一致
- 若 menubar 有一个可视化的label,则 role=menubar 的元素应该使用 [aria-labelledby](/aria?id=aria-labelledby-property)指向 label 元素。否则 menubar 元素 使用 aria-label 设置 label.
- 若 menubar 的方向是垂直的，[aria-orientation](/aria?id=aria-orientation-property) 值设为 vertical, menubar 的 aria-orientation 默认值为 horizontal

- role=menu 的元素 应该有以下之一：
    - aria-labelledby 的值 指向 一个 menuitem 或者 控制该元素展示的 button 元素
    - aria-label 设置 label 值
- 若 menu 的方向是水平的，[aria-orientation](/aria?id=aria-orientation-property) 值设为 horizontal, menu 的 aria-orientation 默认值为 vertical

### other Examples
- [material](https://material.angular.io/components/menu/overview)
- [wai-aria-practices](https://www.w3.org/TR/wai-aria-practices/examples/menubar/menubar-1/menubar-1.html)
- [wai-aria-practices](https://www.w3.org/TR/wai-aria-practices/examples/menubar/menubar-2/menubar-2.html)