# Button 按钮

按钮允许用户使用单击执行操作或选择。

## 引入

全局引入，在 `miniprogram` 根目录下的 `app.json` 中配置。局部引入，在需要引入的页面或组件的 `index.json` 中配置。

```json
"usingComponents": {
  "k-button": "kite-weapp/button/button"
}
```

## 代码示例

### 颜色

通过 `color` 属性设置颜色，支持 `default`、`primary`、`warning`、`danger`、`success` 五种颜色。

```wxml
<k-button>Default</k-button>
<k-button color="primary">Primary</k-button>
<k-button color="warning">Warning</k-button>
<k-button color="danger">Danger</k-button>
<k-button color="success">Success</k-button>
```

### 尺寸

通过 `size` 属性设置尺寸，支持 `small`、`default`、`large` 三种尺寸。

```wxml
<k-button size="small">Small</k-button>
<k-button>Default</k-button>
<k-button size="large">Large</k-button>
```

### 变体

通过 `variant` 属性设置变体，支持 `clear`、`default`、`outline` 三种变体，将呈现标准变体、文字变体与镂空变体。

```wxml
<k-button variant="clear">Clear</k-button>
<k-button>Default</k-button>
<k-button variant="outline">Outline</k-button>
```

### 禁用状态

通过 `disabled` 属性禁用按钮，此时按钮不可点击。

```wxml
<k-button disabled>Button</k-button>
```

### 加载状态

通过 `loading` 属性使按钮呈现加载状态，此时按钮不可点击。

```wxml
<k-button loading>Button</k-button>
```

### 图标

通过 `icon` 属性设置图标，支持 Icon 组件里的所有图标，也可以传入图片链接。

```wxml
<k-button icon="add">Button</k-button>
```

### 形状

通过 `shape` 属性设置形状，支持 `default`、`round`、`circle` 三种形状，将呈现标准形状、圆角形状和圆形形状。

```wxml
<k-button>Default</k-button>
<k-button shape="round">Round</k-button>
<k-button icon="add" shape="circle" />
```

### 展开

通过 `expand` 属性设置展开，支持 `default`、`block`、`full` 三种展开，将呈现标准展开、块状展开和块状直角展开。

```wxml
<k-button>Default</k-button>
<k-button expand="block">Block</k-button>
<k-button expand="full">Full</k-button>
```

## API

### 属性

| 参数                        | 说明                                                                                                                | 类型    | 默认值       |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------- | ------- | ------------ |
| k-id                        | 根节点 id                                                                                                           | String  | -            |
| style                       | 根结点样式                                                                                                          | String  | -            |
| color                       | 按钮颜色，可选值为 `primary`、`warning`、`danger`、`success`                                                        | String  | -            |
| size                        | 按钮尺寸，可选值为 `small`、`large`                                                                                 | String  | -            |
| variant                     | 按钮变体，可选值为 `clear`、`outline`                                                                               | String  | -            |
| disabled                    | 是否禁用按钮                                                                                                        | Boolean | -            |
| loading                     | 是否呈现加载状态                                                                                                    | Boolean | -            |
| icon                        | 左侧图标名称或图片链接，可选值见 Icon 组件                                                                          | String  | -            |
| shape                       | 按钮形状，可选值为 `round`、`circle`                                                                                | String  | -            |
| expand                      | 按钮展开，可选值为 `block`、`full`                                                                                  | String  | -            |
| lang                        | 指定返回用户信息的语言，zh_CN 简体中文，zh_TW 繁体中文，en 英文                                                     | String  | en           |
| type                        | 同小程序的 form-type                                                                                                | String  | -            |
| hover-stop-propagation      | 指定是否阻止本节点的祖先节点出现点击态                                                                              | Boolean | -            |
| hover-start-time            | 按住多久后出现点击态，单位毫秒                                                                                      | Number  | 20           |
| hover-stay-time             | 手指松开后点击态保留时间，单位毫秒                                                                                  | Number  | 70           |
| open-type                   | 微信开放能力，具体支持可参考 [微信官方文档](https://mp.weixin.qq.com/debug/wxadoc/dev/component/button.wxml)        | String  | -            |
| session-form                | 会话来源，open-type="contact" 时有效                                                                                | String  | -            |
| send-message-title          | 会话内消息卡片标题，open-type="contact" 时有效                                                                      | String  | 当前标题     |
| send-message-path           | 会话内消息卡片点击跳转小程序路径，open-type="contact" 时有效                                                        | String  | 当前分享路径 |
| send-message-img            | 会话内消息卡片图片，open-type="contact" 时有效                                                                      | String  | 截图         |
| show-message-card           | 是否显示会话内消息卡片，open-type="contact" 时有效                                                                  | Boolean | -            |
| app-parameter               | 打开 APP 时，向 APP 传递的参数，open-type="launchApp" 时有效                                                        | String  | -            |
| phone-number-no-quota-toast | 当手机号验证额度用尽时，是否对用户显示提示，open-type="getPhoneNumber" 或 open-type="getRealtimePhoneNumber" 时有效 | Boolean | true         |

### 事件

| 事件名                    | 说明                                                                             | 参数 |
| ------------------------- | -------------------------------------------------------------------------------- | ---- |
| click                     | 点击按钮，当按钮不为加载或禁用状态时触发                                         | -    |
| getuserinfo               | 点击按钮，会返回获取到的用户信息，回调的 detail 数据与 wx.getUserInfo 返回的一致 | -    |
| contact                   | 客服消息回调                                                                     | -    |
| getphonenumber            | 获取用户手机号回调                                                               | -    |
| error                     | 使用开放能力时，发生错误的回调                                                   | -    |
| opensetting               | 打开授权设置页后回调                                                             | -    |
| launchapp                 | 打开 APP 成功的回调                                                              | -    |
| chooseavatar              | 获取用户头像回调                                                                 | -    |
| agreeprivacyauthorization | 用户同意隐私协议事件回调                                                         | -    |

### 外部样式类

| 类名        | 说明         |
| ----------- | ------------ |
| k-class     | 根节点样式类 |
| hover-class | 点击态样式类 |

### CSS 变量

Button 组件提供了以下 CSS 变量，可用于自定义样式。

| 名称                              | 默认值         |
| --------------------------------- | -------------- |
| --button-default-color            | @black-color   |
| --button-default-background-color | @default-color |
| --button-default-border-color     | @default-color |
| --button-primary-color            | @white-color   |
| --button-primary-background-color | @primary-color |
| --button-primary-border-color     | @primary-color |
| --button-success-color            | @white-color   |
| --button-success-background-color | @success-color |
| --button-success-border-color     | @success-color |
| --button-warning-color            | @black-color   |
| --button-warning-background-color | @warning-color |
| --button-warning-border-color     | @warning-color |
| --button-danger-color             | @white-color   |
| --button-danger-background-color  | @danger-color  |
| --button-danger-border-color      | @danger-color  |
| --button-small-border-radius      | @radius-s      |
| --button-small-padding-inline     | 12px           |
| --button-small-height             | 30px           |
| --button-small-font-size          | @font-size-s   |
| --button-default-border-radius    | @radius-m      |
| --button-default-padding-inline   | 16px           |
| --button-default-height           | 44px           |
| --button-default-font-size        | @font-size-m   |
| --button-large-border-radius      | @radius-l      |
| --button-large-padding-inline     | 20px           |
| --button-large-height             | 50px           |
| --button-large-font-size          | @font-size-l   |
| --button-disabled-opacity         | 0.5            |
| --button-border-width             | 2px            |
| --button-font-weight              | 500            |
