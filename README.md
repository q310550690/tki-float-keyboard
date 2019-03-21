# uni-app 浮动键盘
### 作者：诗小柒

## 简介
使用与H5、小程序、App端的浮动键盘，键盘包括三种类型，纯数字键盘、汽车键盘、还有全键盘，所有键盘都可以自定义按键类型的禁用转态，值得体验，不懂如何使用的请直接github打包下载运行

## 开始使用
NPM 
```
npm i tki-float-keyboard
```
GIT 
```
git clone https://github.com/q310550690/tki-float-keyboard 
```
## 更新说明
+ 0.0.2 适配新版uni-app编译器(如果github上下载后使用新版HbuilderX1.7.1.20190320编译后无法启动请等待Dcloud更新即可)

### 1.引入组件
```javascript
// template 使用
<tki-float-keyboard ref="keyb" :mode="keyMode" :type="keyType" :title="keyTitle" @del="keyDel" @val="keyVal" @show="keyShow" @hide="keyHide"></tki-float-keyboard>

// 普通引入组件
import tkiFloatKeyboard from '@/components/tki-float-keyboard/tki-float-keyboard.vue'
// npm 引入
import tkiFloatKeyboard from "tki-float-keyboard"

// 注册组件
components: {
    tkiFloatKeyboard
}
```

### 2.属性
`title` String
```
title 浮动键盘的标题 默认值为空
```
`type` [Number, String]
```
type 键盘可用区域，配合mode属性使用  默认值：0

mode = keyboard 时 type = 0 全部、 1 字母加数字、 2 符号、 3 字母、 4 数字、 5 字母加符号、6 数字加符号
mode = car 时 type = 0 全部、 1 字母加数字、 2 省、 3 字母加数字加特、 4 字母、 5 数字
mode = number 时 type = 0 全部、 1 禁用.
```
`mode` String
```
mode 键盘类型  keyboard 普通键盘，car 汽车键盘，number 数字键盘
```

### 3.方法
`_keyShow()` Function
```
this.$refs.keyb._keyShow() 显示键盘
```
`_keyHide()` Function
```
this.$refs.keyb._keyHide() 隐藏键盘
```

### 4.回调
`val` Function
```
@val="keyVal" 返回键盘输入内容
keyVal(v){
    console.log(v)
}
```
`del` Function
```
@del="keyDel" 键盘退格时回调
keyDel(){
    let d = this.val
    this.val = d.substring(0,d.length-1)
}
```
`show` Function
```
@show="keyShow" 键盘显示的回调 返回键盘节点信息
keyShow(h){
    console.log(h)
}
```
`hide` Function
```
@hide="keyHide" 键盘隐藏时触发
keyHide(){
    // 做点什么
}
```

### 5.问题
暂无问题

### 6.感谢

[uni-app](https://uniapp.dcloud.io/ "uni-app")