## aria
aria-labelledby (property)

标识一个元素内容是当前元素的label,aria-labelledby作用和aria-label是一样的，都是为object提供 accessible name，当页面上没有可视的label内容时，使用aria-label，当两个属性同时存在，在计算object的accessible name 的算法中，aria-labelledby 的优先级高于 aria-label；aria-labelledby 的值一般是页面上可视元素的ID，注意：label内容是比较简洁的；