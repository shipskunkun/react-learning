汇总

2021.6.13 update


7章
修改axios，配置全局loading效果， 支持jsonp

pagenation 公共机制，定义在utils中




6章

moment 常用作用，设置date显示格式，获取当天开始时间，结束时间，传给后台







4章

router 如何定义路由 和 页面，'react-router-dom' 插件使用

```react
import {HashRouter , Route , Link, Switch} from 'react-router-dom'
```

嵌套路由，如何定义

路由匹配，动态路由参数

```react
{this.props.match.params.value}
```



3章

按需加载，什么插件，babel-plugin-import 

菜单是如何render的，data.map，递归渲染

基于axios 二次封装，jsonp，支持loading 动画

​	为啥二次封装？支持jsonp, 定义全局loading 动画的开始和结束，处理错误提示



​	跨域跟axios没什么关系，配置服务器的cros,或者jsonp，常用的跨域解决方案就可以了

​	请求百度地图服务，肯定不能设置cors， 只能通过 jsonp

​	如果 server 端是自己开发的，那么修改相关代码支持跨域即可。如果不是自己开发的，那么可以自己写个后端转发该请求，用代理的方式实现。





2章

yarn比npm三个优点

react 生命周期





1章

前端框架+路由+状态管理，

使用了哪种组件库，npm第三方插件，

公共机制的封装：

​		业务组件封装，

​		权限、菜单、API封装、axios二次封装、http错误处理、错误监控、公共utils封装、mixin等

```html
React 全家桶
	生命周期
	Router4.0
	Redux
AntD UI 组件
	基础组件
	栅格系统
	Etable，基于table组件的二次封装
	BaseForm 组件封装 
	表格内嵌单选、复选封装
公共机制封装
	axios
	http错误处理
	API封装
	权限、菜单封装
	日期、金额、手机号封装
	Loading、分页、mock
```

