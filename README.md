# wepy-com-toast

一个 toast 消息框组件。

此组件依赖 [wepy](https://github.com/Tencent/wepy) 1.7.0+。

如果你正在使用 wepy 2.x，请移步 [wepy2-com-toast](https://github.com/fudiwei/wepy2-com-toast)。

---

## 用法

安装：

``` shell
npm install @step/wepy-com-toast --save
```

导入：

``` html
<template>
    <ui-toast />
</template>
<script>
    import wepy from 'wepy';
    import UIToast from '@step/wepy-com-toast';

    export default class DemoPage extends wepy.page {
        components = {
            'ui-toast': UIToast
        };
    }
</script>
```

### 可配置项

#### 属性：

*无*

#### 方法：

``` javascript
/**
 * 显示消息对话框。
 * @param {Object} options 配置项。
 * @param {String} options.content 提示文本。
 * @param {String} options.position 对话框出现在屏幕的位置，支持“top”、“center”、“bottom”，默认值为“bottom”。
 * @param {String} options.duration 指定对话框若干毫秒后自动消失，默认值为“2000”。
 */
this.$invoke('ui-toast', 'show', {
    content: '这是一条消息',
    position: 'center',
    duration: 3000
});

/**
 * 显示消息对话框。
 * @param {String} content 消息文本。
 */
this.$invoke('ui-toast', 'show', '这是一条消息');

/**
 * 隐藏消息对话框。
 */
this.$invoke('ui-toast', 'hide');
```