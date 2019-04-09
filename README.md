# uni-app 浮动键盘
### 作者：诗小柒


## 开始使用
NPM 
```
npm i tki-float-keyboard
```
GIT 
```
git clone https://github.com/q310550690/tki-float-keyboard 
```

### 使用方法
在 `script` 中引入组件
``` javascript
import tkiFloatKeyboard from "@@/components/tki-float-keyboard/tki-float-keyboard.vue"
export default {
    components: {tkiFloatKeyboard}
}
```
在 `template` 中使用
``` javascript
<tki-float-keyboard ref="keyb" :mode="keyMode" :type="keyType" :title="keyTitle" @del="keyDel" @val="keyVal" @show="keyShow" @hide="keyHide"></tki-float-keyboard>
```
### 属性

|属性名|类型|默认值|可选值|说明|
|:-|:-:|:--:|:--:|-:|
|title|String|空||浮动键盘的标题|
|type| Number, String |0|mode=keyboard时 type=0全部、1字母加数字、2符号、3字母、4数字、5字母加符号、6数字加符号<br/><br/>mode=car时 type=0全部、1字母加数字、2省、3字母加数字加特、4字母、5数字<br/><br/>mode=number时 type=0全部、1禁用|键盘可用区域，配合mode属性使用|
|mode|String|keyboard|keyboard普通键盘<br/>car汽车键盘<br/>number数字键盘|键盘类型|

### 方法
|方法名|参数|默认值|说明|
|:-|:-:|:--:|-:|
|_keyShow()|||显示键盘|
|_keyHide()|||隐藏键盘|

### 事件
|事件名|返回值|说明|
|:-|:-:|-:|
|val|输入的内容|返回键盘输入内容|
|del||返回键盘输入内容|
|show|节点信息|键盘显示时触发，返回键盘节点信息|
|hide||键盘隐藏时触发|

### 6.感谢

[uni-app](https://uniapp.dcloud.io/ "uni-app")