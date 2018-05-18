## Tree
树形组件代表的是一个有层级关系的列表。 在列表中的每一个 item 都可能会有子 items，可通过展开和折叠来显示或隐藏子元素。比如一个文件系统的导航会使用
树形组件来展示文件夹和文件，每个代表文件夹的节点展开时会包含一些文件或者子文件夹。

### Keyboard Interaction
- 垂直方向：
    - 单选树获得焦点时：
        - 树中没有节点被选中，则焦点设置在树中第一个节点上
        - 有节点处于被选中状态，则焦点设置在被选中的节点上
    - 多选树获得焦点时：
        - 树中没有节点被选中，则焦点设置在树中第一个节点上
        - 有节点处于被选中状态，则焦点设置在被选中的第一个节点上
    - Right：
        - 焦点处在一个 closed 状态的节点上时，open 该节点，焦点不移动
        - 焦点处在一个 open 状态的节点上时，焦点移动到第一个子节点上
        - 焦点在结束节点上时，不作任何改变

    - Left:
        - 焦点处在一个 open 状态的节点上时，close 该节点，焦点不移动
        - 焦点处在子节点上且是结束节点或关闭状态的节点，焦点动到父节点上
        - 焦点处在某个分支的根节点上且是结束节点或关闭状态的节点，不作任何改变
    - Down:
        焦点移动到下一个可聚焦节点上，不打开或者关闭节点
    - Up：
        焦点移动到上一个可聚焦节点上，不打开或者关闭节点
    - Home：
        焦点移动到树中第一个可聚焦节点上，不打开或者关闭节点
    - End：
        焦点移动到树中最后一个可聚焦节点上，不打开或者关闭节点
    - Enter：
        激活节点，执行默认行为，一般为打开或关闭或者选中节点(单选树)
    - 字母导航，尤其是当树中包含7个以上根节点时
        - 按下字符：将焦点移动到下一个 名字以该字符开头的节点上
        - 按下多个字符：将焦点移动到下一个 名字以字符串开头的节点上
    - 多选树种的选择模式：一般不应该要求用户按下修饰符比如  Shift or Control 键，但是当在一个列表中导航时，需要使用修饰符来保持选择状态不丢失
       -  Recommended模式： 当仅仅移动焦点时，修饰符不需要按住
            - Space: 切换当前聚焦节点的选中状态
            - Shift + Down (可选): 聚焦且选中下一个节点
            - Shift + Up (可选): 聚焦且选中上一个节点
            - Control + A (可选): 选中树中所有节点
            
- 水平方向：
    - Down 键的作用同 Right 键， 反之亦然
    - Up 键的作用同 Left 键， 反之亦然

### WAI-ARIA Roles, States, and Properties
- 树中所有的节点都应该包含在 role=tree 的元素中
- 每个树节点 赋值 role=treeitem
- 每个包含子节点的节点都应当设置 [aria-expanded](/aria?id=aria-expanded-state) 属性
- 每个父节点应包含一个 role=group 的元素来包含 role=treeitem 的子节点
- 多选树 根元素应当设置 aria-multiselectable 值为 true.
- 如果一个树不支持多选， aria-selected 属性应当只设置在 被选中的节点上，其他节点不应该出现该属性
- 如果一个树支持多选，被选中的节点上 aria-selected 值为 true，其他节点 aria-selected 值为 false
- 为组件提供一个可访问的语义化label，可使用[aria-labelledby](/aria?id=aria-labelledby-property) 或者 [aria-label](/aria?id=aria-label-property)提供
- 如果树是水平方向的，设置 [aria-orientation](/aria?id=aria-orientation-property) 值为 horizontal，默认值为 vertical

### Examples
- [material](https://material.angular.io/components/tree/overview)
- [open ajax](http://www.oaa-accessibility.org/examplep/treeview1/)
- [wai-aria-practices](https://www.w3.org/TR/wai-aria-practices/examples/treeview/treeview-1/treeview-1a.html)
- [wai-aria-practices](https://www.w3.org/TR/wai-aria-practices/examples/treeview/treeview-1/treeview-1b.html)
- [wai-aria-practices](https://www.w3.org/TR/wai-aria-practices/examples/treeview/treeview-2/treeview-2b.html)