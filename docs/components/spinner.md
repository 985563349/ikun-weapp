# Spinner 加载

用于页面和区块的加载中状态。

## 引入

全局引入，在 `miniprogram` 根目录下的 `app.json` 中配置。局部引入，在需要引入的页面或组件的 `index.json` 中配置。

```json
"usingComponents": {
  "k-spinner": "kite-weapp/spinner/spinner"
}
```

## 代码示例

### 颜色

通过 `color` 属性设置颜色，支持 `default`、`primary`、`warning`、`danger`、`success` 五种颜色。

```wxml
<k-spinner>Default</k-spinner>
<k-spinner color="primary" />
<k-spinner color="warning" />
<k-spinner color="danger" />
<k-spinner color="success" />
```

### 尺寸

通过 `size` 属性设置尺寸，支持 `small`、`default`、`large` 三种尺寸。

```wxml
<k-spinner size="sm" />
<k-spinner />
<k-spinner size="lg" />
```

### 描述文案

通过 `label` 属性设置描述文案。

```wxml
<k-spinner label="loading..." />
```

### 垂直布局

通过 `vertical` 属性设置加载指示符与描述文案呈垂直布局。

```wxml
<k-spinner label="loading..." vertical />
```

## API

### 属性

| 参数     | 说明                                                         | 类型    | 默认值 |
| -------- | ------------------------------------------------------------ | ------- | ------ |
| k-id     | 根节点 id                                                    | String  | -      |
| style    | 根结点样式                                                   | String  | -      |
| color    | 组件颜色，可选值为 `primary`、`warning`、`danger`、`success` | String  | -      |
| size     | 组件大小，可选值为 `small`、`large`                          | String  | -      |
| label    | 描述文案                                                     | String  | -      |
| vertical | 是否为垂直布局                                               | Boolean | false  |

### 外部样式类

| 类名    | 说明         |
| ------- | ------------ |
| k-class | 根节点样式类 |

### CSS 变量

Spinner 组件提供了以下 CSS 变量，可用于自定义样式。

| 名称                         | 默认值         |
| ---------------------------- | -------------- |
| --spinner-default-color      | @default-color |
| --spinner-primary-color      | @primary-color |
| --spinner-warning-color      | @warning-color |
| --spinner-danger-color       | @danger-color  |
| --spinner-success-color      | @success-color |
| --spinner-small-size         | 20px           |
| --spinner-default-size       | 28px           |
| --spinner-large-size         | 36px           |
| --spinner-label-font-size    | @font-size-xs  |
| --spinner-animation-duration | 0.8s           |
