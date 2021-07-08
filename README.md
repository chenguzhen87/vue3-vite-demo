# vue3-vite-demo
该项目主要用于学习vue3新特性

- setup 函数中获取不到this,在其他vue3钩子函数可以获取到this,但此时this是一个Proxy对象，vue2.x是一个vue组件实例对象

- vue2和vue3中$attrs行为不同，$listeners 对象在 Vue 3 中已被移除,现在事件监听器是 $attrs 的一部分,在vue2中，$attrs包含传给组件不被 prop 被识别 (且获取) 的 attribute 绑定 (class 和 style 除外),vue3中$attr包括了class、style、事件监听器(变成以on开头)、传给组件不被 prop 被识别 (且获取) 的 attribute
- 自定义组件绑定原生事件行为不同，vue2中<Test @click="onClick" />点击组件不会执行，需要加native修饰符，在vue3中去不需要，就可以直接执行

- vue3整合vue2组件报错
![preview](./assets/1625734049.jpg)
 
