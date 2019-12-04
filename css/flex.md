## fllex 弹性布局
### 基本概念
```css
.container {
  display: flex | inline-flex;
}
```

定义一个flex容器,为内容创建了一个新的flex环境 注意：当设置 flex 布局之后，子元素的 `float、clear、vertical-align` 的属性将会失效

## 一，容器上的6个属性

1.1， `flex-direction` 决定主轴方向
<details><summary>属性值</summary>
<p>

* row（默认值）：主轴为水平方向，起点在左端。
* row-reverse：主轴为水平方向，起点在右端。
* column：主轴为垂直方向，起点在上沿。
* column-reverse：主轴为垂直方向，起点在下沿
</p>
</details>

1.2，`flex-wrap`
> 默认情况下 item都排在一条轴线上，`flex-wrap`定义一行拍不下时如何换行

<details><summary>属性值</summary>
<p>

* nowrap:（默认）不换行。
* wrap: 第一行在上方。
* wrap-reverse: 第一行在下方。
</p>
</details>