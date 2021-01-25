7章

redux中处理样式的一种解决方案是 Styled-Components

transition: property duration timing-function delay 

过渡效果的css属性名称，持续时间，速度曲线函数名，延迟时间

.fade-enter {} //入场第一时刻
.fade-enter-active {} //入场第二个时刻到完成
.fade-enter-done{} //整个入场动画执行完成之后
.fade-exit{}
.fade-exit-active {} //出场第二个时刻到完成
.fade-exit-done{} //整个出场动画执行完成之后





6章

redux-thunk 使用

组件中如何使用redux?

provider 给组件提供store，组件中通过connect高阶函数，获得mapState 和 mapDispatch方法





5章

actions   // 行为，从图书馆借书。是改变 redux 应用程序中 state 的唯一方式。

store  // 存储数据的公共区域，图书馆管理员。存放State 的地方。

reducers   // 图书记录册，记账本。**reducer 是一类函数，将当前的state和action传入，返回新的state。作用是更新state特定值。**

react Components // 借书人，



reducer 接受参数和返回参数怎么记忆？action是行为，对state修改，联想。

如何把 store 和 reducer 联系起来？createStore(reducer)

组件如何通过store获取初始state？store.getState()

action是如何触发的？通过dispatch

dispatch是谁的方法？store

对action的抽象：统一管理变量，定义action方法，返回action





4章

如何理解setState 异步

为了提高性能，多次对state修改合并成一次，只执行一次render， 把三次更新合并成一次，提高效率

为什么key不是 index,

不能节点的唯一标识，在重新生成 虚拟dom的时候，可能无法缓存

**<u>比如数组删除中间一项，会导致节点key 值不稳定，key值失去存在意义</u>**

性能优化的地方：

1. 修改 this的操作，放在 constructor 中

2. setState 多次数据改变变成一次做

3. 虚拟dom, key 值

4. 借助shouldComponentUpdate ， 避免无谓的代码更新

   



3章

单项数据流：子组件中接受父组件中值，但是不能直接改变传过来的值

