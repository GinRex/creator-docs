# 属性参数

> 属性参数用来给已定义的属性附加元数据，类似于脚本语言的 Decorator 或者 C# 的 Attribute。

### 属性检查器相关属性

参数名 | 说明 | 类型 | 默认值 | 备注
--- | --- |:---:|:---:|---
type | 限定属性的数据类型 | (Any) | undefined | 详见 [type 参数](class.md#type)
visible | 在 **属性检视器** 面板中显示或隐藏 | boolean | (注1) | 详见 [visible 参数](class.md#visible)
displayName | 在 **属性检视器** 面板中显示为另一个名字 | string | undefined |
tooltip | 在 **属性检视器** 面板中添加属性的 Tooltip | string | undefined |
multiline | 在 **属性检视器** 面板中使用多行文本框 | boolean | false |
readonly | 在 **属性检视器** 面板中只读 | boolean | false |
min | 限定数值在编辑器中输入的最小值 | number | undefined |
max | 限定数值在编辑器中输入的最大值 | number | undefined |
step | 指定数值在编辑器中调节的步长 | number | undefined |
range | 一次性设置 min, max, step | [min, max, step] | undefined | step 值可选
slide | 在 **属性检视器** 面板中显示为滑动条 | boolean | false |

### 序列化相关属性

这些属性不能用于 get 方法

参数名 | 说明 | 类型 | 默认值 | 备注
--- | --- |:---:|:---:|---
serializable | 序列化该属性 | boolean | true | 详见 [serializable 参数](class.md#serializable)
editorOnly | 在导出项目前剔除该属性 | boolean | false |

### 其它属性

参数名 | 说明 | 类型 | 默认值 | 备注
--- | --- |:---:|:---:|---
default | 定义属性的默认值 | (Any) | undefined | 详见 [default 参数](class.md#default)
url | 该属性为指定资源的 url | `function` <br> (继承自 cc.RawAsset 的构造函数) | undefined | 详见 [获取和加载资源: Raw Asset](../load-assets.md#raw-asset)
notify | 当属性被赋值时触发指定方法 | `function (oldValue) {}` | undefined | 需要定义 default 属性并且不能用于数组
override | 当重写父类属性时需要定义该参数为 true | boolean | false | 详见 [override 参数](class.md#override)
animatable | 该属性是否能被动画修改 | boolean | true |

**注1:** visible 的默认值取决于属性名。当属性名以下划线 `_` 开头时，默认隐藏，否则默认显示。


---

继续前往 [动画系统](../../animation/index.md) 或者返回 [脚本开发](../index.md)。
