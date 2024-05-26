# Grid 栅格

24 栅格系统。

## 引入

全局引入，在 `miniprogram` 根目录下的 `app.json` 中配置。局部引入，在需要引入的页面或组件的 `index.json` 中配置。

```json
"usingComponents": {
  "k-row": "kite-weapp/row/row",
  "k-col": "kite-weapp/col/col"
}
```

## 代码示例

### 基础用法

使用单一的一组 row 和 col 栅格组件，就可以创建一个基本的栅格系统。所有列（col）必须放在行（row）内。

```wxml
<k-row>
  <k-col span="8">col-8</k-col>
  <k-col span="8">col-8</k-col>
  <k-col span="8">col-8</k-col>
</k-row>
```

### 间隙

通过 `gutter` 属性设置列组件之间的间隙。如果需要垂直间隙，可以写成数组形式 `[水平间隙、垂直间隙]`。

```wxml
<k-row gutter="16">
  <k-col span="8">col-8</k-col>
  <k-col span="8">col-8</k-col>
  <k-col span="8">col-8</k-col>
</k-row>
```

### 偏移

通过 `offset` 属性设置列的偏移，例如，`offset="8"` 表示将列右偏移 8 个宽度。

```wxml
<k-row>
  <k-col span="8">col-8</k-col>
  <k-col span="8" offset="8">col-8</k-col>
</k-row>
```

### 对齐方式

通过 `justify` 属性设置列水平方向的对齐方式。

```wxml
<k-row justify="center">
  <k-col span="4">span:4</k-col>
  <k-col span="4">span:4</k-col>
</k-row>
```

通过 `align` 属性设置列垂直方向的对齐方式。

```wxml
<k-row align="midden">
  <k-col span="4" style="height: 100px">span:4</k-col>
  <k-col span="4" style="height: 50px">span:4</k-col>
</k-row>
```

### 自动换行

通过 `wrap` 属性设置列自动换行。

```wxml
<k-row wrap>
  <k-col span="8">col-8</k-col>
  <k-col span="8">col-8</k-col>
  <k-col span="8">col-8</k-col>
  <k-col span="8">col-8</k-col>
</k-row>
```

## API

### Row 属性

| 参数    | 说明                                                                                             | 类型           | 默认值 |
| ------- | ------------------------------------------------------------------------------------------------ | -------------- | ------ |
| k-id    | 根节点 id                                                                                        | String         | -      |
| style   | 根结点样式                                                                                       | String         | -      |
| gutter  | 栅格间隙                                                                                         | Array / Number | -      |
| justify | 水平对齐方式，可选值为 `start`、`center`、`end`、`space-between`、`space-around`、`space-evenly` | String         | start  |
| align   | 垂直对齐方式，可选值为 `start`、`center`、`end`、`stretch`                                       | String         | top    |
| wrap    | 元素是否自动换行                                                                                 | Boolean        | true   |

### Row 外部样式类

| 类名    | 说明         |
| ------- | ------------ |
| k-class | 根节点样式类 |

### Col 属性

| 参数   | 说明                                        | 类型   | 默认值 |
| ------ | ------------------------------------------- | ------ | ------ |
| k-id   | 根节点 id                                   | String | -      |
| style  | 根结点样式                                  | String | -      |
| span   | 栅格占位宽度，为 0 时相当于 `display: none` | Number | -      |
| offset | 栅格偏移宽度                                | Number | -      |

### Col 外部样式类

| 类名    | 说明         |
| ------- | ------------ |
| k-class | 根节点样式类 |
