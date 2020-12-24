如何创建组件

```
class WebSite extends React.Component
```

最简单的定义组件的方法是写一个 JavaScript 函数:

```
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```

Babel 将JSX编译成 `React.createElement()` 调用。

下面的两个例子是是完全相同的：

```
const element = (
  <h1 className="greeting">
    Hello, world!
  </h1>
);
const element = React.createElement(
  'h1',
  {className: 'greeting'},
  'Hello, world!'
);
```

阻止默认行为

```
 e.preventDefault();
```

不渲染

```
return null
```

## 设置状态:setState

```
setState(object nextState[, function callback])
```

参数说明

- **nextState**，将要设置的新状态，该状态会和当前的**state**合并
- **callback**，可选参数，回调函数。该函数会在**setState**设置成功，且组件重新渲染后调用。

合并nextState和当前state，并重新渲染组件。setState是React事件处理函数中和请求回调函数中触发UI更新的主要方法。

setState()并不会立即改变this.state，而是创建一个即将处理的state。setState()并不一定是同步的，为了提升性能React会批量执行state和DOM渲染。



第二个参数什么时候执行？setState 完成，且重新渲染之后执行。



**jsx 语法规则：**

 JSX 的基本语法规则：遇到 HTML 标签（以 `<` 开头），就用 HTML 规则解析；遇到代码块（以 `{` 开头），就用 JavaScript 规则解析

组件类的第一个字母必须大写，否则会报错，比如`HelloMessage`不能写成`helloMessage`。另外，组件类只能包含一个顶层标签，否则也会报错



1. this.props.children 是什么东西？

它表示组件的所有子节点

