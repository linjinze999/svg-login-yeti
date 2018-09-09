# svg-login-yeti
#### 导语
> 2018年3月份，在[https://codepen.io/](https://codepen.io/)中出现了一个很有意思的登录页面[yeti login](https://codepen.io/dsenneff/pen/2c3e5bc86b372d5424b00edaf4990173)。一只小白熊会看着你输入账号，输入密码时还会捂住眼睛。
> 个人挺喜欢这种有趣的效果的，可惜没有找到开箱即用的代码，因此自己根据源代码完善了一下，可以直接使用。

## 简述
源代码依赖于`TweenMax.js`和`MorphSVGPlugin.js`实现svg动态效果。其中`TweenMax.js`免费，依赖此库可以实现本页面的基本效果；`MorphSVGPlugin.js`收费，因此我们只能放弃部分效果（张嘴和平肩）。

效果示例：
![svg-login-yeti.gif](https://i.imgur.com/9JlbggJ.gif)

以下是不同框架的实现：

## html
纯html + css + js实现，打开页面即可看到效果，见`html/index.html`

## vue
vue框架的组件，需要提前安装`gsap`：`npm install gsap --save`。`vue`目录下有两个vue组件文件：
- vue.vue：简单实现，使用了自己书写的样式
- elementUi.vue：基于[element组件库](http://element-cn.eleme.io/#/zh-CN/component/installation)实现，用了element的组件，提供表单校验、更友好的样式。需要提前安装`element-ui`：`npm install element-ui --save`

使用时将vue文件复制到你的`vue-cli`项目中，通过`import AppLogin from vue.vue`使用即可。