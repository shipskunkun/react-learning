区别：

1. 通过setState 修改data，实现数据影响视图

2. state在constructor 中定义
3. 写方法的时候，要在花括号中写，要改变this指向，指向组件，推荐在constructor中改

 ```react
constructor() {
  this.onChange = this.onChange.bind(this)
}

 ```
4. 父子组件传值，父组件传给子组件方法，bind this为父组件的方法，这样达到调用父组件中方法

子组件的 constructor 也需要 bind this

   而vue 中是 emit 方法，调用注册在父组件中的方法，不用修改this指向这样子

   ```react
   // 父组件中
   <TodoItem
     	content={item}
     	index={index}
     	deleteItem={this.handleItemDelete.bind(this)}
   />
   
   //子组件中
   handleClick() {
     this.props.deleteItem(this.props.index)
   }
   ```

5. Fragment 而不是 template

6. 生命周期不同

7. 绑定方法，Vue中@,  react 是驼峰模式，onChange

8. 用className 代替 class

9. vue中获取 dom相关，nextTick , react 中 setState 第二个参数中

10. redux 中，没有 mutation，取代的是 reducers

11. 样式隔离，Vue 使用 scoped， react 中使用 插件管理



代码：

12. 打包后 vue 在dist 中， react 在public 中

13. vue方法需要卸载methods 中， react不需要

14. vue中命中路由，监听 location ，react 中 通过 switch 匹配的方式。

    ​	vue中，配置嵌套路由，在 vue-router 中通过对象数组配置

    ​	react 中 ，通过 HashRouter 或者 BrowserRouter  + switch，做路由匹配。

15. 调用方法

    ​	如果不写 bind(this)  就要在方法定义的时候使用箭头函数

    ​	方法一：	

    ```react
    <Button type="primary" onClick={this.handleCloseLoading}>关闭</Button>
    
    handleCloseLoading=()=>{
      this.setState({
        loading:false
      });
    }
    ```

    ​	方法二：

    

    ```react
    <Button type="primary" onClick={this.handleCloseLoading.bind(this)}>关闭</Button>
    
    handleCloseLoading(){
      this.setState({
        loading:false
      });
    }
    ```

    ​	

16. 