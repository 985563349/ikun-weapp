# Flex 弹性布局

用于对齐的弹性布局容器。

## 引入

全局引入，在 `miniprogram` 根目录下的 `app.json` 中配置。局部引入，在需要引入的页面或组件的 `index.json` 中配置。

```json
"usingComponents": {
  "k-flex": "kite-weapp/flex/flex"
}
```

## 代码示例

### 垂直布局

通过 `vertical` 属性设置主轴为垂直方向。

```wxml
<k-flex vertical>
  <k-button color="primary">Button</k-button>
  <k-button color="primary">Button</k-button>
</k-flex>
```

### 对齐方式

通过 `justify` 属性设置主轴方向的对齐方式。

```wxml
<k-flex justify="center">
  <k-button color="primary">Button</k-button>
  <k-button color="primary">Button</k-button>
</k-flex>
```

通过 `align` 属性设置交叉轴方向的对齐方式。

```wxml
<k-flex align="center">
  <k-button color="primary">Button</k-button>
  <k-button color="primary">Button</k-button>
</k-flex>
```

### 间隙

通过 `gap` 属性设置元素之间的间隙，支持 `small`、`middle`、`large` 三种尺寸。

```wxml
<k-flex gap="small">
  <k-button color="primary">Button</k-button>
  <k-button color="primary">Button</k-button>
</k-flex>
```

### 换行

通过 `wrap` 属性设置元素换行方式。

```wxml
<k-flex gap="small" wrap>
  <k-button color="primary">Button</k-button>
  <k-button color="primary">Button</k-button>
  <k-button color="primary">Button</k-button>
  <k-button color="primary">Button</k-button>
  <k-button color="primary">Button</k-button>
</k-flex>
```

## API

### 属性

| 参数     | 说明                                                | 类型                                                                                | 默认值 |
| -------- | --------------------------------------------------- | ----------------------------------------------------------------------------------- | ------ |
| k-id     | 根节点 id                                           | String                                                                              | -      |
| style    | 根结点样式                                          | String                                                                              | -      |
| vertical | 主轴方向是否垂直                                    | Boolean                                                                             | -      |
| justify  | 主轴方向对齐方式                                    | [justify-content](https://developer.mozilla.org/zh-CN/docs/Web/CSS/justify-content) | -      |
| align    | 交叉轴方向对齐方式                                  | [align-items](https://developer.mozilla.org/zh-CN/docs/Web/CSS/align-items)         | -      |
| gap      | 元素之间的间隙，可选值为 `small`、`middle`、`large` | String                                                                              | -      |
| wrap     | 元素换行方式                                        | [flex-wrap](https://developer.mozilla.org/zh-CN/docs/Web/CSS/flex-wrap) / Boolean   | -      |

### 外部样式类

| 类名    | 说明         |
| ------- | ------------ |
| k-class | 根节点样式类 |
