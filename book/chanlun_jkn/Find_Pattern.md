# 嘉可能缠论 - 查找分型

## 查找转折形态

![](/images/jkn/pattern_01.png)

### 底分型

临近3根K线的**中间K线**是3根K线的**最低点**，同时最高点是3根K线的最低点。

### 顶分型

临近3根K线的**中间K线**是3根K线低点的**最高点**，同时最低点是3根K线的最高点。


- PineScript:

```javascript
// 查找分型
// 返回: 'top'(顶分型)/'bottom'(底分型)/''(无分型)
getPattern(ppH, ppL, pH, pL, cH, cL) =>
    if max(ppH, ph, cH) == pH and max(0ppL, pL, cL) == pL
        'top'
    else if min(ppH, ph, cH) == pH and min(ppL, pL, cL) == pL
        'bottom'
    else
        ''Find_Pattern.md
```

### 强势分型

![](/images/jkn/pattern_02.png)

### 强势下降型与上升型

![](/images/jkn/pattern_03.png)

## 下一章

- [1-4、画笔](Draw_Pen.md)
