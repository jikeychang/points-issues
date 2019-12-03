## 页面间路由传参

#### 方案一：URL传参
```js
//调用时打开新页面
showDetail(id) {
  this.$router.push({
    path: `/roleEdit/${id}`,
  })
}

//对应路由配置
{
  path: '/roleEdit/:id',
  name: 'roleEdit',
  component: roleEdit
}

//子组件获取传递的参数值
this.$route.params.id
```

#### 方案二：匹配name来传参

```js
// // 调用时打开新页面
showDialog(obj) {
  // this.setRoleParamObj(obj) //vuex中赋值;
  this.$router.push({
    name: 'RoleEdit',
    params: obj,
  });
},

//对应路由
{
  path: '/roleEdit',
  name: 'roleEdit',
  component: roleEdit
}

//子组件获取值
this.paramObj = this.$route.params

```

#### 方案三：query传参
父组件：使用path来匹配路由，然后通过query来传递参数
这种情况下 query传递的参数会显示在url后面?id=？

```js
//调用打开新页面
showDialog(id) {
  this.$router.push({
    path: '/roleEdit',
    query: {
      id: id
    }
  })
}

//路由配置
{
  path: '/roleEdit',
  name: 'roleEdit',
  component: roleEdit
}

//子组件获取参数
this.$route.query.id
```