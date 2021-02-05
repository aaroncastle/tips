# tips
- CSS:
    - 宽度已知，高度未知。获得一个正方形的元素的方法



- 单行文本溢出隐藏并打点
```css
     div{
        white-space: nowrap;
        overflow: hidden;
        text-overflow-ellipsis: ellipsis;   
     }
```
- 多行文本溢出隐藏并打点
```css
    div{
        display: -webkit-box;           /*设置盒模型为伸缩盒*/
        -webkit-box-orient: vertical;   /*设置伸缩盒内子元素排列方式为 vertical */
        -webkit-line-clamp: 2;          /*设置盒内文本的展示行数*/
        overflow: hidden;
    }
```
- 设置元素不可被用户选中
```css
    div{
        user-select: none;
    }
```
- css计数器  一般多用于li，让其自动计数从1开始（非从0开始）
```css
    div{
        counter-reset: kaivon;
    }
    div:before{
        counter-increment: kaivon;
        content: counter(kaivon);
    }
```
------
```css
    pointer-events: none;
```
> 有此属性且值为'none'的元素，不会接受任何的鼠标事件。但如果子元素也有此属性但是别的值会有正常的捕获与冒泡事件的传递
