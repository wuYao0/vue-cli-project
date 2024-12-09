# vue-cli-project

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


substring
trim
split
slice
indexOf
tounpperCase
tolowerCase


concat
push
each
map
find
filt
sort
unshift
shift
resever
splice



双向绑定
主要书通过监听器和解析模板实现的
监听器是observer循环数据 在每个对象属性上加上setter getter方法 数据发生变化时就会通知他
模板解析器时把变量解析展现在页面上 同时给数据添加订阅
watch时链接ocserver和解析器的桥梁 主要是在自身实例化时添加自己  有一个updata的方法 属性发生变化时触发解析器的回调
mvvm就是整合了他们



props
vuex
location
ref
$emit
eventBus


diff算法
比较找出差异 进行最小化更新
把虚拟dom当参数传入pathch方法进行比较
patchnode方法通过比较操作真实dom
同层进行比较 不会跨层级
从两边往中间比较