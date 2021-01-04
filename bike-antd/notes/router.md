学习网站：

https://reactrouter.com/web/guides/quick-start



Link:

```
<Link to="/about">About</Link>
```

vue：

```html
<router-link
  to="/about"
  v-slot="{ href, route, navigate, isActive, isExactActive }"
>
```



url 参数

```react
<Switch>
	<Route path="/:id" children={<Child />} />
</Switch>
let { id } = useParams();
```



重定向：

```react
 <Redirect
 to={{
 pathname: "/login",
 state: { from: location }
 }}
 />
```









