区别：

1. 通过setState 修改data，实现数据影响视图

2. state在constructor 中定义
3. 写方法的时候，要在花括号中写，要改变this指向，指向组件，推荐在constructor中改

4. 父子组件传值，父组件传给子组件方法，bind this为父组件的方法，这样达到调用父组件中方法

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

   #### 

5. Fragment 而不是 template

6. 生命周期不同

7. 绑定方法，Vue中@,  react 是驼峰模式，onChange

8. 用className 代替 class

9. vue中获取 dom相关，nextTick , react 中 setState 第二个参数中

10. redux 中，没有 mutation，取代的是 reducers

11. 

