## fllex 弹性布局
### 基本概念
```css
.container {
  display: flex | inline-flex;
}
```

定义一个flex容器,为内容创建了一个新的flex环境 注意：当设置 flex 布局之后，子元素的 `float、clear、vertical-align` 的属性将会失效

## 一，容器上的6个属性

1.1， `flex-direction` 

> 决定主轴方向

<details><summary>属性值</summary>
<p>

* row（默认值）：主轴为水平方向，起点在左端。
* row-reverse：主轴为水平方向，起点在右端。
* column：主轴为垂直方向，起点在上沿。
* column-reverse：主轴为垂直方向，起点在下沿
</p>
</details>

1.2，`flex-wrap`
> 默认情况下 item都排在一条轴线上，`flex-wrap`定义一行排不下时如何换行

<details><summary>属性值</summary>
<p>

* nowrap:（默认）不换行。
* wrap: 第一行在上方。
* wrap-reverse: 第一行在下方。
</p>
</details>

1.3， `justify-content`
> item在主轴上的对齐方式

<details><summary>属性值</summary>
<p>

* flex-start（默认值）：左对齐
* flex-end：右对齐
* center： 居中
* space-between：两端对齐，项目之间的间隔都相等。
* space-around：每个项目两侧的间隔相等。所以，项目之间的间隔比项目与边框的间隔大一倍。

</p>
</details>

1,4，`align-items`

> item在交叉轴上的对齐方式

<details><summary>属性值</summary>
<p>

* stretch（默认值）：如果项目未设置高度或设为auto，将占满整个容器的高度。
* flex-start：交叉轴的起点对齐。
* flex-end：交叉轴的终点对齐。
* center：交叉轴的中点对齐。
* baseline: 项目的第一行文字的基线对齐。
</p>
</details>

1.5，`align-content`

> `align-content` 属性定义了多根轴线的对齐方式。如果项目只有一根轴线，该属性不起作用。

<details><summary>属性值</summary>
<p>

* stretch（默认值）：轴线占满整个交叉轴。
* flex-start：与交叉轴的起点对齐。
* flex-end：与交叉轴的终点对齐。
* center：与交叉轴的中点对齐。
* space-between：与交叉轴两端对齐，轴线之间的间隔平均分布。
* space-around：每根轴线两侧的间隔都相等。所以，轴线之间的间隔比轴线与边框的间隔大一倍。
</p>
</details>