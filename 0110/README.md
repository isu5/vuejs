
### 1.自定义样式style.css

`cd assets`

创建 css/style.css 文件


### 2.引入自定义css 文件

nano App.vue

```
# 这里必须是该文件对应style.css 的相对路径

import './assets/css/style.css'  //在js里边引入

<div class="myclass">hello world!</div>

```


## 工程说明

1. 所有组件都被统一放在工程中的组件文件夹下

`{myproject}/src/components/* `

2. 组件格式

* template : 组件html内容

* script: 组件js脚本(ES6)

* style: 组件css样式

### html示例

```
<template>
	<div class="container">
		<h2>{{msg}}</h2>
	</div>
</template>

<script>
export default{
	name:'HelloWorld',
	data (){
		return {
			msg: '欢迎使用vuejs'
		}
	}
}
</script>

<style scoped>
h2{
	font-weight:normal;
	color:red;
}
</style>
```



















